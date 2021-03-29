---
title: hybridse::codec::StringColInfo

---

# hybridse::codec::StringColInfo




`#include <fe_row_codec.h>`

Inherits from [hybridse::codec::ColInfo](/hybridse/usage/api/markdown/Classes/structhybridse_1_1codec_1_1_col_info.md)

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[StringColInfo](/hybridse/usage/api/markdown/Classes/structhybridse_1_1codec_1_1_string_col_info.md#function-stringcolinfo)**() |
| | **[StringColInfo](/hybridse/usage/api/markdown/Classes/structhybridse_1_1codec_1_1_string_col_info.md#function-stringcolinfo)**(const std::string & name, ::hybridse::type::Type type, uint32_t idx, uint32_t offset, uint32_t str_next_offset, uint32_t str_start_offset) |

## Public Attributes

|                | Name           |
| -------------- | -------------- |
| uint32_t | **[str_next_offset](/hybridse/usage/api/markdown/Classes/structhybridse_1_1codec_1_1_string_col_info.md#variable-str_next_offset)**  |
| uint32_t | **[str_start_offset](/hybridse/usage/api/markdown/Classes/structhybridse_1_1codec_1_1_string_col_info.md#variable-str_start_offset)**  |

## Additional inherited members

**Public Functions inherited from [hybridse::codec::ColInfo](/hybridse/usage/api/markdown/Classes/structhybridse_1_1codec_1_1_col_info.md)**

|                | Name           |
| -------------- | -------------- |
| | **[ColInfo](/hybridse/usage/api/markdown/Classes/structhybridse_1_1codec_1_1_col_info.md#function-colinfo)**() |
| | **[ColInfo](/hybridse/usage/api/markdown/Classes/structhybridse_1_1codec_1_1_col_info.md#function-colinfo)**(const std::string & name, ::hybridse::type::Type type, uint32_t idx, uint32_t offset) |

**Public Attributes inherited from [hybridse::codec::ColInfo](/hybridse/usage/api/markdown/Classes/structhybridse_1_1codec_1_1_col_info.md)**

|                | Name           |
| -------------- | -------------- |
| ::hybridse::type::Type | **[type](/hybridse/usage/api/markdown/Classes/structhybridse_1_1codec_1_1_col_info.md#variable-type)**  |
| uint32_t | **[idx](/hybridse/usage/api/markdown/Classes/structhybridse_1_1codec_1_1_col_info.md#variable-idx)**  |
| uint32_t | **[offset](/hybridse/usage/api/markdown/Classes/structhybridse_1_1codec_1_1_col_info.md#variable-offset)**  |
| std::string | **[name](/hybridse/usage/api/markdown/Classes/structhybridse_1_1codec_1_1_col_info.md#variable-name)**  |


## Public Functions Documentation

### function StringColInfo

```cpp
inline StringColInfo()
```


### function StringColInfo

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


## Public Attributes Documentation

### variable str_next_offset

```cpp
uint32_t str_next_offset;
```


### variable str_start_offset

```cpp
uint32_t str_start_offset;
```


-------------------------------

Updated on 29 March 2021 at 10:12:21 PDT