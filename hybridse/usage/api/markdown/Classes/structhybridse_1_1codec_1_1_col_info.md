---
title: hybridse::codec::ColInfo

---

# hybridse::codec::ColInfo




`#include <fe_row_codec.h>`

Inherited by [hybridse::codec::StringColInfo](/hybridse/usage/api/markdown/Classes/structhybridse_1_1codec_1_1_string_col_info.md)

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[ColInfo](/hybridse/usage/api/markdown/Classes/structhybridse_1_1codec_1_1_col_info.md#function-colinfo)**() |
| | **[ColInfo](/hybridse/usage/api/markdown/Classes/structhybridse_1_1codec_1_1_col_info.md#function-colinfo)**(const std::string & name, ::hybridse::type::Type type, uint32_t idx, uint32_t offset) |

## Public Attributes

|                | Name           |
| -------------- | -------------- |
| ::hybridse::type::Type | **[type](/hybridse/usage/api/markdown/Classes/structhybridse_1_1codec_1_1_col_info.md#variable-type)**  |
| uint32_t | **[idx](/hybridse/usage/api/markdown/Classes/structhybridse_1_1codec_1_1_col_info.md#variable-idx)**  |
| uint32_t | **[offset](/hybridse/usage/api/markdown/Classes/structhybridse_1_1codec_1_1_col_info.md#variable-offset)**  |
| std::string | **[name](/hybridse/usage/api/markdown/Classes/structhybridse_1_1codec_1_1_col_info.md#variable-name)**  |

## Public Functions Documentation

### function ColInfo

```cpp
inline ColInfo()
```


### function ColInfo

```cpp
inline ColInfo(
    const std::string & name,
    ::hybridse::type::Type type,
    uint32_t idx,
    uint32_t offset
)
```


## Public Attributes Documentation

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

Updated on 29 March 2021 at 10:12:21 PDT