---
title: hybridse::vm::CompileInfo

---

# hybridse::vm::CompileInfo




`#include <engine_context.h>`

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[CompileInfo](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_compile_info.md#function-compileinfo)**() |
| virtual | **[~CompileInfo](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_compile_info.md#function-~compileinfo)**() |
| virtual bool | **[GetIRBuffer](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_compile_info.md#function-getirbuffer)**(const base::RawBuffer & buf) =0 |
| virtual size_t | **[GetIRSize](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_compile_info.md#function-getirsize)**() =0 |
| virtual const [EngineMode](/hybridse/usage/api/markdownNamespaces/namespacehybridse_1_1vm.md#enum-enginemode) | **[GetEngineMode](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_compile_info.md#function-getenginemode)**() const =0 |
| virtual const std::string & | **[GetSQL](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_compile_info.md#function-getsql)**() const =0 |
| virtual const Schema & | **[GetSchema](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_compile_info.md#function-getschema)**() const =0 |
| virtual const [ComileType](/hybridse/usage/api/markdownNamespaces/namespacehybridse_1_1vm.md#enum-comiletype) | **[GetCompileType](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_compile_info.md#function-getcompiletype)**() const =0 |
| virtual const std::string & | **[GetEncodedSchema](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_compile_info.md#function-getencodedschema)**() const =0 |
| virtual const Schema & | **[GetRequestSchema](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_compile_info.md#function-getrequestschema)**() const =0 |
| virtual const std::string & | **[GetRequestName](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_compile_info.md#function-getrequestname)**() const =0 |
| virtual const [hybridse::vm::BatchRequestInfo](/hybridse/usage/api/markdownClasses/structhybridse_1_1vm_1_1_batch_request_info.md) & | **[GetBatchRequestInfo](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_compile_info.md#function-getbatchrequestinfo)**() const =0 |
| virtual const hybridse::vm::PhysicalOpNode * | **[GetPhysicalPlan](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_compile_info.md#function-getphysicalplan)**() const =0 |
| virtual void | **[DumpPhysicalPlan](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_compile_info.md#function-dumpphysicalplan)**(std::ostream & output, const std::string & tab) =0 |
| virtual void | **[DumpClusterJob](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_compile_info.md#function-dumpclusterjob)**(std::ostream & output, const std::string & tab) =0 |

## Public Functions Documentation

### function CompileInfo

```cpp
inline CompileInfo()
```


### function ~CompileInfo

```cpp
inline virtual ~CompileInfo()
```


### function GetIRBuffer

```cpp
virtual bool GetIRBuffer(
    const base::RawBuffer & buf
) =0
```


### function GetIRSize

```cpp
virtual size_t GetIRSize() =0
```


### function GetEngineMode

```cpp
virtual const EngineMode GetEngineMode() const =0
```


### function GetSQL

```cpp
virtual const std::string & GetSQL() const =0
```


### function GetSchema

```cpp
virtual const Schema & GetSchema() const =0
```


### function GetCompileType

```cpp
virtual const ComileType GetCompileType() const =0
```


### function GetEncodedSchema

```cpp
virtual const std::string & GetEncodedSchema() const =0
```


### function GetRequestSchema

```cpp
virtual const Schema & GetRequestSchema() const =0
```


### function GetRequestName

```cpp
virtual const std::string & GetRequestName() const =0
```


### function GetBatchRequestInfo

```cpp
virtual const hybridse::vm::BatchRequestInfo & GetBatchRequestInfo() const =0
```


### function GetPhysicalPlan

```cpp
virtual const hybridse::vm::PhysicalOpNode * GetPhysicalPlan() const =0
```


### function DumpPhysicalPlan

```cpp
virtual void DumpPhysicalPlan(
    std::ostream & output,
    const std::string & tab
) =0
```


### function DumpClusterJob

```cpp
virtual void DumpClusterJob(
    std::ostream & output,
    const std::string & tab
) =0
```


-------------------------------

Updated on 28 March 2021 at 19:34:48 PDT