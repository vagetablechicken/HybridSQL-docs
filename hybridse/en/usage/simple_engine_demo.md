# Design a simple Engine based on HybridSE

HybridSE提供C++编程接口，用户可以在C/C++项目中使用[HybridSE的C++SDK](../usage/api/c++/reference.md)实现自己的引擎。

## First step: Implement SimpleCatalog and SimpleTableHandler

In order to create a HybridSE Engine for our own purpose, we have to implement a  `Catalog` class specifically adapt to our Strorage system. That means it will contain  the infomation of the dataset and will define a set of operations to access data efficiently. 

### SimpleCatalog

In this case, we just simplily implement a `SimpleCatalog`, where two maps( `table_handlers_` and `databases_` ) are adopted to manage the database and table information and data.

```c++
/**
 * Simple Catalog without actual data bindings.
 */
class SimpleCatalog : public Catalog {
 public:
    explicit SimpleCatalog(const bool enable_index = false);
    SimpleCatalog(const SimpleCatalog &) = delete;
    ~SimpleCatalog();
    std::shared_ptr<type::Database> GetDatabase(const std::string &db) override;
    std::shared_ptr<TableHandler> GetTable(
        const std::string &db, const std::string &table_name) override;
    bool IndexSupport() override;

  	void AddDatabase(const hybridse::type::Database &db);
    bool InsertRows(const std::string &db, const std::string &table,
                    const std::vector<Row> &row);
 private:
    bool enable_index_;
    std::map<std::string,
             std::map<std::string, std::shared_ptr<SimpleCatalogTableHandler>>>
        table_handlers_;
    std::map<std::string, std::shared_ptr<type::Database>> databases_;
};

```

```c++
SimpleCatalog::SimpleCatalog(const bool enable_index)
    : enable_index_(enable_index) {}
SimpleCatalog::~SimpleCatalog() {}
bool SimpleCatalog::IndexSupport() { return enable_index_; }
```

```c++
std::shared_ptr<type::Database> SimpleCatalog::GetDatabase(
    const std::string &db_name) {
    return databases_[db_name];
}
```

```c++
std::shared_ptr<TableHandler> SimpleCatalog::GetTable(
    const std::string &db_name, const std::string &table_name) {
    auto &dict = table_handlers_[db_name];
    return dict[table_name];
}
```

#### Additinal functions

`AddDatabase` and `InsertRows`  aren't  necessary for a  `Catalog` class, but here we truely need them to help us to initialize  database and prepare data.

```c++
void SimpleCatalog::AddDatabase(const hybridse::type::Database &db) {
    auto &dict = table_handlers_[db.name()];
    for (int k = 0; k < db.tables_size(); ++k) {
        auto tbl = db.tables(k);
        dict[tbl.name()] =
            std::make_shared<SimpleCatalogTableHandler>(db.name(), tbl);
    }
    databases_[db.name()] = std::make_shared<hybridse::type::Database>(db);
}
bool SimpleCatalog::InsertRows(const std::string &db_name,
                               const std::string &table_name,
                               const std::vector<Row> &rows) {
    auto table = GetTable(db_name, table_name);
    if (!table) {
        LOG(WARNING) << "table:" << table_name
                     << " isn't exist in db:" << db_name;
    }
    for (auto &row : rows) {
        if (!std::dynamic_pointer_cast<SimpleCatalogTableHandler>(table)
                 ->AddRow(row)) {
            return false;
        }
    }
    return true;
}
```



### SimpleTableHandler



 `MemPartitionHandler` and `MemTableHandler`  make it easy to implement a memory table storage.

```c++

class SimpleCatalogTableHandler : public TableHandler {
 public:
    explicit SimpleCatalogTableHandler(const std::string &db_name,
                                       const hybridse::type::TableDef &);
  	// decalre TableHandler funtions
    const Schema *GetSchema() override;
  	// ... 

  	// functions for data preparation
    bool AddRow(const Row row);
    bool DecodeKeysAndTs(const IndexSt &index, const int8_t *buf, uint32_t size,
                         std::string &key, int64_t *time_ptr);  // NOLINT

 private:
    std::string db_name_;
    hybridse::type::TableDef table_def_;
    Types types_dict_;
    IndexHint index_hint_;
    codec::RowView row_view_;
    std::map<std::string, std::shared_ptr<MemPartitionHandler>> table_storage;
    std::shared_ptr<MemTableHandler> full_table_storage_;
};
```

At the very beginning, we have to initialize tablehandler with `TableDef`

```c++
SimpleCatalogTableHandler::SimpleCatalogTableHandler(
    const std::string &db_name, const hybridse::type::TableDef &table_def)
    : db_name_(db_name),
      table_def_(table_def),
      row_view_(table_def_.columns()) {
    // build col info and index info
    // init types var
    for (int32_t i = 0; i < table_def.columns_size(); i++) {
        const type::ColumnDef &column = table_def.columns(i);
        codec::ColInfo col_info(column.name(), column.type(), i, 0);
        types_dict_.insert(std::make_pair(column.name(), col_info));
    }

    // init index hint
    for (int32_t i = 0; i < table_def.indexes().size(); i++) {
        const type::IndexDef &index_def = table_def.indexes().Get(i);
        vm::IndexSt index_st;
        index_st.index = i;
        index_st.ts_pos = ::hybridse::vm::INVALID_POS;
        if (!index_def.second_key().empty()) {
            int32_t pos = GetColumnIndex(index_def.second_key());
            if (pos < 0) {
                LOG(WARNING)
                    << "fail to get second key " << index_def.second_key();
                return;
            }
            index_st.ts_pos = pos;
        } else {
            DLOG(INFO) << "init table with empty second key";
        }
        index_st.name = index_def.name();
        for (int32_t j = 0; j < index_def.first_keys_size(); j++) {
            const std::string &key = index_def.first_keys(j);
            auto it = types_dict_.find(key);
            if (it == types_dict_.end()) {
                LOG(WARNING) << "column " << key << " does not exist in table "
                             << table_def.name();
                return;
            }
            index_st.keys.push_back(it->second);
        }
        index_hint_.insert(std::make_pair(index_st.name, index_st));
        table_storage.insert(std::make_pair(
            index_st.name, std::make_shared<MemPartitionHandler>()));
    }
    full_table_storage_ = std::make_shared<MemTableHandler>();
}
```



