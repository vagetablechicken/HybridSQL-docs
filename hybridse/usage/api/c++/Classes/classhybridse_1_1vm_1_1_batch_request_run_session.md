---
title: hybridse::vm::BatchRequestRunSession
summary: BatchRequestRunSession is a kind of RunSession designed for batch request mode query. 

---
# hybridse::vm::BatchRequestRunSession



`#include <engine.h>`

[BatchRequestRunSession]() is a kind of [RunSession]() designed for batch request mode query. 
## Summary

```cpp
class hybridse::vm::BatchRequestRunSession;
```
[BatchRequestRunSession]() is a kind of [RunSession]() designed for batch request mode query. 

BatchRequest-mode query is widely used in OLAD database. It requires a batch of request Rows. 


|  Public functions|            |
| -------------- | -------------- |
|**[BatchRequestRunSession](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_batch_request_run_session.md#function-batchrequestrunsession)**()|  |
|**[~BatchRequestRunSession](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_batch_request_run_session.md#function-~batchrequestrunsession)**()|  |
|**[GetRequestSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_batch_request_run_session.md#function-getrequestschema)**() const| const Schema & <br>Return the schema of request row.  |
|**[GetRequestName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_batch_request_run_session.md#function-getrequestname)**() const| const std::string & <br>Return the name of request row.  |
|**[Run](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_batch_request_run_session.md#function-run)**(const std::vector< [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) > & request_batch, std::vector< [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) > & output)| int32_t <br>Run query in batch request mode.  |
|**[Run](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_batch_request_run_session.md#function-run)**(const uint32_t id, const std::vector< [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) > & request_batch, std::vector< [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) > & output)| int32_t <br>Run a task specified by task_id in request mode.  |
|**[AddCommonColumnIdx](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_batch_request_run_session.md#function-addcommoncolumnidx)**(size_t idx)| void <br>Add common column idx.  |
|**[common_column_indices](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_batch_request_run_session.md#function-common_column_indices)**() const| const std::set< size_t > & <br>Return a set of common column indices.  |

## Inherited members

Inherited from [hybridse::vm::RunSession](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md)

|  Inherited Public functions|            |
| -------------- | -------------- |
|**[RunSession](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#function-runsession)**([EngineMode](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-enginemode) engine_mode)|  |
|**[~RunSession](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#function-~runsession)**()|  |
|**[GetSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#function-getschema)**() const| const Schema & <br>Return query result schema.  |
|**[GetEncodedSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#function-getencodedschema)**() const| const std::string & <br>Return query schema string.  |
|**[GetCompileInfo](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#function-getcompileinfo)**()| std::shared_ptr< [hybridse::vm::CompileInfo](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_compile_info.md) > <br>Return query related compile information.  |
|**[SetCompileInfo](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#function-setcompileinfo)**(const std::shared_ptr< [hybridse::vm::CompileInfo](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_compile_info.md) > & compile_info)| bool <br>Update query related compile information.  |
|**[EnableDebug](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#function-enabledebug)**()| void <br>Enable printing debug information while running a query.  |
|**[DisableDebug](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#function-disabledebug)**()| void <br>Disable printing debug information while running a query.  |
|**[IsDebug](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#function-isdebug)**()| bool <br>Return if this run session support printing debug information.  |
|**[SetSpName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#function-setspname)**(const std::string & sp_name)| void <br>Bind this run session with specific procedure.  |
|**[engine_mode](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#function-engine_mode)**() const| [EngineMode](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-enginemode) <br>Return the engine mode of this run session.  |

|**Inherited protected attributes**| |
| -------------- | -------------- |
| **[compile_info_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#variable-compile_info_)**|std::shared_ptr< [hybridse::vm::CompileInfo](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_compile_info.md) >  |
| **[engine_mode_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#variable-engine_mode_)**|[hybridse::vm::EngineMode](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-enginemode)  |
| **[is_debug_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#variable-is_debug_)**|bool  |
| **[sp_name_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#variable-sp_name_)**|std::string  |
| **[Engine](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#variable-engine)**|friend  |


## Public Functions

#### function BatchRequestRunSession

```cpp
inline BatchRequestRunSession()
```


#### function ~BatchRequestRunSession

```cpp
inline ~BatchRequestRunSession()
```


#### function GetRequestSchema

```cpp
inline const Schema & GetRequestSchema() const
```

Return the schema of request row. 

#### function GetRequestName

```cpp
inline const std::string & GetRequestName() const
```

Return the name of request row. 

#### function Run

```cpp
int32_t Run(
    const std::vector< Row > & request_batch,
    std::vector< Row > & output
)
```

Run query in batch request mode. 

**Parameters**: 

  * **request_batch** a batch of request rows 
  * **output** query results will be returned as std::vector<Row> in output 


**Return**: return 0 if query successfully, otherwise return negative int 

#### function Run

```cpp
int32_t Run(
    const uint32_t id,
    const std::vector< Row > & request_batch,
    std::vector< Row > & output
)
```

Run a task specified by task_id in request mode. 

**Parameters**: 

  * **id** id of task 
  * **request_batch** a batch of request rows 
  * **output** query results will be returned as std::vector<Row> in output 


**Return**: return 0 if query successfully, otherwise return negative int 

#### function AddCommonColumnIdx

```cpp
inline void AddCommonColumnIdx(
    size_t idx
)
```

Add common column idx. 

#### function common_column_indices

```cpp
inline const std::set< size_t > & common_column_indices() const
```

Return a set of common column indices. 

