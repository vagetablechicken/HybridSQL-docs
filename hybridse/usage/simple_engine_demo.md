# Design a simple SQL engine 

In this article, we try to help developers to build their own SQL engine. We just simply our storage system by using a memory table so that we can pay more attention on implementation of engine.

Before deeply insight the details, let's  briefly outline how to design simple SQL engine with HybridSE:

1. Design memory table storage
2. Implement Catalog and TableHandler, e.g, `SimpleCatalog`, `SimpleTableHandler`.
3. Build and execute engine

More detail  : [simple_engine_demo](https://github.com/4paradigm/HybridSE/blob/main/src/cmd/simple_engine_demo.cc)

## 1. Memory table storage

<img src="images/image-simple-storage.png" alt="image-20210326122554032" align="left" style="zoom:50%;" />

```c++
typedef std::deque<std::pair<uint64_t, Row>> MemTimeTable;
typedef std::map<std::string, MemTimeTable> MemSegmentMap;
```

- Our memory table support multi-indexes. And each index binds to a `SegmentMemMap`. 
- `SegmentMemMap` is a `map<Key,MemTimeTable>` where `key` is index key string。Rows with same keys will be collected together, ordered by time and added into the same `MemTimeTable` .

## 2. Catalog Implementation 

### [SimpleCatalog](https://github.com/4paradigm/HybridSE/blob/main/src/vm/simple_catalog.h)

In order to create a HybridSE Engine for our own purpose, we have to implement a  `Catalog` class specifically adapt to our Strorage system. That means it will contain  the infomation of the dataset and will define a set of operations to access the memory table  efficiently. 

#### Fields

We use `database_` and `table_handler to maintain and manage database and table。`type::Database is our Database prototype and `SimpleCatalogTableHandler` will be discussed later.

#### Functions

Here, we list some implementations (More detail can be found from [simple_catalog.h](https://github.com/4paradigm/HybridSE/blob/main/src/vm/simple_catalog.h) and [simple_catalog.cc](https://github.com/4paradigm/HybridSE/blob/main/src/vm/simple_catalog.cc)）

- Constructor

The constructor initialize the `enable_index` to enable or disable index-based-optimization.  And the database and table meta and data are empty.

```c++
SimpleCatalog::SimpleCatalog(const bool enable_index)
    : enable_index_(enable_index) {}
SimpleCatalog::~SimpleCatalog() {}
bool SimpleCatalog::IndexSupport() { return enable_index_; }
```

- GetDatabases and GetTable

```c++
std::map<std::string, std::shared_ptr<type::Database>> databases_;
std::map<std::string,
             std::map<std::string, std::shared_ptr<SimpleCatalogTableHandler>>>
        table_handlers_;
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

- AddDatabases and InsertRows

Actually, `AddDatabase` and `InsertRows`  aren't  necessity for a  `Catalog` class, but here we truely need them to help us to initialize  database and to prepare data.

### [SimpleCatalogTableHandler](https://github.com/4paradigm/HybridSE/blob/main/src/vm/simple_catalog.h)

#### Fields

Internally, we maintain `table_storage` to maintain and manage the [memory table storage](#1. memory table storage)：

``` c++
std::map<std::string, std::shared_ptr<MemPartitionHandler>> table_storage;
```

`MemPartitionHandler` is a  `TableHandler` implementation. It makes it very convenient to`GetWindowIterator`.

At the same time, we also use `full_table_storage_` to store full table data. Although, it is kind of memory costly, it simply  implement `GetIterator`.

```c++
std::shared_ptr<MemTableHandler> full_table_storage_;
```

#### Functions

Here, we list some implementations (More detail can be found here: [simple_catalog.h](https://github.com/4paradigm/HybridSE/blob/main/src/vm/simple_catalog.h)和[simple_catalog.cc](https://github.com/4paradigm/HybridSE/blob/main/src/vm/simple_catalog.cc))

- Constructor

At the very beginning, we have to initialize the table infomations, e.g.,  `TableDef`, `IndexHint` and `Types`

- Get table  infomation 

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

- GetPartition and GetWindowIterator

`MemPartitionHandler makes it easy to implement   `GetPartition() ` and   `GetWindowIterator()

```c++
std::shared_ptr<PartitionHandler> SimpleCatalogTableHandler::GetPartition(
  const std::string &index_name) {    
  	if (table_storage.find(index_name) == table_storage.end()) {        
      return nullptr;    
    } else {        
      return table_storage[index_name];    
    }
}

std::unique_ptr<WindowIterator> SimpleCatalogTableHandler::GetWindowIterator(
    const std::string &index_name) {
    if (table_storage.find(index_name) == table_storage.end()) {
        return nullptr;
    } else {
        return table_storage[index_name]->GetWindowIterator();
    }
}
```

More details: [MemPartitionHandler::GetWindowIterator()](https://github.com/4paradigm/HybridSE/blob/main/src/vm/mem_catalog.cc)

- GetIterator

Then we can simplity implement `GetIterator` by returning the `full_table_storage_->GetIterator()`

```c++
std::unique_ptr<RowIterator> SimpleCatalogTableHandler::GetIterator() {
    return full_table_storage_->GetIterator();
}
```

More details: [MemTableHandler::GetIterator()](https://github.com/4paradigm/HybridSE/blob/main/src/vm/mem_catalog.cc)

- GetCount and At

If we are not ready for some operation, we can just return `0` or `null`. Sorry do not support error system currently.

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

## 3. Build and execute engine

### Build engine

- Prepare Catalog

```c++
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
```

- Prepare data

```c++
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
```

- Config `EngineOption`

We simply use default `EngineOptions`

```c++
EngineOptions options;
```

- Build `Engine`

```c++
Engine engine(catalog, options);
```

### Compile and execute SQL

- Compile SQL

```c++
std::string sql = "select col0, col1, col2, col1+col2 as col12 from t1;";
base::Status get_status;
BatchRunSession session;
// compile sql
if (!engine.Get(sql, "simple_db", session, get_status) ||
    get_status.code != common::kOk) {
  return SIMPLE_ENGINE_COMPILE_ERROR;
}
```

- Execute SQL

```c++
std::vector<Row> outputs;
// run sql query
if (0 != session.Run(outputs)) {
  return SIMPLE_ENGINE_RUN_ERROR;
}
// print result
PrintRows(session.GetSchema(), outputs);
```

## 4. Run SimpleEngineDemo

```shell
cd hybridse/build
cmake .. 
make simple_engine_demo
./src/simple_engine_demo
```
