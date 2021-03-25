# Catalog

`include <vm/catalog.h>`

## Summary

 `Catalog` class is the Catalog interface for HybridSE. Users should implement their own  `Catalog`

| Constructors and Destructors |
| :--------------------------- |
| [Catalog](#Catalog)          |

| Public functions                      | Return type                                |
| :------------------------------------ | ------------------------------------------ |
| [IndexSupport](#IndexSupport)         | `Bool`                                     |
| [GetDatabase](#GetDatabase)           | `std::shared_ptr<type::Database`>          |
| [GetTable](#GetTable)                 | `std::shared_ptr<TableHandler>`            |
| [GetProcedureInfo](#GetProcedureInfo) | std::shared_ptr<fesql::sdk::ProcedureInfo> |

## Public functions

#### Catalog

```c++
Catalog() {}
```

Construct an Catalog 

#### IndexSupport

```c++
virtual bool IndexSupport() = 0;
```

Return `true` if index based optimization is enable, otherwise return `false`

#### GetDatabase

```c++
// get database information
virtual std::shared_ptr<type::Database> GetDatabase(
    const std::string& db) = 0;
```

Return `Database` instance with given dababase name `db`

#### GetTable

```c++
// get table handler
virtual std::shared_ptr<TableHandler> GetTable(
    const std::string& db, const std::string& table_name) = 0;
```

Return `TableHandler` instance with given dababase name `db`

#### GetProcedureInfo

```c++
virtual std::shared_ptr<fesql::sdk::ProcedureInfo> GetProcedureInfo(
    const std::string& db, const std::string& sp_name) = 0;
```

Return `ProcedureInfo` instance with given dababase name `db` and procedure name `sp_name`