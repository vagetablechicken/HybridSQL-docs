---
title: hybridse::vm::Catalog
summary: A Catalog handler which defines a set of operation for, e.g, database, table and index management. 

---
# hybridse::vm::Catalog



`#include <catalog.h>`

A [Catalog]() handler which defines a set of operation for, e.g, database, table and index management. 
## Summary

```cpp
class hybridse::vm::Catalog;
```
A [Catalog]() handler which defines a set of operation for, e.g, database, table and index management. 

Users should implement the subclasses for their own purpose 



|  Public functions|            |
| -------------- | -------------- |
|**[Catalog](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_catalog.md#function-catalog)**()|  |
|**[~Catalog](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_catalog.md#function-~catalog)**()|  |
|**[IndexSupport](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_catalog.md#function-indexsupport)**() =0| bool <br>Return whether index is supported or not.  |
|**[GetDatabase](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_catalog.md#function-getdatabase)**(const std::string & db) =0| std::shared_ptr< type::Database > <br>Return database information.  |
|**[GetTable](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_catalog.md#function-gettable)**(const std::string & db, const std::string & table_name) =0| std::shared_ptr< [TableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md) >  |
|**[GetProcedureInfo](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_catalog.md#function-getprocedureinfo)**(const std::string & db, const std::string & sp_name)| std::shared_ptr< hybridse::sdk::ProcedureInfo >  |

## Public Functions

#### Catalog { #function-Catalog }

```cpp
inline Catalog()
```


#### ~Catalog { #function-~Catalog }

```cpp
inline virtual ~Catalog()
```


#### IndexSupport { #function-IndexSupport }

```cpp
virtual bool IndexSupport() =0
```

Return whether index is supported or not. 

**Reimplemented by**: [hybridse::vm::MemCatalog::IndexSupport](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_catalog.md#function-indexsupport)


#### GetDatabase { #function-GetDatabase }

```cpp
virtual std::shared_ptr< type::Database > GetDatabase(
    const std::string & db
) =0
```

Return database information. 

**Reimplemented by**: [hybridse::vm::MemCatalog::GetDatabase](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_catalog.md#function-getdatabase)


#### GetTable { #function-GetTable }

```cpp
virtual std::shared_ptr< TableHandler > GetTable(
    const std::string & db,
    const std::string & table_name
) =0
```


**Reimplemented by**: [hybridse::vm::MemCatalog::GetTable](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_catalog.md#function-gettable)


Return a table handler with given table name 


#### GetProcedureInfo { #function-GetProcedureInfo }

```cpp
inline virtual std::shared_ptr< hybridse::sdk::ProcedureInfo > GetProcedureInfo(
    const std::string & db,
    const std::string & sp_name
)
```


Return ProcedureInfo instance with given database name `db` and procedure name `sp_name`


-------------------------------

Updated on 29 March 2021 at 18:02:27 PDT