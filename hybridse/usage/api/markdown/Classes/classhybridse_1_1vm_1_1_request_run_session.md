---
title: hybridse::vm::RequestRunSession

---

# hybridse::vm::RequestRunSession




`#include <engine.h>`

Inherits from [hybridse::vm::RunSession](/Classes/classhybridse_1_1vm_1_1_run_session.md)

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[RequestRunSession](/Classes/classhybridse_1_1vm_1_1_request_run_session.md#function-requestrunsession)**() |
| | **[~RequestRunSession](/Classes/classhybridse_1_1vm_1_1_request_run_session.md#function-~requestrunsession)**() |
| int32_t | **[Run](/Classes/classhybridse_1_1vm_1_1_request_run_session.md#function-run)**(const Row & in_row, Row * output) |
| int32_t | **[Run](/Classes/classhybridse_1_1vm_1_1_request_run_session.md#function-run)**(uint32_t task_id, const Row & in_row, Row * output) |
| virtual const Schema & | **[GetRequestSchema](/Classes/classhybridse_1_1vm_1_1_request_run_session.md#function-getrequestschema)**() const |
| virtual const std::string & | **[GetRequestName](/Classes/classhybridse_1_1vm_1_1_request_run_session.md#function-getrequestname)**() const |

## Additional inherited members

**Public Functions inherited from [hybridse::vm::RunSession](/Classes/classhybridse_1_1vm_1_1_run_session.md)**

|                | Name           |
| -------------- | -------------- |
| | **[RunSession](/Classes/classhybridse_1_1vm_1_1_run_session.md#function-runsession)**([EngineMode](/Namespaces/namespacehybridse_1_1vm.md#enum-enginemode) engine_mode) |
| virtual | **[~RunSession](/Classes/classhybridse_1_1vm_1_1_run_session.md#function-~runsession)**() |
| virtual const Schema & | **[GetSchema](/Classes/classhybridse_1_1vm_1_1_run_session.md#function-getschema)**() const |
| virtual const std::string & | **[GetEncodedSchema](/Classes/classhybridse_1_1vm_1_1_run_session.md#function-getencodedschema)**() const |
| virtual std::shared_ptr< [hybridse::vm::CompileInfo](/Classes/classhybridse_1_1vm_1_1_compile_info.md) > | **[GetCompileInfo](/Classes/classhybridse_1_1vm_1_1_run_session.md#function-getcompileinfo)**() |
| bool | **[SetCompileInfo](/Classes/classhybridse_1_1vm_1_1_run_session.md#function-setcompileinfo)**(const std::shared_ptr< [hybridse::vm::CompileInfo](/Classes/classhybridse_1_1vm_1_1_compile_info.md) > & compile_info) |
| void | **[EnableDebug](/Classes/classhybridse_1_1vm_1_1_run_session.md#function-enabledebug)**() |
| void | **[DisableDebug](/Classes/classhybridse_1_1vm_1_1_run_session.md#function-disabledebug)**() |
| bool | **[IsDebug](/Classes/classhybridse_1_1vm_1_1_run_session.md#function-isdebug)**() |
| void | **[SetSpName](/Classes/classhybridse_1_1vm_1_1_run_session.md#function-setspname)**(const std::string & sp_name) |
| [EngineMode](/Namespaces/namespacehybridse_1_1vm.md#enum-enginemode) | **[engine_mode](/Classes/classhybridse_1_1vm_1_1_run_session.md#function-engine_mode)**() const |

**Protected Attributes inherited from [hybridse::vm::RunSession](/Classes/classhybridse_1_1vm_1_1_run_session.md)**

|                | Name           |
| -------------- | -------------- |
| std::shared_ptr< [hybridse::vm::CompileInfo](/Classes/classhybridse_1_1vm_1_1_compile_info.md) > | **[compile_info_](/Classes/classhybridse_1_1vm_1_1_run_session.md#variable-compile_info_)**  |
| [hybridse::vm::EngineMode](/Namespaces/namespacehybridse_1_1vm.md#enum-enginemode) | **[engine_mode_](/Classes/classhybridse_1_1vm_1_1_run_session.md#variable-engine_mode_)**  |
| bool | **[is_debug_](/Classes/classhybridse_1_1vm_1_1_run_session.md#variable-is_debug_)**  |
| std::string | **[sp_name_](/Classes/classhybridse_1_1vm_1_1_run_session.md#variable-sp_name_)**  |
| friend | **[Engine](/Classes/classhybridse_1_1vm_1_1_run_session.md#variable-engine)**  |


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

Updated on 28 March 2021 at 19:23:48 PDT