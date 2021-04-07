---
title: hybridse::vm::LocalTablet
summary: Local tablet is responsible to run a task locally. 

---
# hybridse::vm::LocalTablet



`#include <engine.h>`

Local tablet is responsible to run a task locally. 
## Summary

```cpp
class hybridse::vm::LocalTablet;
```
Local tablet is responsible to run a task locally. 

Local tablet won't invoke rpc to run a task remotely. 


|  Public functions|            |
| -------------- | -------------- |
|**[LocalTablet](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_local_tablet.md#function-localtablet)**([hybridse::vm::Engine](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine.md) * engine, std::shared_ptr< [hybridse::vm::CompileInfoCache](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_compile_info_cache.md) > sp_cache)|  |
|**[~LocalTablet](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_local_tablet.md#function-~localtablet)**()|  |
|**[SubQuery](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_local_tablet.md#function-subquery)**(uint32_t task_id, const std::string & db, const std::string & sql, const [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) & row, const bool is_procedure, const bool is_debug) override| std::shared_ptr< [RowHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md) >  |
|**[SubQuery](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_local_tablet.md#function-subquery)**(uint32_t task_id, const std::string & db, const std::string & sql, const std::set< size_t > & common_column_indices, const std::vector< [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) > & in_rows, const bool request_is_common, const bool is_procedure, const bool is_debug)| std::shared_ptr< [TableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md) >  |
|**[GetName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_local_tablet.md#function-getname)**() const| const std::string & <br>Return the name of tablet.  |

## Inherited members

Inherited from [hybridse::vm::Tablet](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_tablet.md)

|  Inherited Public functions|            |
| -------------- | -------------- |
|**[Tablet](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_tablet.md#function-tablet)**()|  |
|**[~Tablet](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_tablet.md#function-~tablet)**()|  |


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


**Parameters**: 

  * **task_id** id of task 
  * **db** name of database 
  * **sql** represents a sql string if `is_procedure` is ture, or represents a procedure name 
  * **row** request row 
  * **is_procedure** whether sql is a procedure or not 
  * **is_debug** whether printing debug information while running 


**Return**: Return query result row as [RowHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md) pointer 

**Reimplements**: [hybridse::vm::Tablet::SubQuery](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_tablet.md#function-subquery)


Run a task in request mode locally 

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


**Parameters**: 

  * **task_id** id of task 
  * **db** name of database 
  * **sql** represents a sql string if `is_procedure` is ture, or represents a procedure name 
  * **common_column_indices** a set of common column indices 
  * **in_rows** a batch of request rows 
  * **request_is_common** whether request is common or not 
  * **is_procedure** whether run procedure or not 
  * **is_debug** whether printing debug information while running 


**Return**: Return query result rows as [TableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md) pointer 

**Reimplements**: [hybridse::vm::Tablet::SubQuery](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_tablet.md#function-subquery)


Run a task in batch-request mode locally 

#### function GetName

```cpp
inline virtual const std::string & GetName() const
```

Return the name of tablet. 

**Reimplements**: [hybridse::vm::Tablet::GetName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_tablet.md#function-getname)


