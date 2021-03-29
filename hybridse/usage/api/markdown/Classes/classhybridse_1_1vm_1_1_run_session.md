---
title: hybridse::vm::RunSession

---

# hybridse::vm::RunSession




`#include <engine.h>`

Inherited by [hybridse::vm::BatchRequestRunSession](/Classes/classhybridse_1_1vm_1_1_batch_request_run_session.md), [hybridse::vm::BatchRunSession](/Classes/classhybridse_1_1vm_1_1_batch_run_session.md), [hybridse::vm::RequestRunSession](/Classes/classhybridse_1_1vm_1_1_request_run_session.md)

## Public Functions

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

## Protected Attributes

|                | Name           |
| -------------- | -------------- |
| std::shared_ptr< [hybridse::vm::CompileInfo](/Classes/classhybridse_1_1vm_1_1_compile_info.md) > | **[compile_info_](/Classes/classhybridse_1_1vm_1_1_run_session.md#variable-compile_info_)**  |
| [hybridse::vm::EngineMode](/Namespaces/namespacehybridse_1_1vm.md#enum-enginemode) | **[engine_mode_](/Classes/classhybridse_1_1vm_1_1_run_session.md#variable-engine_mode_)**  |
| bool | **[is_debug_](/Classes/classhybridse_1_1vm_1_1_run_session.md#variable-is_debug_)**  |
| std::string | **[sp_name_](/Classes/classhybridse_1_1vm_1_1_run_session.md#variable-sp_name_)**  |
| friend | **[Engine](/Classes/classhybridse_1_1vm_1_1_run_session.md#variable-engine)**  |

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

Updated on 28 March 2021 at 19:23:48 PDT