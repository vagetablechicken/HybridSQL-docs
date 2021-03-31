---
title: hybridse::vm::CompileInfoCache

---
# hybridse::vm::CompileInfoCache



`#include <engine_context.h>`

## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[GetRequestInfo](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_compile_info_cache.md#function-getrequestinfo)**(const std::string & db, const std::string & sp_name, base::Status & status) =0| std::shared_ptr< [hybridse::vm::CompileInfo](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_compile_info.md) >  |
|**[GetBatchRequestInfo](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_compile_info_cache.md#function-getbatchrequestinfo)**(const std::string & db, const std::string & sp_name, base::Status & status) =0| std::shared_ptr< [hybridse::vm::CompileInfo](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_compile_info.md) >  |

## Public Functions

#### function GetRequestInfo

```cpp
virtual std::shared_ptr< hybridse::vm::CompileInfo > GetRequestInfo(
    const std::string & db,
    const std::string & sp_name,
    base::Status & status
) =0
```


#### function GetBatchRequestInfo

```cpp
virtual std::shared_ptr< hybridse::vm::CompileInfo > GetBatchRequestInfo(
    const std::string & db,
    const std::string & sp_name,
    base::Status & status
) =0
```


-------------------------------

Updated on 29 March 2021 at 19:04:07 PDT