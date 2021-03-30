---
title: hybridse::vm::CompileInfo

---
# hybridse::vm::CompileInfo



`#include <engine_context.h>`

## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[CompileInfo](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_compile_info.md#function-compileinfo)**()|  |
|**[~CompileInfo](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_compile_info.md#function-~compileinfo)**()|  |
|**[GetIRBuffer](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_compile_info.md#function-getirbuffer)**(const base::RawBuffer & buf) =0| bool  |
|**[GetIRSize](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_compile_info.md#function-getirsize)**() =0| size_t  |
|**[GetEngineMode](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_compile_info.md#function-getenginemode)**() const =0| const [EngineMode](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-enginemode)  |
|**[GetSQL](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_compile_info.md#function-getsql)**() const =0| const std::string &  |
|**[GetSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_compile_info.md#function-getschema)**() const =0| const Schema &  |
|**[GetCompileType](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_compile_info.md#function-getcompiletype)**() const =0| const [ComileType](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-comiletype)  |
|**[GetEncodedSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_compile_info.md#function-getencodedschema)**() const =0| const std::string &  |
|**[GetRequestSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_compile_info.md#function-getrequestschema)**() const =0| const Schema &  |
|**[GetRequestName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_compile_info.md#function-getrequestname)**() const =0| const std::string &  |
|**[GetBatchRequestInfo](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_compile_info.md#function-getbatchrequestinfo)**() const =0| const [hybridse::vm::BatchRequestInfo](/hybridse/usage/api/c++/Classes/structhybridse_1_1vm_1_1_batch_request_info.md) &  |
|**[GetPhysicalPlan](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_compile_info.md#function-getphysicalplan)**() const =0| const hybridse::vm::PhysicalOpNode *  |
|**[DumpPhysicalPlan](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_compile_info.md#function-dumpphysicalplan)**(std::ostream & output, const std::string & tab) =0| void  |
|**[DumpClusterJob](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_compile_info.md#function-dumpclusterjob)**(std::ostream & output, const std::string & tab) =0| void  |

## Public Functions

#### CompileInfo { function CompileInfo }

```cpp
inline CompileInfo()
```


#### ~CompileInfo { function ~CompileInfo }

```cpp
inline virtual ~CompileInfo()
```


#### GetIRBuffer { function GetIRBuffer }

```cpp
virtual bool GetIRBuffer(
    const base::RawBuffer & buf
) =0
```


#### GetIRSize { function GetIRSize }

```cpp
virtual size_t GetIRSize() =0
```


#### GetEngineMode { function GetEngineMode }

```cpp
virtual const EngineMode GetEngineMode() const =0
```


#### GetSQL { function GetSQL }

```cpp
virtual const std::string & GetSQL() const =0
```


#### GetSchema { function GetSchema }

```cpp
virtual const Schema & GetSchema() const =0
```


#### GetCompileType { function GetCompileType }

```cpp
virtual const ComileType GetCompileType() const =0
```


#### GetEncodedSchema { function GetEncodedSchema }

```cpp
virtual const std::string & GetEncodedSchema() const =0
```


#### GetRequestSchema { function GetRequestSchema }

```cpp
virtual const Schema & GetRequestSchema() const =0
```


#### GetRequestName { function GetRequestName }

```cpp
virtual const std::string & GetRequestName() const =0
```


#### GetBatchRequestInfo { function GetBatchRequestInfo }

```cpp
virtual const hybridse::vm::BatchRequestInfo & GetBatchRequestInfo() const =0
```


#### GetPhysicalPlan { function GetPhysicalPlan }

```cpp
virtual const hybridse::vm::PhysicalOpNode * GetPhysicalPlan() const =0
```


#### DumpPhysicalPlan { function DumpPhysicalPlan }

```cpp
virtual void DumpPhysicalPlan(
    std::ostream & output,
    const std::string & tab
) =0
```


#### DumpClusterJob { function DumpClusterJob }

```cpp
virtual void DumpClusterJob(
    std::ostream & output,
    const std::string & tab
) =0
```


-------------------------------

Updated on 29 March 2021 at 17:58:50 PDT