---
title: hybridse::vm::BatchRequestRunSession

---

# hybridse::vm::BatchRequestRunSession




`#include <engine.h>`

Inherits from [hybridse::vm::RunSession](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_run_session.md)

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[BatchRequestRunSession](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_batch_request_run_session.md#function-batchrequestrunsession)**() |
| | **[~BatchRequestRunSession](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_batch_request_run_session.md#function-~batchrequestrunsession)**() |
| const Schema & | **[GetRequestSchema](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_batch_request_run_session.md#function-getrequestschema)**() const |
| const std::string & | **[GetRequestName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_batch_request_run_session.md#function-getrequestname)**() const |
| int32_t | **[Run](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_batch_request_run_session.md#function-run)**(const uint32_t id, const std::vector< Row > & request_batch, std::vector< Row > & output) |
| int32_t | **[Run](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_batch_request_run_session.md#function-run)**(const std::vector< Row > & request_batch, std::vector< Row > & output) |
| void | **[AddCommonColumnIdx](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_batch_request_run_session.md#function-addcommoncolumnidx)**(size_t idx) |
| const std::set< size_t > & | **[common_column_indices](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_batch_request_run_session.md#function-common_column_indices)**() const |

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

### function BatchRequestRunSession

```cpp
inline BatchRequestRunSession()
```


### function ~BatchRequestRunSession

```cpp
inline ~BatchRequestRunSession()
```


### function GetRequestSchema

```cpp
inline const Schema & GetRequestSchema() const
```


### function GetRequestName

```cpp
inline const std::string & GetRequestName() const
```


### function Run

```cpp
int32_t Run(
    const uint32_t id,
    const std::vector< Row > & request_batch,
    std::vector< Row > & output
)
```


### function Run

```cpp
int32_t Run(
    const std::vector< Row > & request_batch,
    std::vector< Row > & output
)
```


### function AddCommonColumnIdx

```cpp
inline void AddCommonColumnIdx(
    size_t idx
)
```


### function common_column_indices

```cpp
inline const std::set< size_t > & common_column_indices() const
```


-------------------------------

Updated on 28 March 2021 at 19:41:18 PDT