---
title: hybridse::vm::Tablet

---

# hybridse::vm::Tablet




`#include <catalog.h>`

Inherited by [hybridse::vm::LocalTablet](/Classes/classhybridse_1_1vm_1_1_local_tablet.md)

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[Tablet](/Classes/classhybridse_1_1vm_1_1_tablet.md#function-tablet)**() |
| virtual | **[~Tablet](/Classes/classhybridse_1_1vm_1_1_tablet.md#function-~tablet)**() |
| virtual const std::string & | **[GetName](/Classes/classhybridse_1_1vm_1_1_tablet.md#function-getname)**() const =0 |
| virtual std::shared_ptr< [RowHandler](/Classes/classhybridse_1_1vm_1_1_row_handler.md) > | **[SubQuery](/Classes/classhybridse_1_1vm_1_1_tablet.md#function-subquery)**(uint32_t task_id, const std::string & db, const std::string & sql, const hybridse::codec::Row & row, const bool is_procedure, const bool is_debug) =0 |
| virtual std::shared_ptr< [TableHandler](/Classes/classhybridse_1_1vm_1_1_table_handler.md) > | **[SubQuery](/Classes/classhybridse_1_1vm_1_1_tablet.md#function-subquery)**(uint32_t task_id, const std::string & db, const std::string & sql, const std::set< size_t > & common_column_indices, const std::vector< Row > & in_rows, const bool request_is_common, const bool is_procedure, const bool is_debug) =0 |

## Public Functions Documentation

### function Tablet

```cpp
inline Tablet()
```


### function ~Tablet

```cpp
inline virtual ~Tablet()
```


### function GetName

```cpp
virtual const std::string & GetName() const =0
```


**Reimplemented by**: [hybridse::vm::LocalTablet::GetName](/Classes/classhybridse_1_1vm_1_1_local_tablet.md#function-getname)


### function SubQuery

```cpp
virtual std::shared_ptr< RowHandler > SubQuery(
    uint32_t task_id,
    const std::string & db,
    const std::string & sql,
    const hybridse::codec::Row & row,
    const bool is_procedure,
    const bool is_debug
) =0
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
) =0
```


**Reimplemented by**: [hybridse::vm::LocalTablet::SubQuery](/Classes/classhybridse_1_1vm_1_1_local_tablet.md#function-subquery)


-------------------------------

Updated on 28 March 2021 at 19:23:48 PDT