---
title: hybridse::vm::Catalog

---

# hybridse::vm::Catalog



 [More...](#detailed-description)


`#include <catalog.h>`

Inherited by [hybridse::vm::MemCatalog](/Classes/classhybridse_1_1vm_1_1_mem_catalog.md)

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[Catalog](/Classes/classhybridse_1_1vm_1_1_catalog.md#function-catalog)**() |
| virtual | **[~Catalog](/Classes/classhybridse_1_1vm_1_1_catalog.md#function-~catalog)**() |
| virtual bool | **[IndexSupport](/Classes/classhybridse_1_1vm_1_1_catalog.md#function-indexsupport)**() =0<br>Implemented by subclasses return whether index is supported or not.  |
| virtual std::shared_ptr< type::Database > | **[GetDatabase](/Classes/classhybridse_1_1vm_1_1_catalog.md#function-getdatabase)**(const std::string & db) =0<br>Implemented by subclasses to return database information.  |
| virtual std::shared_ptr< [TableHandler](/Classes/classhybridse_1_1vm_1_1_table_handler.md) > | **[GetTable](/Classes/classhybridse_1_1vm_1_1_catalog.md#function-gettable)**(const std::string & db, const std::string & table_name) =0<br>Implemented by subclasses to return a table handler with given table name.  |
| virtual std::shared_ptr< hybridse::sdk::ProcedureInfo > | **[GetProcedureInfo](/Classes/classhybridse_1_1vm_1_1_catalog.md#function-getprocedureinfo)**(const std::string & db, const std::string & sp_name)<br>Return `ProcedureInfo` instance with given database name `db` and procedure name `sp_name` |

## Detailed Description

```cpp
class hybridse::vm::Catalog;
```


`[Catalog](/Classes/classhybridse_1_1vm_1_1_catalog.md)` class defines a set of operation for, e.g, database, table and index management. Users should implement the subclasses for their own purpose 

## Public Functions Documentation

### function Catalog

```cpp
inline Catalog()
```


### function ~Catalog

```cpp
inline virtual ~Catalog()
```


### function IndexSupport

```cpp
virtual bool IndexSupport() =0
```

Implemented by subclasses return whether index is supported or not. 

**Reimplemented by**: [hybridse::vm::MemCatalog::IndexSupport](/Classes/classhybridse_1_1vm_1_1_mem_catalog.md#function-indexsupport)


### function GetDatabase

```cpp
virtual std::shared_ptr< type::Database > GetDatabase(
    const std::string & db
) =0
```

Implemented by subclasses to return database information. 

**Reimplemented by**: [hybridse::vm::MemCatalog::GetDatabase](/Classes/classhybridse_1_1vm_1_1_mem_catalog.md#function-getdatabase)


### function GetTable

```cpp
virtual std::shared_ptr< TableHandler > GetTable(
    const std::string & db,
    const std::string & table_name
) =0
```

Implemented by subclasses to return a table handler with given table name. 

**Reimplemented by**: [hybridse::vm::MemCatalog::GetTable](/Classes/classhybridse_1_1vm_1_1_mem_catalog.md#function-gettable)


### function GetProcedureInfo

```cpp
inline virtual std::shared_ptr< hybridse::sdk::ProcedureInfo > GetProcedureInfo(
    const std::string & db,
    const std::string & sp_name
)
```

Return `ProcedureInfo` instance with given database name `db` and procedure name `sp_name`

-------------------------------

Updated on 28 March 2021 at 19:23:48 PDT