---
title: hybridse::vm::Engine
summary: An engine is responsible to compile SQL on the specific Catalog. 

---
# hybridse::vm::Engine



`#include <engine.h>`

An engine is responsible to compile SQL on the specific [Catalog](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_catalog.md). 
## Summary

```cpp
class hybridse::vm::Engine;
```
An engine is responsible to compile SQL on the specific [Catalog](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_catalog.md). 

An engine can be used to `compile sql and explain the compiling result. It maintains a LRU cache for compiling result.

**Example**

```cpp
// Assuming the catalog has been created and initialized before
base::Status status;
EngineOptions options;
Engine engine(catalog, options);
BatchRunSession session;
std::db = "test_db";
std::string sql = "select col0, col1, col2, col1+col2 as col12 from t1;";
engine.Get(sql, db, session, status);
engine.Explain(sql, db, EngineMode::kBatchMode, &output, &status);
```


|  Public functions|            |
| -------------- | -------------- |
|**[Engine](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine.md#function-engine)**(const std::shared_ptr< [Catalog](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_catalog.md) > & cl)| <br>Create an [Engine](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine.md) with a specific [Catalog](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_catalog.md) object.  |
|**[Engine](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine.md#function-engine)**(const std::shared_ptr< [Catalog](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_catalog.md) > & cl, const [EngineOptions](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md) & options)| <br>Create an [Engine](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine.md) a specific [Catalog](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_catalog.md) object, configuring it with [EngineOptions]().  |
|**[~Engine](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine.md#function-~engine)**()|  |
|**[Get](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine.md#function-get)**(const std::string & sql, const std::string & db, [RunSession](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md) & session, base::Status & status)| bool <br>Compile sql in db and stored the results in the session.  |
|**[GetDependentTables](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine.md#function-getdependenttables)**(const std::string & sql, const std::string & db, [EngineMode](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-enginemode) engine_mode, std::set< std::string > * tables, base::Status & status)| bool <br>Search all tables related to the specific sql in db.  |
|**[Explain](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine.md#function-explain)**(const std::string & sql, const std::string & db, [EngineMode](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-enginemode) engine_mode, [ExplainOutput](/hybridse/usage/api/c++/Classes/structhybridse_1_1vm_1_1_explain_output.md) * explain_output, base::Status * status)| bool <br>Explain sql compiling result.  |
|**[Explain](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine.md#function-explain)**(const std::string & sql, const std::string & db, [EngineMode](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-enginemode) engine_mode, const std::set< size_t > & common_column_indices, [ExplainOutput](/hybridse/usage/api/c++/Classes/structhybridse_1_1vm_1_1_explain_output.md) * explain_output, base::Status * status)| bool <br>Same as above, but allowing compiling with configuring common column indices.  |
|**[UpdateCatalog](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine.md#function-updatecatalog)**(std::shared_ptr< [Catalog](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_catalog.md) > cl)| void <br>Update engine's catalog.  |
|**[ClearCacheLocked](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine.md#function-clearcachelocked)**(const std::string & db)| void <br>Clear engine's compiling result cache.  |
|**[InitializeGlobalLLVM](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine.md#function-initializegloballlvm)**()| void <br>Initialize LLVM environments.  |

## Public Functions

#### function Engine

```cpp
explicit Engine(
    const std::shared_ptr< Catalog > & cl
)
```

Create an [Engine](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine.md) with a specific [Catalog](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_catalog.md) object. 

#### function Engine

```cpp
Engine(
    const std::shared_ptr< Catalog > & cl,
    const EngineOptions & options
)
```

Create an [Engine](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine.md) a specific [Catalog](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_catalog.md) object, configuring it with [EngineOptions](). 

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

Compile sql in db and stored the results in the session. 

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

Search all tables related to the specific sql in db. 

The tables' names are returned in tables 

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

Explain sql compiling result. 

The results are returned as [ExplainOutput](/hybridse/usage/api/c++/Classes/structhybridse_1_1vm_1_1_explain_output.md) in explain_output. The success or fail status message is returned as Status in status. TODO: base::Status* status -> base::Status& status 

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

Same as above, but allowing compiling with configuring common column indices. 

The common column indices are used for common column optimization under EngineMode::kBatchRequestMode 

#### function UpdateCatalog

```cpp
inline void UpdateCatalog(
    std::shared_ptr< Catalog > cl
)
```

Update engine's catalog. 

#### function ClearCacheLocked

```cpp
void ClearCacheLocked(
    const std::string & db
)
```

Clear engine's compiling result cache. 

#### function InitializeGlobalLLVM

```cpp
static void InitializeGlobalLLVM()
```

Initialize LLVM environments. 

