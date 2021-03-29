---
title: hybridse::vm::LocalTablet

---

# hybridse::vm::LocalTablet




`#include <engine.h>`

Inherits from [hybridse::vm::Tablet](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_tablet.md)

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[LocalTablet](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_local_tablet.md#function-localtablet)**([hybridse::vm::Engine](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_engine.md) * engine, std::shared_ptr< [hybridse::vm::CompileInfoCache](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_compile_info_cache.md) > sp_cache) |
| | **[~LocalTablet](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_local_tablet.md#function-~localtablet)**() |
| virtual std::shared_ptr< [RowHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_row_handler.md) > | **[SubQuery](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_local_tablet.md#function-subquery)**(uint32_t task_id, const std::string & db, const std::string & sql, const [Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md) & row, const bool is_procedure, const bool is_debug) override |
| virtual std::shared_ptr< [TableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md) > | **[SubQuery](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_local_tablet.md#function-subquery)**(uint32_t task_id, const std::string & db, const std::string & sql, const std::set< size_t > & common_column_indices, const std::vector< [Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md) > & in_rows, const bool request_is_common, const bool is_procedure, const bool is_debug) |
| virtual const std::string & | **[GetName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_local_tablet.md#function-getname)**() const<br>Implemented by subclasses to return the name of tablet.  |

## Additional inherited members

**Public Functions inherited from [hybridse::vm::Tablet](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_tablet.md)**

|                | Name           |
| -------------- | -------------- |
| | **[Tablet](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_tablet.md#function-tablet)**() |
| virtual | **[~Tablet](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_tablet.md#function-~tablet)**() |


## Public Functions Documentation

### function LocalTablet

```cpp
inline explicit LocalTablet(
    hybridse::vm::Engine * engine,
    std::shared_ptr< hybridse::vm::CompileInfoCache > sp_cache
)
```


### function ~LocalTablet

```cpp
inline ~LocalTablet()
```


### function SubQuery

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


**Reimplements**: [hybridse::vm::Tablet::SubQuery](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_tablet.md#function-subquery)


Implemented by subclasses to return [RowHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_row_handler.md) by calling request-mode query on subtask which is specified by task_id and sql string 


### function SubQuery

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


**Reimplements**: [hybridse::vm::Tablet::SubQuery](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_tablet.md#function-subquery)


Implemented by subclassed to return [TableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md) by calling batch-request-mode query on subtask which is specified by task_id and sql 


### function GetName

```cpp
inline virtual const std::string & GetName() const
```

Implemented by subclasses to return the name of tablet. 

**Reimplements**: [hybridse::vm::Tablet::GetName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_tablet.md#function-getname)


-------------------------------

Updated on 29 March 2021 at 10:12:21 PDT