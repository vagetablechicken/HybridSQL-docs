---
title: hybridse::vm::MemCatalog

---
# hybridse::vm::MemCatalog



`#include <mem_catalog.h>`

## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[MemCatalog](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_catalog.md#function-memcatalog)**()|  |
|**[~MemCatalog](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_catalog.md#function-~memcatalog)**()|  |
|**[Init](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_catalog.md#function-init)**()| bool  |
|**[GetDatabase](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_catalog.md#function-getdatabase)**(const std::string & db)| std::shared_ptr< type::Database > <br>Return database information.  |
|**[GetTable](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_catalog.md#function-gettable)**(const std::string & db, const std::string & table_name)| std::shared_ptr< [TableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md) >  |
|**[IndexSupport](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_catalog.md#function-indexsupport)**() override| bool <br>Return whether index is supported or not.  |

## Inherited members
Inherited from [hybridse::vm::Catalog](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_catalog.md)
| **Inherited public functions** | Name           |
| -------------- | -------------- |
|**[Catalog](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_catalog.md#function-catalog)**()|  |
|**[~Catalog](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_catalog.md#function-~catalog)**()| virtual  |
|**[GetProcedureInfo](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_catalog.md#function-getprocedureinfo)**(const std::string & db, const std::string & sp_name)| virtual std::shared_ptr< hybridse::sdk::ProcedureInfo >  |


## Public Functions

#### MemCatalog { #function-MemCatalog }

```cpp
MemCatalog()
```


#### ~MemCatalog { #function-~MemCatalog }

```cpp
~MemCatalog()
```


#### Init { #function-Init }

```cpp
bool Init()
```


#### GetDatabase { #function-GetDatabase }

```cpp
inline virtual std::shared_ptr< type::Database > GetDatabase(
    const std::string & db
)
```

Return database information. 

**Reimplements**: [hybridse::vm::Catalog::GetDatabase](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_catalog.md#function-getdatabase)


#### GetTable { #function-GetTable }

```cpp
inline virtual std::shared_ptr< TableHandler > GetTable(
    const std::string & db,
    const std::string & table_name
)
```


**Reimplements**: [hybridse::vm::Catalog::GetTable](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_catalog.md#function-gettable)


Return a table handler with given table name 


#### IndexSupport { #function-IndexSupport }

```cpp
inline virtual bool IndexSupport() override
```

Return whether index is supported or not. 

**Reimplements**: [hybridse::vm::Catalog::IndexSupport](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_catalog.md#function-indexsupport)


-------------------------------

Updated on 29 March 2021 at 18:02:27 PDT