## 编译

### 使用Docker镜像。
```shell
docker run -it develop-registry.4pd.io/centos6_gcc7_fesql:master bash
```


## 从源码编译项目
```shell
git clone git@github.com:4paradigm/hybridse.git

mkdir -p ./hybridse/build
cd ./hybridse/build/

cmake ..
make -j4
```

## C++编程接口
HybridSE提供C++编程接口，用户可以在C/C++项目中使用来编译SQL以及生成最终的可执行代码。[C++API文档](../usage/api/c++/reference.md)

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



## Java编程接口
HybridSE也提供Java编程接口，基于Java/Scala的项目也可以使用来实现SQL语法支持，详情参考HybridSE Java SDK。


## 示例： 一个简单NewSQL数据库
开发者使用HybridSE可以快速实现一个支持SQL的高性能数据库。examples/toydb就是一个简易的单机版面向实时决策的NewSQL数据库。

[ToyDB快速使用手册](./toydb_tutorial/toydb_usage.md)