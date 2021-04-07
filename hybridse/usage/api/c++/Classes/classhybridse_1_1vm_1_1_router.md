---
title: hybridse::vm::Router

---
# hybridse::vm::Router



`#include <router.h>`

## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[SetMainTable](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_router.md#function-setmaintable)**(const std::string & main_table)| void  |
|**[GetMainTable](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_router.md#function-getmaintable)**() const| const std::string &  |
|**[Parse](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_router.md#function-parse)**(const PhysicalOpNode * physical_plan)| int  |
|**[GetRouterCol](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_router.md#function-getroutercol)**() const| const std::string &  |

## Public Functions

#### function SetMainTable

```cpp
inline void SetMainTable(
    const std::string & main_table
)
```


#### function GetMainTable

```cpp
inline const std::string & GetMainTable() const
```


#### function Parse

```cpp
int Parse(
    const PhysicalOpNode * physical_plan
)
```


#### function GetRouterCol

```cpp
inline const std::string & GetRouterCol() const
```


