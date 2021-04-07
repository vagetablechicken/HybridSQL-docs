---
title: hybridse::vm::BatchRunSession
summary: BatchRunSession is a kind of RunSession designed for batch mode query. 

---
# hybridse::vm::BatchRunSession



`#include <engine.h>`

[BatchRunSession]() is a kind of [RunSession]() designed for batch mode query. 
## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[BatchRunSession](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_batch_run_session.md#function-batchrunsession)**(bool mini_batch =false)|  |
|**[~BatchRunSession](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_batch_run_session.md#function-~batchrunsession)**()|  |
|**[Run](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_batch_run_session.md#function-run)**(std::vector< [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) > & output, uint64_t limit =0)| int32_t <br>Query sql in batch mode. Query results will be returned as std::vector<Row> in output.  |
|**[Run](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_batch_run_session.md#function-run)**()| std::shared_ptr< [TableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md) > <br>Query sql in batch mode. Return query result as [TableHandler]() pointer.  |

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

#### function BatchRunSession

```cpp
inline explicit BatchRunSession(
    bool mini_batch =false
)
```


#### function ~BatchRunSession

```cpp
inline ~BatchRunSession()
```


#### function Run

```cpp
int32_t Run(
    std::vector< Row > & output,
    uint64_t limit =0
)
```

Query sql in batch mode. Query results will be returned as std::vector<Row> in output. 

#### function Run

```cpp
std::shared_ptr< TableHandler > Run()
```

Query sql in batch mode. Return query result as [TableHandler]() pointer. 

