---
title: hybridse::codec::Row

---

# hybridse::codec::Row




`#include <row.h>`

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md#function-row)**() |
| | **[Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md#function-row)**(const std::string & str) |
| | **[Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md#function-row)**(const [Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md) & s) |
| | **[Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md#function-row)**(size_t major_slices, const [Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md) & major, size_t secondary_slices, const [Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md) & secondary) |
| | **[Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md#function-row)**(const hybridse::base::RefCountedSlice & s, size_t secondary_slices, const [Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md) & secondary) |
| | **[Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md#function-row)**(const hybridse::base::RefCountedSlice & s) |
| virtual | **[~Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md#function-~row)**() |
| int8_t * | **[buf](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md#function-buf)**() const |
| int8_t * | **[buf](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md#function-buf)**(int32_t pos) const |
| int32_t | **[size](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md#function-size)**() const |
| int32_t | **[size](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md#function-size)**(int32_t pos) const |
| bool | **[empty](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md#function-empty)**() const |
| int | **[compare](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md#function-compare)**(const [Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md) & b) const |
| int8_t ** | **[GetRowPtrs](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md#function-getrowptrs)**() const |
| int32_t | **[GetRowPtrCnt](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md#function-getrowptrcnt)**() const |
| int32_t * | **[GetRowSizes](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md#function-getrowsizes)**() const |
| hybridse::base::RefCountedSlice | **[GetSlice](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md#function-getslice)**(uint32_t slice_index) const |
| void | **[Append](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md#function-append)**(const hybridse::base::RefCountedSlice & slice) |
| std::string | **[ToString](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md#function-tostring)**() const |
| void | **[Reset](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md#function-reset)**(const int8_t * buf, size_t size) |

## Public Functions Documentation

### function Row

```cpp
Row()
```


### function Row

```cpp
explicit Row(
    const std::string & str
)
```


### function Row

```cpp
Row(
    const Row & s
)
```


### function Row

```cpp
Row(
    size_t major_slices,
    const Row & major,
    size_t secondary_slices,
    const Row & secondary
)
```


### function Row

```cpp
Row(
    const hybridse::base::RefCountedSlice & s,
    size_t secondary_slices,
    const Row & secondary
)
```


### function Row

```cpp
explicit Row(
    const hybridse::base::RefCountedSlice & s
)
```


### function ~Row

```cpp
virtual ~Row()
```


### function buf

```cpp
inline int8_t * buf() const
```


### function buf

```cpp
inline int8_t * buf(
    int32_t pos
) const
```


### function size

```cpp
inline int32_t size() const
```


### function size

```cpp
inline int32_t size(
    int32_t pos
) const
```


### function empty

```cpp
inline bool empty() const
```


### function compare

```cpp
int compare(
    const Row & b
) const
```


### function GetRowPtrs

```cpp
int8_t ** GetRowPtrs() const
```


### function GetRowPtrCnt

```cpp
int32_t GetRowPtrCnt() const
```


### function GetRowSizes

```cpp
int32_t * GetRowSizes() const
```


### function GetSlice

```cpp
inline hybridse::base::RefCountedSlice GetSlice(
    uint32_t slice_index
) const
```


### function Append

```cpp
inline void Append(
    const hybridse::base::RefCountedSlice & slice
)
```


### function ToString

```cpp
std::string ToString() const
```


### function Reset

```cpp
inline void Reset(
    const int8_t * buf,
    size_t size
)
```


-------------------------------

Updated on 29 March 2021 at 10:12:21 PDT