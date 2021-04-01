---
title: hybridse::vm::RequestRunSession

---
# hybridse::vm::RequestRunSession



`#include <engine.h>`

## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[RequestRunSession](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_request_run_session.md#function-requestrunsession)**()|  |
|**[~RequestRunSession](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_request_run_session.md#function-~requestrunsession)**()|  |
|**[Run](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_request_run_session.md#function-run)**(const [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) & in_row, [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) * output)| int32_t  |
|**[Run](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_request_run_session.md#function-run)**(uint32_t task_id, const [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) & in_row, [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) * output)| int32_t  |
|**[GetRequestSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_request_run_session.md#function-getrequestschema)**() const| const Schema &  |
|**[GetRequestName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_request_run_session.md#function-getrequestname)**() const| const std::string &  |

## Inherited members
Inherited from [hybridse::vm::RunSession](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md)
| **Inherited public functions** | Name           |
| -------------- | -------------- |
|**[RunSession](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#function-runsession)**([EngineMode](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-enginemode) engine_mode)|  |
|**[~RunSession](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#function-~runsession)**()| virtual  |
|**[GetSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#function-getschema)**() const| virtual const Schema &  |
|**[GetEncodedSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#function-getencodedschema)**() const| virtual const std::string &  |
|**[GetCompileInfo](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#function-getcompileinfo)**()| virtual std::shared_ptr< [hybridse::vm::CompileInfo](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_compile_info.md) >  |
|**[SetCompileInfo](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#function-setcompileinfo)**(const std::shared_ptr< [hybridse::vm::CompileInfo](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_compile_info.md) > & compile_info)| bool  |
|**[EnableDebug](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#function-enabledebug)**()| void  |
|**[DisableDebug](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#function-disabledebug)**()| void  |
|**[IsDebug](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#function-isdebug)**()| bool  |
|**[SetSpName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#function-setspname)**(const std::string & sp_name)| void  |
|**[engine_mode](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#function-engine_mode)**() const| [EngineMode](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-enginemode)  |

|**Inherited protected attributes| |
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


#### function Run

```cpp
int32_t Run(
    uint32_t task_id,
    const Row & in_row,
    Row * output
)
```


#### function GetRequestSchema

```cpp
inline virtual const Schema & GetRequestSchema() const
```


#### function GetRequestName

```cpp
inline virtual const std::string & GetRequestName() const
```


-------------------------------

Updated on  1 April 2021 at 16:11:23 PDT