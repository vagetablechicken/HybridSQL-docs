---
title: hybridse::vm::Engine

---
# hybridse::vm::Engine



`#include <engine.h>`

## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[Engine](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine.md#function-engine)**(const std::shared_ptr< [Catalog](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_catalog.md) > & cl, const [EngineOptions](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md) & options)|  |
|**[Engine](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine.md#function-engine)**(const std::shared_ptr< [Catalog](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_catalog.md) > & cl)|  |
|**[~Engine](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine.md#function-~engine)**()|  |
|**[Get](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine.md#function-get)**(const std::string & sql, const std::string & db, [RunSession](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md) & session, base::Status & status)| bool  |
|**[GetDependentTables](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine.md#function-getdependenttables)**(const std::string & sql, const std::string & db, [EngineMode](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-enginemode) engine_mode, std::set< std::string > * tables, base::Status & status)| bool  |
|**[Explain](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine.md#function-explain)**(const std::string & sql, const std::string & db, [EngineMode](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-enginemode) engine_mode, [ExplainOutput](/hybridse/usage/api/c++/Classes/structhybridse_1_1vm_1_1_explain_output.md) * explain_output, base::Status * status)| bool  |
|**[Explain](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine.md#function-explain)**(const std::string & sql, const std::string & db, [EngineMode](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-enginemode) engine_mode, const std::set< size_t > & common_column_indices, [ExplainOutput](/hybridse/usage/api/c++/Classes/structhybridse_1_1vm_1_1_explain_output.md) * explain_output, base::Status * status)| bool  |
|**[UpdateCatalog](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine.md#function-updatecatalog)**(std::shared_ptr< [Catalog](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_catalog.md) > cl)| void  |
|**[ClearCacheLocked](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine.md#function-clearcachelocked)**(const std::string & db)| void  |
|**[InitializeGlobalLLVM](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine.md#function-initializegloballlvm)**()| void  |

## Public Functions

#### function Engine

```cpp
Engine(
    const std::shared_ptr< Catalog > & cl,
    const EngineOptions & options
)
```


#### function Engine

```cpp
explicit Engine(
    const std::shared_ptr< Catalog > & cl
)
```


#### function ~Engine

```cpp
~Engine()
```


#### function Get

```cpp
bool Get(
    const std::string & sql,
    const std::string & db,
    RunSession & session,
    base::Status & status
)
```


#### function GetDependentTables

```cpp
bool GetDependentTables(
    const std::string & sql,
    const std::string & db,
    EngineMode engine_mode,
    std::set< std::string > * tables,
    base::Status & status
)
```


#### function Explain

```cpp
bool Explain(
    const std::string & sql,
    const std::string & db,
    EngineMode engine_mode,
    ExplainOutput * explain_output,
    base::Status * status
)
```


#### function Explain

```cpp
bool Explain(
    const std::string & sql,
    const std::string & db,
    EngineMode engine_mode,
    const std::set< size_t > & common_column_indices,
    ExplainOutput * explain_output,
    base::Status * status
)
```


#### function UpdateCatalog

```cpp
inline void UpdateCatalog(
    std::shared_ptr< Catalog > cl
)
```


#### function ClearCacheLocked

```cpp
void ClearCacheLocked(
    const std::string & db
)
```


#### function InitializeGlobalLLVM

```cpp
static void InitializeGlobalLLVM()
```


-------------------------------

Updated on 29 March 2021 at 18:05:16 PDT