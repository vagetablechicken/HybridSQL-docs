---
title: hybridse::vm::CompileInfoCache

---

# hybridse::vm::CompileInfoCache




`#include <engine_context.h>`

## Public Functions

|                | Name           |
| -------------- | -------------- |
| virtual std::shared_ptr< [hybridse::vm::CompileInfo](/Classes/classhybridse_1_1vm_1_1_compile_info.md) > | **[GetRequestInfo](/Classes/classhybridse_1_1vm_1_1_compile_info_cache.md#function-getrequestinfo)**(const std::string & db, const std::string & sp_name, base::Status & status) =0 |
| virtual std::shared_ptr< [hybridse::vm::CompileInfo](/Classes/classhybridse_1_1vm_1_1_compile_info.md) > | **[GetBatchRequestInfo](/Classes/classhybridse_1_1vm_1_1_compile_info_cache.md#function-getbatchrequestinfo)**(const std::string & db, const std::string & sp_name, base::Status & status) =0 |

## Public Functions Documentation

### function GetRequestInfo

```cpp
virtual std::shared_ptr< hybridse::vm::CompileInfo > GetRequestInfo(
    const std::string & db,
    const std::string & sp_name,
    base::Status & status
) =0
```


### function GetBatchRequestInfo

```cpp
virtual std::shared_ptr< hybridse::vm::CompileInfo > GetBatchRequestInfo(
    const std::string & db,
    const std::string & sp_name,
    base::Status & status
) =0
```


-------------------------------

Updated on 28 March 2021 at 19:23:48 PDT