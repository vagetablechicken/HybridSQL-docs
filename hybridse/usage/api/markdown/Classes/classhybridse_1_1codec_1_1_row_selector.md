---
title: hybridse::codec::RowSelector

---

# hybridse::codec::RowSelector




`#include <fe_row_selector.h>`

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[RowSelector](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row_selector.md#function-rowselector)**(const [hybridse::codec::Schema](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1codec.md#typedef-schema) * schema, const std::vector< size_t > & indices) |
| | **[RowSelector](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row_selector.md#function-rowselector)**(const std::vector< const [hybridse::codec::Schema](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1codec.md#typedef-schema) * > & schemas, const std::vector< std::pair< size_t, size_t >> & indices) |
| bool | **[Select](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row_selector.md#function-select)**(const int8_t * slice, size_t size, int8_t ** out_slice, size_t * out_size) |
| bool | **[Select](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row_selector.md#function-select)**(const [Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md) & row, int8_t ** out_slice, size_t * out_size) |

## Public Functions Documentation

### function RowSelector

```cpp
RowSelector(
    const hybridse::codec::Schema * schema,
    const std::vector< size_t > & indices
)
```


### function RowSelector

```cpp
RowSelector(
    const std::vector< const hybridse::codec::Schema * > & schemas,
    const std::vector< std::pair< size_t, size_t >> & indices
)
```


### function Select

```cpp
bool Select(
    const int8_t * slice,
    size_t size,
    int8_t ** out_slice,
    size_t * out_size
)
```


### function Select

```cpp
bool Select(
    const Row & row,
    int8_t ** out_slice,
    size_t * out_size
)
```


-------------------------------

Updated on 29 March 2021 at 10:12:21 PDT