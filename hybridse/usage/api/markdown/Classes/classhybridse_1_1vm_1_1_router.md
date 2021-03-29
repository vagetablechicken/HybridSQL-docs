---
title: hybridse::vm::Router

---

# hybridse::vm::Router




`#include <router.h>`

## Public Functions

|                | Name           |
| -------------- | -------------- |
| void | **[SetMainTable](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_router.md#function-setmaintable)**(const std::string & main_table) |
| const std::string & | **[GetMainTable](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_router.md#function-getmaintable)**() const |
| int | **[Parse](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_router.md#function-parse)**(const PhysicalOpNode * physical_plan) |
| const std::string & | **[GetRouterCol](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_router.md#function-getroutercol)**() const |

## Public Functions Documentation

### function SetMainTable

```cpp
inline void SetMainTable(
    const std::string & main_table
)
```


### function GetMainTable

```cpp
inline const std::string & GetMainTable() const
```


### function Parse

```cpp
int Parse(
    const PhysicalOpNode * physical_plan
)
```


### function GetRouterCol

```cpp
inline const std::string & GetRouterCol() const
```


-------------------------------

Updated on 28 March 2021 at 19:41:19 PDT