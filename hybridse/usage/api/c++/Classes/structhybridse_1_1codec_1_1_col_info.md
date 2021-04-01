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
| **[type](/hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_col_info.md#variable-type)**| ::hybridse::type::Type  |
| **[idx](/hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_col_info.md#variable-idx)**| uint32_t  |
| **[offset](/hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_col_info.md#variable-offset)**| uint32_t  |
| **[name](/hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_col_info.md#variable-name)**| std::string  |

## Public Functions

#### function ColInfo

```cpp
inline ColInfo()
```


#### function ColInfo

```cpp
inline ColInfo(
    const std::string & name,
    ::hybridse::type::Type type,
    uint32_t idx,
    uint32_t offset
)
```


## Public Attributes

### variable type

```cpp
::hybridse::type::Type type;
```


### variable idx

```cpp
uint32_t idx;
```


### variable offset

```cpp
uint32_t offset;
```


### variable name

```cpp
std::string name;
```


-------------------------------

Updated on  1 April 2021 at 16:11:23 PDT