---
title: hybridse::vm::RequestRunSession
summary: RequestRunSession is a kind of RunSession designed for request mode query. 

---
# hybridse::vm::RequestRunSession



`#include <engine.h>`

[RequestRunSession]() is a kind of [RunSession]() designed for request mode query. 
## Summary

```cpp
class hybridse::vm::RequestRunSession;
```
[RequestRunSession]() is a kind of [RunSession]() designed for request mode query. 

Request-mode query is widely used in OLAD database. It requires a request Row. 


|  Public functions|            |
| -------------- | -------------- |
|**[RequestRunSession](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_request_run_session.md#function-requestrunsession)**()|  |
|**[~RequestRunSession](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_request_run_session.md#function-~requestrunsession)**()|  |
|**[Run](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_request_run_session.md#function-run)**(const [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) & in_row, [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) * output)| int32_t <br>Query sql in request mode.  |
|**[Run](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_request_run_session.md#function-run)**(uint32_t task_id, const [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) & in_row, [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) * output)| int32_t <br>Run a task specified by task_id in request mode.  |
|**[GetRequestSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_request_run_session.md#function-getrequestschema)**() const| const Schema & <br>Return the schema of request row.  |
|**[GetRequestName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_request_run_session.md#function-getrequestname)**() const| const std::string & <br>Return the name of request row.  |

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

#### function RequestRunSession

```cpp
inline RequestRunSession()
```


#### function ~RequestRunSession

```cpp
inline ~RequestRunSession()
```


#### function Run

```cpp
int32_t Run(
    const Row & in_row,
    Row * output
)
```

Query sql in request mode. 

**Parameters**: 

  * **in_row** request row 
  * **output** query result will be returned as Row in output 


**Return**: return 0 if query successfully, otherwise return negative int 

#### function Run

```cpp
int32_t Run(
    uint32_t task_id,
    const Row & in_row,
    Row * output
)
```

Run a task specified by task_id in request mode. 

**Parameters**: 

  * **task_id** task id of task 
  * **in_row** request row 
  * **output** query result will be returned as Row in output 


**Return**: return 0 if query successfully, otherwise return negative int 

#### function GetRequestSchema

```cpp
inline virtual const Schema & GetRequestSchema() const
```

Return the schema of request row. 

#### function GetRequestName

```cpp
inline virtual const std::string & GetRequestName() const
```

Return the name of request row. 

-------------------------------

Updated on  6 April 2021 at 19:38:01 PDT