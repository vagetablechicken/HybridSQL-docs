---
title: hybridse::vm::MemCatalog

---

# hybridse::vm::MemCatalog




`#include <mem_catalog.h>`

Inherits from [hybridse::vm::Catalog](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_catalog.md)

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[MemCatalog](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_catalog.md#function-memcatalog)**() |
| | **[~MemCatalog](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_catalog.md#function-~memcatalog)**() |
| bool | **[Init](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_catalog.md#function-init)**() |
| virtual std::shared_ptr< type::Database > | **[GetDatabase](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_catalog.md#function-getdatabase)**(const std::string & db)<br>Implemented by subclasses to return database information.  |
| virtual std::shared_ptr< [TableHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_table_handler.md) > | **[GetTable](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_catalog.md#function-gettable)**(const std::string & db, const std::string & table_name)<br>Implemented by subclasses to return a table handler with given table name.  |
| virtual bool | **[IndexSupport](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_catalog.md#function-indexsupport)**() override<br>Implemented by subclasses return whether index is supported or not.  |

## Additional inherited members

**Public Functions inherited from [hybridse::vm::Catalog](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_catalog.md)**

|                | Name           |
| -------------- | -------------- |
| | **[Catalog](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_catalog.md#function-catalog)**() |
| virtual | **[~Catalog](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_catalog.md#function-~catalog)**() |
| virtual std::shared_ptr< hybridse::sdk::ProcedureInfo > | **[GetProcedureInfo](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_catalog.md#function-getprocedureinfo)**(const std::string & db, const std::string & sp_name)<br>Return `ProcedureInfo` instance with given database name `db` and procedure name `sp_name` |


## Public Functions Documentation

### function MemCatalog

```cpp
MemCatalog()
```


### function ~MemCatalog

```cpp
~MemCatalog()
```


### function Init

```cpp
bool Init()
```


### function GetDatabase

```cpp
inline virtual std::shared_ptr< type::Database > GetDatabase(
    const std::string & db
)
```

Implemented by subclasses to return database information. 

**Reimplements**: [hybridse::vm::Catalog::GetDatabase](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_catalog.md#function-getdatabase)


### function GetTable

```cpp
inline virtual std::shared_ptr< TableHandler > GetTable(
    const std::string & db,
    const std::string & table_name
)
```

Implemented by subclasses to return a table handler with given table name. 

**Reimplements**: [hybridse::vm::Catalog::GetTable](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_catalog.md#function-gettable)


### function IndexSupport

```cpp
inline virtual bool IndexSupport() override
```

Implemented by subclasses return whether index is supported or not. 

**Reimplements**: [hybridse::vm::Catalog::IndexSupport](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_catalog.md#function-indexsupport)


-------------------------------

Updated on 28 March 2021 at 19:34:49 PDT