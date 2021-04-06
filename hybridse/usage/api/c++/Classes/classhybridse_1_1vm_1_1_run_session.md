---
title: hybridse::vm::RunSession

---
# hybridse::vm::RunSession



`#include <engine.h>`

## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[RunSession](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#function-runsession)**([EngineMode](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-enginemode) engine_mode)|  |
|**[~RunSession](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#function-~runsession)**()|  |
|**[GetSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#function-getschema)**() const| const Schema &  |
|**[GetEncodedSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#function-getencodedschema)**() const| const std::string &  |
|**[GetCompileInfo](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#function-getcompileinfo)**()| std::shared_ptr< [hybridse::vm::CompileInfo](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_compile_info.md) >  |
|**[SetCompileInfo](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#function-setcompileinfo)**(const std::shared_ptr< [hybridse::vm::CompileInfo](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_compile_info.md) > & compile_info)| bool  |
|**[EnableDebug](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#function-enabledebug)**()| void  |
|**[DisableDebug](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#function-disabledebug)**()| void  |
|**[IsDebug](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#function-isdebug)**()| bool  |
|**[SetSpName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#function-setspname)**(const std::string & sp_name)| void  |
|**[engine_mode](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#function-engine_mode)**() const| [EngineMode](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-enginemode)  |



| **Protected attributes** | |
| -------------- | -------------- |
| **[compile_info_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#variable-compile_info_)** | std::shared_ptr< [hybridse::vm::CompileInfo](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_compile_info.md) > |
| **[engine_mode_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#variable-engine_mode_)** | [hybridse::vm::EngineMode](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-enginemode) |
| **[is_debug_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#variable-is_debug_)** | bool |
| **[sp_name_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#variable-sp_name_)** | std::string |
| **[Engine](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md#variable-engine)** | friend |

## Public Functions

#### function RunSession

```cpp
explicit RunSession(
    EngineMode engine_mode
)
```


#### function ~RunSession

```cpp
virtual ~RunSession()
```


#### function GetSchema

```cpp
inline virtual const Schema & GetSchema() const
```


#### function GetEncodedSchema

```cpp
inline virtual const std::string & GetEncodedSchema() const
```


#### function GetCompileInfo

```cpp
inline virtual std::shared_ptr< hybridse::vm::CompileInfo > GetCompileInfo()
```


#### function SetCompileInfo

```cpp
bool SetCompileInfo(
    const std::shared_ptr< hybridse::vm::CompileInfo > & compile_info
)
```


#### function EnableDebug

```cpp
inline void EnableDebug()
```


#### function DisableDebug

```cpp
inline void DisableDebug()
```


#### function IsDebug

```cpp
inline bool IsDebug()
```


#### function SetSpName

```cpp
inline void SetSpName(
    const std::string & sp_name
)
```


#### function engine_mode

```cpp
inline EngineMode engine_mode() const
```


## Protected Attributes

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

Updated on  6 April 2021 at 09:17:26 PDT