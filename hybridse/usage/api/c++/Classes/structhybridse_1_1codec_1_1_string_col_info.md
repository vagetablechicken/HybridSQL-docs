---
title: hybridse::codec::StringColInfo

---
# hybridse::codec::StringColInfo



`#include <fe_row_codec.h>`

## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[StringColInfo](hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_string_col_info.md#function-stringcolinfo)**()|  |
|**[StringColInfo](hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_string_col_info.md#function-stringcolinfo)**(const std::string & name, ::hybridse::type::Type type, uint32_t idx, uint32_t offset, uint32_t str_next_offset, uint32_t str_start_offset)|  |



| **Public attributes**|    |
| -------------- | -------------- |
| **[str_next_offset](hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_string_col_info.md#variable-str_next_offset)**| uint32_t  |
| **[str_start_offset](hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_string_col_info.md#variable-str_start_offset)**| uint32_t  |

## Inherited members
Inherited from [hybridse::codec::ColInfo](hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_col_info.md)
| **Inherited public functions** |            |
| -------------- | -------------- |
|**[ColInfo](hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_col_info.md#function-colinfo)**()| |
|**[ColInfo](hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_col_info.md#function-colinfo)**(const std::string & name, ::hybridse::type::Type type, uint32_t idx, uint32_t offset)| |

|**Inherited attributes **| |
| -------------- | -------------- |
| **[type](hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_col_info.md#variable-type)**|::hybridse::type::Type  |
| **[idx](hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_col_info.md#variable-idx)**|uint32_t  |
| **[offset](hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_col_info.md#variable-offset)**|uint32_t  |
| **[name](hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_col_info.md#variable-name)**|std::string  |


## Public Functions

#### function StringColInfo

```cpp
inline StringColInfo()
```


#### function StringColInfo

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

### variable str_next_offset

```cpp
uint32_t str_next_offset;
```


### variable str_start_offset

```cpp
uint32_t str_start_offset;
```


-------------------------------

Updated on  6 April 2021 at 08:47:46 PDT