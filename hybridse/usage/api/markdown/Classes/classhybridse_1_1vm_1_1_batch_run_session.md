---
title: hybridse::vm::BatchRunSession

---

# hybridse::vm::BatchRunSession




`#include <engine.h>`

Inherits from [hybridse::vm::RunSession](/Classes/classhybridse_1_1vm_1_1_run_session.md)

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[BatchRunSession](/Classes/classhybridse_1_1vm_1_1_batch_run_session.md#function-batchrunsession)**(bool mini_batch =false) |
| | **[~BatchRunSession](/Classes/classhybridse_1_1vm_1_1_batch_run_session.md#function-~batchrunsession)**() |
| int32_t | **[Run](/Classes/classhybridse_1_1vm_1_1_batch_run_session.md#function-run)**(std::vector< Row > & output, uint64_t limit =0) |
| std::shared_ptr< [TableHandler](/Classes/classhybridse_1_1vm_1_1_table_handler.md) > | **[Run](/Classes/classhybridse_1_1vm_1_1_batch_run_session.md#function-run)**() |

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

### function BatchRunSession

```cpp
inline explicit BatchRunSession(
    bool mini_batch =false
)
```


### function ~BatchRunSession

```cpp
inline ~BatchRunSession()
```


### function Run

```cpp
int32_t Run(
    std::vector< Row > & output,
    uint64_t limit =0
)
```


### function Run

```cpp
std::shared_ptr< TableHandler > Run()
```


-------------------------------

Updated on 28 March 2021 at 19:23:48 PDT