---
title: hybridse::codec::RowBuilder

---
# hybridse::codec::RowBuilder



`#include <fe_row_codec.h>`

## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[RowBuilder](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_builder.md#function-rowbuilder)**(const [hybridse::codec::Schema](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1codec.md#typedef-schema) & schema)|  |
|**[~RowBuilder](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_builder.md#function-~rowbuilder)**() =default|  |
|**[CalTotalLength](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_builder.md#function-caltotallength)**(uint32_t string_length)| uint32_t  |
|**[SetBuffer](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_builder.md#function-setbuffer)**(int8_t * buf, uint32_t size)| bool  |
|**[SetBuffer](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_builder.md#function-setbuffer)**(int64_t buf_handle, uint32_t size)| bool  |
|**[SetBuffer](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_builder.md#function-setbuffer)**(const hybridse::base::RawBuffer & buf)| bool  |
|**[AppendBool](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_builder.md#function-appendbool)**(bool val)| bool  |
|**[AppendInt32](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_builder.md#function-appendint32)**(int32_t val)| bool  |
|**[AppendInt16](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_builder.md#function-appendint16)**(int16_t val)| bool  |
|**[AppendInt64](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_builder.md#function-appendint64)**(int64_t val)| bool  |
|**[AppendTimestamp](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_builder.md#function-appendtimestamp)**(int64_t val)| bool  |
|**[AppendDate](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_builder.md#function-appenddate)**(int32_t year, int32_t month, int32_t day)| bool  |
|**[AppendFloat](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_builder.md#function-appendfloat)**(float val)| bool  |
|**[AppendDouble](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_builder.md#function-appenddouble)**(double val)| bool  |
|**[AppendString](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_builder.md#function-appendstring)**(const char * val, uint32_t length)| bool  |
|**[AppendNULL](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_builder.md#function-appendnull)**()| bool  |

## Public Functions

#### function RowBuilder

```cpp
explicit RowBuilder(
    const hybridse::codec::Schema & schema
)
```


#### function ~RowBuilder

```cpp
~RowBuilder() =default
```


#### function CalTotalLength

```cpp
uint32_t CalTotalLength(
    uint32_t string_length
)
```


#### function SetBuffer

```cpp
bool SetBuffer(
    int8_t * buf,
    uint32_t size
)
```


#### function SetBuffer

```cpp
bool SetBuffer(
    int64_t buf_handle,
    uint32_t size
)
```


#### function SetBuffer

```cpp
bool SetBuffer(
    const hybridse::base::RawBuffer & buf
)
```


#### function AppendBool

```cpp
bool AppendBool(
    bool val
)
```


#### function AppendInt32

```cpp
bool AppendInt32(
    int32_t val
)
```


#### function AppendInt16

```cpp
bool AppendInt16(
    int16_t val
)
```


#### function AppendInt64

```cpp
bool AppendInt64(
    int64_t val
)
```


#### function AppendTimestamp

```cpp
bool AppendTimestamp(
    int64_t val
)
```


#### function AppendDate

```cpp
bool AppendDate(
    int32_t year,
    int32_t month,
    int32_t day
)
```


#### function AppendFloat

```cpp
bool AppendFloat(
    float val
)
```


#### function AppendDouble

```cpp
bool AppendDouble(
    double val
)
```


#### function AppendString

```cpp
bool AppendString(
    const char * val,
    uint32_t length
)
```


#### function AppendNULL

```cpp
bool AppendNULL()
```


