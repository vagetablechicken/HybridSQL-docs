---
title: hybridse::vm::Tablet
summary: A component responsible to Query subtask. 

---
# hybridse::vm::Tablet



`#include <catalog.h>`

A component responsible to Query subtask. 
## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[Tablet](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_tablet.md#function-tablet)**()|  |
|**[~Tablet](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_tablet.md#function-~tablet)**()|  |
|**[GetName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_tablet.md#function-getname)**() const =0| const std::string & <br>Return the name of tablet.  |
|**[SubQuery](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_tablet.md#function-subquery)**(uint32_t task_id, const std::string & db, const std::string & sql, const [hybridse::codec::Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) & row, const bool is_procedure, const bool is_debug) =0| std::shared_ptr< [RowHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md) >  |
|**[SubQuery](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_tablet.md#function-subquery)**(uint32_t task_id, const std::string & db, const std::string & sql, const std::set< size_t > & common_column_indices, const std::vector< [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) > & in_rows, const bool request_is_common, const bool is_procedure, const bool is_debug) =0| std::shared_ptr< [TableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md) >  |

## Public Functions

#### function Tablet

```cpp
inline Tablet()
```


#### function ~Tablet

```cpp
inline virtual ~Tablet()
```


#### function GetName

```cpp
virtual const std::string & GetName() const =0
```

Return the name of tablet. 

**Reimplemented by**: [hybridse::vm::LocalTablet::GetName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_local_tablet.md#function-getname)


#### function SubQuery

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


**Reimplemented by**: [hybridse::vm::LocalTablet::SubQuery](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_local_tablet.md#function-subquery)


Return [RowHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md) by calling request-mode query on subtask which is specified by task_id and sql string 


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
) =0
```


**Reimplemented by**: [hybridse::vm::LocalTablet::SubQuery](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_local_tablet.md#function-subquery)


Return [TableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md) by calling batch-request-mode query on subtask which is specified by task_id and sql 


-------------------------------

Updated on 29 March 2021 at 18:05:16 PDT