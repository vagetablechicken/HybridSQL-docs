---
title: hybridse::codec::Row

---
# hybridse::codec::Row



`#include <row.h>`

## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md#function-row)**()|  |
|**[Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md#function-row)**(const std::string & str)|  |
|**[Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md#function-row)**(const [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) & s)|  |
|**[Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md#function-row)**(size_t major_slices, const [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) & major, size_t secondary_slices, const [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) & secondary)|  |
|**[Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md#function-row)**(const hybridse::base::RefCountedSlice & s, size_t secondary_slices, const [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) & secondary)|  |
|**[Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md#function-row)**(const hybridse::base::RefCountedSlice & s)|  |
|**[~Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md#function-~row)**()|  |
|**[buf](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md#function-buf)**() const| int8_t *  |
|**[buf](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md#function-buf)**(int32_t pos) const| int8_t *  |
|**[size](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md#function-size)**() const| int32_t  |
|**[size](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md#function-size)**(int32_t pos) const| int32_t  |
|**[empty](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md#function-empty)**() const| bool  |
|**[compare](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md#function-compare)**(const [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) & b) const| int  |
|**[GetRowPtrs](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md#function-getrowptrs)**() const| int8_t **  |
|**[GetRowPtrCnt](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md#function-getrowptrcnt)**() const| int32_t  |
|**[GetRowSizes](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md#function-getrowsizes)**() const| int32_t *  |
|**[GetSlice](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md#function-getslice)**(uint32_t slice_index) const| hybridse::base::RefCountedSlice  |
|**[Append](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md#function-append)**(const hybridse::base::RefCountedSlice & slice)| void  |
|**[ToString](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md#function-tostring)**() const| std::string  |
|**[Reset](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md#function-reset)**(const int8_t * buf, size_t size)| void  |

## Public Functions

#### Row

```cpp
Row()
```


#### Row

```cpp
explicit Row(
    const std::string & str
)
```


#### Row

```cpp
Row(
    const Row & s
)
```


#### Row

```cpp
Row(
    size_t major_slices,
    const Row & major,
    size_t secondary_slices,
    const Row & secondary
)
```


#### Row

```cpp
Row(
    const hybridse::base::RefCountedSlice & s,
    size_t secondary_slices,
    const Row & secondary
)
```


#### Row

```cpp
explicit Row(
    const hybridse::base::RefCountedSlice & s
)
```


#### ~Row

```cpp
virtual ~Row()
```


#### buf

```cpp
inline int8_t * buf() const
```


#### buf

```cpp
inline int8_t * buf(
    int32_t pos
) const
```


#### size

```cpp
inline int32_t size() const
```


#### size

```cpp
inline int32_t size(
    int32_t pos
) const
```


#### empty

```cpp
inline bool empty() const
```


#### compare

```cpp
int compare(
    const Row & b
) const
```


#### GetRowPtrs

```cpp
int8_t ** GetRowPtrs() const
```


#### GetRowPtrCnt

```cpp
int32_t GetRowPtrCnt() const
```


#### GetRowSizes

```cpp
int32_t * GetRowSizes() const
```


#### GetSlice

```cpp
inline hybridse::base::RefCountedSlice GetSlice(
    uint32_t slice_index
) const
```


#### Append

```cpp
inline void Append(
    const hybridse::base::RefCountedSlice & slice
)
```


#### ToString

```cpp
std::string ToString() const
```


#### Reset

```cpp
inline void Reset(
    const int8_t * buf,
    size_t size
)
```


-------------------------------

Updated on 29 March 2021 at 17:34:52 PDT