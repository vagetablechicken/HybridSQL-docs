---
title: hybridse::vm::RunSession

---

# hybridse::vm::RunSession




`#include <engine.h>`

Inherited by [hybridse::vm::BatchRequestRunSession](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_batch_request_run_session.md), [hybridse::vm::BatchRunSession](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_batch_run_session.md), [hybridse::vm::RequestRunSession](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_request_run_session.md)

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[RunSession](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_run_session.md#function-runsession)**([EngineMode](/hybridse/usage/api/markdownNamespaces/namespacehybridse_1_1vm.md#enum-enginemode) engine_mode) |
| virtual | **[~RunSession](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_run_session.md#function-~runsession)**() |
| virtual const Schema & | **[GetSchema](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_run_session.md#function-getschema)**() const |
| virtual const std::string & | **[GetEncodedSchema](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_run_session.md#function-getencodedschema)**() const |
| virtual std::shared_ptr< [hybridse::vm::CompileInfo](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_compile_info.md) > | **[GetCompileInfo](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_run_session.md#function-getcompileinfo)**() |
| bool | **[SetCompileInfo](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_run_session.md#function-setcompileinfo)**(const std::shared_ptr< [hybridse::vm::CompileInfo](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_compile_info.md) > & compile_info) |
| void | **[EnableDebug](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_run_session.md#function-enabledebug)**() |
| void | **[DisableDebug](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_run_session.md#function-disabledebug)**() |
| bool | **[IsDebug](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_run_session.md#function-isdebug)**() |
| void | **[SetSpName](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_run_session.md#function-setspname)**(const std::string & sp_name) |
| [EngineMode](/hybridse/usage/api/markdownNamespaces/namespacehybridse_1_1vm.md#enum-enginemode) | **[engine_mode](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_run_session.md#function-engine_mode)**() const |

## Protected Attributes

|                | Name           |
| -------------- | -------------- |
| std::shared_ptr< [hybridse::vm::CompileInfo](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_compile_info.md) > | **[compile_info_](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_run_session.md#variable-compile_info_)**  |
| [hybridse::vm::EngineMode](/hybridse/usage/api/markdownNamespaces/namespacehybridse_1_1vm.md#enum-enginemode) | **[engine_mode_](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_run_session.md#variable-engine_mode_)**  |
| bool | **[is_debug_](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_run_session.md#variable-is_debug_)**  |
| std::string | **[sp_name_](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_run_session.md#variable-sp_name_)**  |
| friend | **[Engine](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_run_session.md#variable-engine)**  |

## Public Functions Documentation

### function RunSession

```cpp
explicit RunSession(
    EngineMode engine_mode
)
```


### function ~RunSession

```cpp
virtual ~RunSession()
```


### function GetSchema

```cpp
inline virtual const Schema & GetSchema() const
```


### function GetEncodedSchema

```cpp
inline virtual const std::string & GetEncodedSchema() const
```


### function GetCompileInfo

```cpp
inline virtual std::shared_ptr< hybridse::vm::CompileInfo > GetCompileInfo()
```


### function SetCompileInfo

```cpp
bool SetCompileInfo(
    const std::shared_ptr< hybridse::vm::CompileInfo > & compile_info
)
```


### function EnableDebug

```cpp
inline void EnableDebug()
```


### function DisableDebug

```cpp
inline void DisableDebug()
```


### function IsDebug

```cpp
inline bool IsDebug()
```


### function SetSpName

```cpp
inline void SetSpName(
    const std::string & sp_name
)
```


### function engine_mode

```cpp
inline EngineMode engine_mode() const
```


## Protected Attributes Documentation

### variable compile_info_

```cpp
std::shared_ptr< hybridse::vm::CompileInfo > compile_info_;
```


### variable engine_mode_

```cpp
hybridse::vm::EngineMode engine_mode_;
```


### variable is_debug_

```cpp
bool is_debug_;
```


### variable sp_name_

```cpp
std::string sp_name_;
```


### variable Engine

```cpp
friend Engine;
```


-------------------------------

Updated on 28 March 2021 at 19:34:49 PDT