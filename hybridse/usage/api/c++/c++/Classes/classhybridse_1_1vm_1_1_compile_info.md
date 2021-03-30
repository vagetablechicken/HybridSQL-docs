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

#### function CompileInfo

```cpp
inline CompileInfo()
```


#### function ~CompileInfo

```cpp
inline virtual ~CompileInfo()
```


#### function GetIRBuffer

```cpp
virtual bool GetIRBuffer(
    const base::RawBuffer & buf
) =0
```


#### function GetIRSize

```cpp
virtual size_t GetIRSize() =0
```


#### function GetEngineMode

```cpp
virtual const EngineMode GetEngineMode() const =0
```


#### function GetSQL

```cpp
virtual const std::string & GetSQL() const =0
```


#### function GetSchema

```cpp
virtual const Schema & GetSchema() const =0
```


#### function GetCompileType

```cpp
virtual const ComileType GetCompileType() const =0
```


#### function GetEncodedSchema

```cpp
virtual const std::string & GetEncodedSchema() const =0
```


#### function GetRequestSchema

```cpp
virtual const Schema & GetRequestSchema() const =0
```


#### function GetRequestName

```cpp
virtual const std::string & GetRequestName() const =0
```


#### function GetBatchRequestInfo

```cpp
virtual const hybridse::vm::BatchRequestInfo & GetBatchRequestInfo() const =0
```


#### function GetPhysicalPlan

```cpp
virtual const hybridse::vm::PhysicalOpNode * GetPhysicalPlan() const =0
```


#### function DumpPhysicalPlan

```cpp
virtual void DumpPhysicalPlan(
    std::ostream & output,
    const std::string & tab
) =0
```


#### function DumpClusterJob

```cpp
virtual void DumpClusterJob(
    std::ostream & output,
    const std::string & tab
) =0
```


-------------------------------

Updated on 29 March 2021 at 19:04:07 PDT