Getting basic information, e.g, schem, index, table name, are implemented as follow:

```c++

const Types &SimpleCatalogTableHandler::GetTypes() { return this->types_dict_; }

const IndexHint &SimpleCatalogTableHandler::GetIndex() {
    return this->index_hint_;
}

const Schema *SimpleCatalogTableHandler::GetSchema() {
    return &this->table_def_.columns();
}

const std::string &SimpleCatalogTableHandler::GetName() {
    return this->table_def_.name();
}

const std::string &SimpleCatalogTableHandler::GetDatabase() {
    return this->db_name_;
}
```

Then we can simplity implement `GetIterator` by returning the `full_table_storage_->GetIterator()`

```c++
std::unique_ptr<WindowIterator> SimpleCatalogTableHandler::GetWindowIterator(
    const std::string &index_name) {
    if (table_storage.find(index_name) == table_storage.end()) {
        return nullptr;
    } else {
        return table_storage[index_name]->GetWindowIterator();
    }
}
std::shared_ptr<PartitionHandler> SimpleCatalogTableHandler::GetPartition(
    const std::string &index_name) {
    if (table_storage.find(index_name) == table_storage.end()) {
        return nullptr;
    } else {
        return table_storage[index_name];
    }
}
std::unique_ptr<RowIterator> SimpleCatalogTableHandler::GetIterator() {
    return full_table_storage_->GetIterator();
}
RowIterator *SimpleCatalogTableHandler::GetRawIterator() {
    return full_table_storage_->GetRawIterator();
}
```

If we are not ready for some operation, we can just ignore it.

```c++
const uint64_t SimpleCatalogTableHandler::GetCount() { 
  LOG(ERROR) << "Unsupported operation: GetCount()";
  return 0; 
}
hybridse::codec::Row SimpleCatalogTableHandler::At(uint64_t pos) {
    LOG(ERROR) << "Unsupported operation: At()";
    return hybridse::codec::Row();
}
```



```c++
using namespace llvm;       // NOLINT (build/namespaces)
using namespace llvm::orc;  // NOLINT (build/namespaces)
namespace fesql {
namespace cmd {
// ...
int run() {
    // build Simple Catalog
    auto catalog = std::make_shared<SimpleCatalog>(true);
    // database simple_db
    fesql::type::Database db;
    db.set_name("simple_db");

    // prepare table t1 schema and data
    fesql::type::TableDef table_def;
    {
        table_def.set_name("t1");
        table_def.set_catalog("db");
        {
            ::fesql::type::ColumnDef* column = table_def.add_columns();
            column->set_type(::fesql::type::kVarchar);
            column->set_name("col0");
        }
        {
            ::fesql::type::ColumnDef* column = table_def.add_columns();
            column->set_type(::fesql::type::kInt32);
            column->set_name("col1");
        }
        {
            ::fesql::type::ColumnDef* column = table_def.add_columns();
            column->set_type(::fesql::type::kInt64);
            column->set_name("col2");
        }
    }
    *(db.add_tables()) = table_def;
    catalog->AddDatabase(db);

    // insert data into simple_db
    std::vector<Row> t1_rows;
    for (int i = 0; i < 10; ++i) {
        std::string str1 = "hello";
        codec::RowBuilder builder(table_def.columns());
        uint32_t total_size = builder.CalTotalLength(str1.size());
        int8_t* ptr = static_cast<int8_t*>(malloc(total_size));
        builder.SetBuffer(ptr, total_size);
        builder.AppendString(str1.c_str(), str1.size());
        builder.AppendInt32(i);
        builder.AppendInt64(1576571615000 - i);
        t1_rows.push_back(Row(base::RefCountedSlice::Create(ptr, total_size)));
    }
    if (!catalog->InsertRows("simple_db", "t1", t1_rows)) {
        return SIMPLE_ENGINE_DATA_ERROR;
    }

    // build simple engine
    EngineOptions options;
    Engine engine(catalog, options);
    std::string sql = "select col0, col1, col2, col1+col2 as col12 from t1;";
    {
        base::Status get_status;
        BatchRunSession session;
        // compile sql
        if (!engine.Get(sql, "simple_db", session, get_status) ||
            get_status.code != common::kOk) {
            return SIMPLE_ENGINE_COMPILE_ERROR;
        }
        std::vector<Row> outputs;
        // run sql query
        if (0 != session.Run(outputs)) {
            return SIMPLE_ENGINE_RUN_ERROR;
        }
        PrintRows(session.GetSchema(), outputs);
    }
    return SIMPLE_ENGINE_RET_SUCCESS;
}

}  // namespace cmd
}  // namespace fesql

int main(int argc, char** argv) {
    InitializeNativeTarget();
    InitializeNativeTargetAsmPrinter();
    return fesql::cmd::run();
}

```

#### 编译和运行SimpleEngineDemo

```shell
cd hybridse/build
cmake .. 
make simple_engine_demo
./src/simple_engine_demo
```

