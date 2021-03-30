---
title: hybridse::codec::RowFormat

---
# hybridse::codec::RowFormat



`#include <fe_row_codec.h>`

## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[RowFormat](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_format.md#function-rowformat)**(const [hybridse::codec::Schema](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1codec.md#typedef-schema) * schema)|  |
|**[~RowFormat](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_format.md#function-~rowformat)**()|  |
|**[GetStringColumnInfo](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_format.md#function-getstringcolumninfo)**(size_t idx, [StringColInfo](/hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_string_col_info.md) * res) const| bool  |
|**[GetColumnInfo](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_format.md#function-getcolumninfo)**(size_t idx) const| const [ColInfo](/hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_col_info.md) *  |

## Public Functions

#### RowFormat { #function-RowFormat }

```cpp
explicit RowFormat(
    const hybridse::codec::Schema * schema
)
```


#### ~RowFormat { #function-~RowFormat }

```cpp
inline virtual ~RowFormat()
```


#### GetStringColumnInfo { #function-GetStringColumnInfo }

```cpp
bool GetStringColumnInfo(
    size_t idx,
    StringColInfo * res
) const
```


#### GetColumnInfo { #function-GetColumnInfo }

```cpp
const ColInfo * GetColumnInfo(
    size_t idx
) const
```


-------------------------------

Updated on 29 March 2021 at 18:02:27 PDT