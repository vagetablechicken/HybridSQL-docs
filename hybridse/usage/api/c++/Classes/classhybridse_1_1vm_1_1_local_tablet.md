---
title: hybridse::vm::LocalTablet

---
# hybridse::vm::LocalTablet



`#include <engine.h>`

## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[LocalTablet](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_local_tablet.md#function-localtablet)**([hybridse::vm::Engine](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine.md) * engine, std::shared_ptr< [hybridse::vm::CompileInfoCache](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_compile_info_cache.md) > sp_cache)|  |
|**[~LocalTablet](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_local_tablet.md#function-~localtablet)**()|  |
|**[SubQuery](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_local_tablet.md#function-subquery)**(uint32_t task_id, const std::string & db, const std::string & sql, const [Row](hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) & row, const bool is_procedure, const bool is_debug) override| std::shared_ptr< [RowHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md) >  |
|**[SubQuery](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_local_tablet.md#function-subquery)**(uint32_t task_id, const std::string & db, const std::string & sql, const std::set< size_t > & common_column_indices, const std::vector< [Row](hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) > & in_rows, const bool request_is_common, const bool is_procedure, const bool is_debug)| std::shared_ptr< [TableHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md) >  |
|**[GetName](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_local_tablet.md#function-getname)**() const| const std::string & <br>Return the name of tablet.  |

## Inherited members
Inherited from [hybridse::vm::Tablet](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_tablet.md)
| **Inherited public functions** |            |
| -------------- | -------------- |
|**[Tablet](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_tablet.md#function-tablet)**()| |
|**[~Tablet](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_tablet.md#function-~tablet)**()| virtual |


## Public Functions

#### function LocalTablet

```cpp
inline explicit LocalTablet(
    hybridse::vm::Engine * engine,
    std::shared_ptr< hybridse::vm::CompileInfoCache > sp_cache
)
```


#### function ~LocalTablet

```cpp
inline ~LocalTablet()
```


#### function SubQuery

```cpp
virtual std::shared_ptr< RowHandler > SubQuery(
    uint32_t task_id,
    const std::string & db,
    const std::string & sql,
    const Row & row,
    const bool is_procedure,
    const bool is_debug
) override
```


**Reimplements**: [hybridse::vm::Tablet::SubQuery](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_tablet.md#function-subquery)


Return [RowHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md) by calling request-mode query on subtask which is specified by task_id and sql string 


#### function SubQuery

```cpp
virtual std::shared_ptr< TableHandler > SubQuery(
    uint32_t task_id,
    const std::string & db,
    const std::string & sql,
    const std::set< size_t > & common_column_indices,
    const std::vector< Row > & in_rows,
    const bool request_is_common,
    const bool is_procedure,
    const bool is_debug
)
```


**Reimplements**: [hybridse::vm::Tablet::SubQuery](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_tablet.md#function-subquery)


Return [TableHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md) by calling batch-request-mode query on subtask which is specified by task_id and sql 


#### function GetName

```cpp
inline virtual const std::string & GetName() const
```

Return the name of tablet. 

**Reimplements**: [hybridse::vm::Tablet::GetName](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_tablet.md#function-getname)


-------------------------------

Updated on  6 April 2021 at 08:47:46 PDT