---
title: hybridse::vm::RunSession
summary: A RunSession maintain SQL running context, including compile information, procedure name. 

---
# hybridse::vm::RunSession



`#include <engine.h>`

A [RunSession]() maintain SQL running context, including compile information, procedure name. 
## Summary


|  Public functions|            |
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

Return query result schema. 

#### function GetEncodedSchema

```cpp
inline virtual const std::string & GetEncodedSchema() const
```

Return query schema string. 

#### function GetCompileInfo

```cpp
inline virtual std::shared_ptr< hybridse::vm::CompileInfo > GetCompileInfo()
```

Return query related compile information. 

#### function SetCompileInfo

```cpp
bool SetCompileInfo(
    const std::shared_ptr< hybridse::vm::CompileInfo > & compile_info
)
```

Update query related compile information. 

#### function EnableDebug

```cpp
inline void EnableDebug()
```

Enable printing debug information while running a query. 

#### function DisableDebug

```cpp
inline void DisableDebug()
```

Disable printing debug information while running a query. 

#### function IsDebug

```cpp
inline bool IsDebug()
```

Return if this run session support printing debug information. 

#### function SetSpName

```cpp
inline void SetSpName(
    const std::string & sp_name
)
```

Bind this run session with specific procedure. 

#### function engine_mode

```cpp
inline EngineMode engine_mode() const
```

Return the engine mode of this run session. 

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


