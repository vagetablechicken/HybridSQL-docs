---
title: hybridse::vm::LocalTablet

---

# hybridse::vm::LocalTablet




`#include <engine.h>`

Inherits from [hybridse::vm::Tablet](/Classes/classhybridse_1_1vm_1_1_tablet.md)

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[LocalTablet](/Classes/classhybridse_1_1vm_1_1_local_tablet.md#function-localtablet)**([hybridse::vm::Engine](/Classes/classhybridse_1_1vm_1_1_engine.md) * engine, std::shared_ptr< [hybridse::vm::CompileInfoCache](/Classes/classhybridse_1_1vm_1_1_compile_info_cache.md) > sp_cache) |
| | **[~LocalTablet](/Classes/classhybridse_1_1vm_1_1_local_tablet.md#function-~localtablet)**() |
| std::shared_ptr< [RowHandler](/Classes/classhybridse_1_1vm_1_1_row_handler.md) > | **[SubQuery](/Classes/classhybridse_1_1vm_1_1_local_tablet.md#function-subquery)**(uint32_t task_id, const std::string & db, const std::string & sql, const Row & row, const bool is_procedure, const bool is_debug) override |
| virtual std::shared_ptr< [TableHandler](/Classes/classhybridse_1_1vm_1_1_table_handler.md) > | **[SubQuery](/Classes/classhybridse_1_1vm_1_1_local_tablet.md#function-subquery)**(uint32_t task_id, const std::string & db, const std::string & sql, const std::set< size_t > & common_column_indices, const std::vector< Row > & in_rows, const bool request_is_common, const bool is_procedure, const bool is_debug) |
| virtual const std::string & | **[GetName](/Classes/classhybridse_1_1vm_1_1_local_tablet.md#function-getname)**() const |

## Additional inherited members

**Public Functions inherited from [hybridse::vm::Tablet](/Classes/classhybridse_1_1vm_1_1_tablet.md)**

|                | Name           |
| -------------- | -------------- |
| | **[Tablet](/Classes/classhybridse_1_1vm_1_1_tablet.md#function-tablet)**() |
| virtual | **[~Tablet](/Classes/classhybridse_1_1vm_1_1_tablet.md#function-~tablet)**() |


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
std::shared_ptr< RowHandler > SubQuery(
    uint32_t task_id,
    const std::string & db,
    const std::string & sql,
    const Row & row,
    const bool is_procedure,
    const bool is_debug
) override
```


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


**Reimplements**: [hybridse::vm::Tablet::SubQuery](/Classes/classhybridse_1_1vm_1_1_tablet.md#function-subquery)


### function GetName

```cpp
inline virtual const std::string & GetName() const
```


**Reimplements**: [hybridse::vm::Tablet::GetName](/Classes/classhybridse_1_1vm_1_1_tablet.md#function-getname)


-------------------------------

Updated on 28 March 2021 at 19:23:48 PDT