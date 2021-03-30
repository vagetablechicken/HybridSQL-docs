---
title: hybridse::codec::StringColInfo

---
# hybridse::codec::StringColInfo



`#include <fe_row_codec.h>`

## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[StringColInfo](/hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_string_col_info.md#function-stringcolinfo)**()|  |
|**[StringColInfo](/hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_string_col_info.md#function-stringcolinfo)**(const std::string & name, ::hybridse::type::Type type, uint32_t idx, uint32_t offset, uint32_t str_next_offset, uint32_t str_start_offset)|  |



| Public attributes|    |
| -------------- | -------------- |
| uint32_t | **[str_next_offset](/hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_string_col_info.md#variable-str_next_offset)**  |
| uint32_t | **[str_start_offset](/hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_string_col_info.md#variable-str_start_offset)**  |

## Inherited members
Inherited from [hybridse::codec::ColInfo](/hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_col_info.md)
| **Inherited public functions** | Name           |
| -------------- | -------------- |
|**[ColInfo](/hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_col_info.md#function-colinfo)**()|  |
|**[ColInfo](/hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_col_info.md#function-colinfo)**(const std::string & name, ::hybridse::type::Type type, uint32_t idx, uint32_t offset)|  |

**Public Attributes inherited from [hybridse::codec::ColInfo](/hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_col_info.md)**

|                | Name           |
| -------------- | -------------- |
| ::hybridse::type::Type | **[type](/hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_col_info.md#variable-type)**  |
| uint32_t | **[idx](/hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_col_info.md#variable-idx)**  |
| uint32_t | **[offset](/hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_col_info.md#variable-offset)**  |
| std::string | **[name](/hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_col_info.md#variable-name)**  |


## Public Functions

#### StringColInfo

```cpp
inline StringColInfo()
```


#### StringColInfo

```cpp
inline StringColInfo(
    const std::string & name,
    ::hybridse::type::Type type,
    uint32_t idx,
    uint32_t offset,
    uint32_t str_next_offset,
    uint32_t str_start_offset
)
```


## Public Attributes

### str_next_offset

```cpp
uint32_t str_next_offset;
```


### str_start_offset

```cpp
uint32_t str_start_offset;
```


-------------------------------

Updated on 29 March 2021 at 17:34:52 PDT