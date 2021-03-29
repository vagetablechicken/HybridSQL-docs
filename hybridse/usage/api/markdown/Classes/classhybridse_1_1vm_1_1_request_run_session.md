---
title: hybridse::vm::RequestRunSession

---

# hybridse::vm::RequestRunSession




`#include <engine.h>`

Inherits from [hybridse::vm::RunSession](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_run_session.md)

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[RequestRunSession](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_request_run_session.md#function-requestrunsession)**() |
| | **[~RequestRunSession](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_request_run_session.md#function-~requestrunsession)**() |
| int32_t | **[Run](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_request_run_session.md#function-run)**(const [Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md) & in_row, [Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md) * output) |
| int32_t | **[Run](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_request_run_session.md#function-run)**(uint32_t task_id, const [Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md) & in_row, [Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md) * output) |
| virtual const Schema & | **[GetRequestSchema](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_request_run_session.md#function-getrequestschema)**() const |
| virtual const std::string & | **[GetRequestName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_request_run_session.md#function-getrequestname)**() const |

## Additional inherited members

**Public Functions inherited from [hybridse::vm::RunSession](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_run_session.md)**

|                | Name           |
| -------------- | -------------- |
| | **[RunSession](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_run_session.md#function-runsession)**([EngineMode](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#enum-enginemode) engine_mode) |
| virtual | **[~RunSession](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_run_session.md#function-~runsession)**() |
| virtual const Schema & | **[GetSchema](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_run_session.md#function-getschema)**() const |
| virtual const std::string & | **[GetEncodedSchema](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_run_session.md#function-getencodedschema)**() const |
| virtual std::shared_ptr< [hybridse::vm::CompileInfo](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_compile_info.md) > | **[GetCompileInfo](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_run_session.md#function-getcompileinfo)**() |
| bool | **[SetCompileInfo](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_run_session.md#function-setcompileinfo)**(const std::shared_ptr< [hybridse::vm::CompileInfo](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_compile_info.md) > & compile_info) |
| void | **[EnableDebug](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_run_session.md#function-enabledebug)**() |
| void | **[DisableDebug](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_run_session.md#function-disabledebug)**() |
| bool | **[IsDebug](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_run_session.md#function-isdebug)**() |
| void | **[SetSpName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_run_session.md#function-setspname)**(const std::string & sp_name) |
| [EngineMode](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#enum-enginemode) | **[engine_mode](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_run_session.md#function-engine_mode)**() const |

**Protected Attributes inherited from [hybridse::vm::RunSession](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_run_session.md)**

|                | Name           |
| -------------- | -------------- |
| std::shared_ptr< [hybridse::vm::CompileInfo](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_compile_info.md) > | **[compile_info_](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_run_session.md#variable-compile_info_)**  |
| [hybridse::vm::EngineMode](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#enum-enginemode) | **[engine_mode_](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_run_session.md#variable-engine_mode_)**  |
| bool | **[is_debug_](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_run_session.md#variable-is_debug_)**  |
| std::string | **[sp_name_](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_run_session.md#variable-sp_name_)**  |
| friend | **[Engine](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_run_session.md#variable-engine)**  |


## Public Functions Documentation

### function RequestRunSession

```cpp
inline RequestRunSession()
```


### function ~RequestRunSession

```cpp
inline ~RequestRunSession()
```


### function Run

```cpp
int32_t Run(
    const Row & in_row,
    Row * output
)
```


### function Run

```cpp
int32_t Run(
    uint32_t task_id,
    const Row & in_row,
    Row * output
)
```


### function GetRequestSchema

```cpp
inline virtual const Schema & GetRequestSchema() const
```


### function GetRequestName

```cpp
inline virtual const std::string & GetRequestName() const
```


-------------------------------

Updated on 29 March 2021 at 10:12:21 PDT