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

#### RowBuilder { #function-RowBuilder }

```cpp
explicit RowBuilder(
    const hybridse::codec::Schema & schema
)
```


#### ~RowBuilder { #function-~RowBuilder }

```cpp
~RowBuilder() =default
```


#### CalTotalLength { #function-CalTotalLength }

```cpp
uint32_t CalTotalLength(
    uint32_t string_length
)
```


#### SetBuffer { #function-SetBuffer }

```cpp
bool SetBuffer(
    int8_t * buf,
    uint32_t size
)
```


#### SetBuffer { #function-SetBuffer }

```cpp
bool SetBuffer(
    int64_t buf_handle,
    uint32_t size
)
```


#### SetBuffer { #function-SetBuffer }

```cpp
bool SetBuffer(
    const hybridse::base::RawBuffer & buf
)
```


#### AppendBool { #function-AppendBool }

```cpp
bool AppendBool(
    bool val
)
```


#### AppendInt32 { #function-AppendInt32 }

```cpp
bool AppendInt32(
    int32_t val
)
```


#### AppendInt16 { #function-AppendInt16 }

```cpp
bool AppendInt16(
    int16_t val
)
```


#### AppendInt64 { #function-AppendInt64 }

```cpp
bool AppendInt64(
    int64_t val
)
```


#### AppendTimestamp { #function-AppendTimestamp }

```cpp
bool AppendTimestamp(
    int64_t val
)
```


#### AppendDate { #function-AppendDate }

```cpp
bool AppendDate(
    int32_t year,
    int32_t month,
    int32_t day
)
```


#### AppendFloat { #function-AppendFloat }

```cpp
bool AppendFloat(
    float val
)
```


#### AppendDouble { #function-AppendDouble }

```cpp
bool AppendDouble(
    double val
)
```


#### AppendString { #function-AppendString }

```cpp
bool AppendString(
    const char * val,
    uint32_t length
)
```


#### AppendNULL { #function-AppendNULL }

```cpp
bool AppendNULL()
```


-------------------------------

Updated on 29 March 2021 at 18:02:27 PDT