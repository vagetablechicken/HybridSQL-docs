---
title: hybridse::codec::ColInfo

---
# hybridse::codec::ColInfo



`#include <fe_row_codec.h>`

## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[ColInfo](/hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_col_info.md#function-colinfo)**()|  |
|**[ColInfo](/hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_col_info.md#function-colinfo)**(const std::string & name, ::hybridse::type::Type type, uint32_t idx, uint32_t offset)|  |



| Public attributes|    |
| -------------- | -------------- |
| ::hybridse::type::Type | **[type](/hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_col_info.md#variable-type)**  |
| uint32_t | **[idx](/hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_col_info.md#variable-idx)**  |
| uint32_t | **[offset](/hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_col_info.md#variable-offset)**  |
| std::string | **[name](/hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_col_info.md#variable-name)**  |

## Public Functions

#### ColInfo

```cpp
inline ColInfo()
```


#### ColInfo

```cpp
inline ColInfo(
    const std::string & name,
    ::hybridse::type::Type type,
    uint32_t idx,
    uint32_t offset
)
```


## Public Attributes

### type

```cpp
::hybridse::type::Type type;
```


### idx

```cpp
uint32_t idx;
```


### offset

```cpp
uint32_t offset;
```


### name

```cpp
std::string name;
```


-------------------------------

Updated on 29 March 2021 at 17:34:52 PDT