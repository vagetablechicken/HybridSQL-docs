---
title: hybridse::codec::RowView

---
# hybridse::codec::RowView



`#include <fe_row_codec.h>`

## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[RowView](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-rowview)**()|  |
|**[RowView](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-rowview)**(const [hybridse::codec::Schema](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1codec.md#typedef-schema) & schema, const int8_t * row, uint32_t size)|  |
|**[RowView](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-rowview)**(const [hybridse::codec::Schema](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1codec.md#typedef-schema) & schema)|  |
|**[RowView](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-rowview)**(const [RowView](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md) & row_view)|  |
|**[~RowView](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-~rowview)**() =default|  |
|**[Reset](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-reset)**(const int8_t * row, uint32_t size)| bool  |
|**[Reset](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-reset)**(const int8_t * row)| bool  |
|**[Reset](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-reset)**(const hybridse::base::RawBuffer & buf)| bool  |
|**[GetBool](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-getbool)**(uint32_t idx, bool * val)| int32_t  |
|**[GetInt32](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-getint32)**(uint32_t idx, int32_t * val)| int32_t  |
|**[GetInt64](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-getint64)**(uint32_t idx, int64_t * val)| int32_t  |
|**[GetTimestamp](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-gettimestamp)**(uint32_t idx, int64_t * val)| int32_t  |
|**[GetInt16](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-getint16)**(uint32_t idx, int16_t * val)| int32_t  |
|**[GetFloat](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-getfloat)**(uint32_t idx, float * val)| int32_t  |
|**[GetDouble](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-getdouble)**(uint32_t idx, double * val)| int32_t  |
|**[GetString](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-getstring)**(uint32_t idx, const char ** val, uint32_t * length)| int32_t  |
|**[GetDate](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-getdate)**(uint32_t idx, int32_t * year, int32_t * month, int32_t * day)| int32_t  |
|**[GetDate](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-getdate)**(uint32_t idx, int32_t * date)| int32_t  |
|**[GetBoolUnsafe](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-getboolunsafe)**(uint32_t idx)| bool  |
|**[GetInt32Unsafe](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-getint32unsafe)**(uint32_t idx)| int32_t  |
|**[GetInt64Unsafe](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-getint64unsafe)**(uint32_t idx)| int64_t  |
|**[GetTimestampUnsafe](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-gettimestampunsafe)**(uint32_t idx)| int64_t  |
|**[GetDateUnsafe](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-getdateunsafe)**(uint32_t idx)| int32_t  |
|**[GetYearUnsafe](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-getyearunsafe)**(int32_t days)| int32_t  |
|**[GetMonthUnsafe](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-getmonthunsafe)**(int32_t days)| int32_t  |
|**[GetDayUnsafe](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-getdayunsafe)**(int32_t idx)| int32_t  |
|**[GetInt16Unsafe](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-getint16unsafe)**(uint32_t idx)| int16_t  |
|**[GetFloatUnsafe](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-getfloatunsafe)**(uint32_t idx)| float  |
|**[GetDoubleUnsafe](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-getdoubleunsafe)**(uint32_t idx)| double  |
|**[GetStringUnsafe](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-getstringunsafe)**(uint32_t idx)| std::string  |
|**[IsNULL](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-isnull)**(uint32_t idx)| bool  |
|**[GetSize](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-getsize)**()| uint32_t  |
|**[GetValue](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-getvalue)**(const int8_t * row, uint32_t idx, ::hybridse::type::Type type, void * val) const| int32_t  |
|**[GetInteger](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-getinteger)**(const int8_t * row, uint32_t idx, ::hybridse::type::Type type, int64_t * val)| int32_t  |
|**[GetValue](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-getvalue)**(const int8_t * row, uint32_t idx, const char ** val, uint32_t * length) const| int32_t  |
|**[GetAsString](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-getasstring)**(uint32_t idx)| std::string  |
|**[GetRowString](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-getrowstring)**()| std::string  |
|**[GetPrimaryFieldOffset](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-getprimaryfieldoffset)**(uint32_t idx)| int32_t  |
|**[GetSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-getschema)**() const| const [Schema](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1codec.md#typedef-schema) *  |
|**[IsNULL](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-isnull)**(const int8_t * row, uint32_t idx) const| bool  |
|**[GetSize](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md#function-getsize)**(const int8_t * row)| uint32_t  |

## Public Functions

#### RowView { function RowView }

```cpp
RowView()
```


#### RowView { function RowView }

```cpp
RowView(
    const hybridse::codec::Schema & schema,
    const int8_t * row,
    uint32_t size
)
```


#### RowView { function RowView }

```cpp
explicit RowView(
    const hybridse::codec::Schema & schema
)
```


#### RowView { function RowView }

```cpp
RowView(
    const RowView & row_view
)
```


#### ~RowView { function ~RowView }

```cpp
~RowView() =default
```


#### Reset { function Reset }

```cpp
bool Reset(
    const int8_t * row,
    uint32_t size
)
```


#### Reset { function Reset }

```cpp
bool Reset(
    const int8_t * row
)
```


#### Reset { function Reset }

```cpp
bool Reset(
    const hybridse::base::RawBuffer & buf
)
```


#### GetBool { function GetBool }

```cpp
int32_t GetBool(
    uint32_t idx,
    bool * val
)
```


#### GetInt32 { function GetInt32 }

```cpp
int32_t GetInt32(
    uint32_t idx,
    int32_t * val
)
```


#### GetInt64 { function GetInt64 }

```cpp
int32_t GetInt64(
    uint32_t idx,
    int64_t * val
)
```


#### GetTimestamp { function GetTimestamp }

```cpp
int32_t GetTimestamp(
    uint32_t idx,
    int64_t * val
)
```


#### GetInt16 { function GetInt16 }

```cpp
int32_t GetInt16(
    uint32_t idx,
    int16_t * val
)
```


#### GetFloat { function GetFloat }

```cpp
int32_t GetFloat(
    uint32_t idx,
    float * val
)
```


#### GetDouble { function GetDouble }

```cpp
int32_t GetDouble(
    uint32_t idx,
    double * val
)
```


#### GetString { function GetString }

```cpp
int32_t GetString(
    uint32_t idx,
    const char ** val,
    uint32_t * length
)
```


#### GetDate { function GetDate }

```cpp
int32_t GetDate(
    uint32_t idx,
    int32_t * year,
    int32_t * month,
    int32_t * day
)
```


#### GetDate { function GetDate }

```cpp
int32_t GetDate(
    uint32_t idx,
    int32_t * date
)
```


#### GetBoolUnsafe { function GetBoolUnsafe }

```cpp
bool GetBoolUnsafe(
    uint32_t idx
)
```


#### GetInt32Unsafe { function GetInt32Unsafe }

```cpp
int32_t GetInt32Unsafe(
    uint32_t idx
)
```


#### GetInt64Unsafe { function GetInt64Unsafe }

```cpp
int64_t GetInt64Unsafe(
    uint32_t idx
)
```


#### GetTimestampUnsafe { function GetTimestampUnsafe }

```cpp
int64_t GetTimestampUnsafe(
    uint32_t idx
)
```


#### GetDateUnsafe { function GetDateUnsafe }

```cpp
int32_t GetDateUnsafe(
    uint32_t idx
)
```


#### GetYearUnsafe { function GetYearUnsafe }

```cpp
int32_t GetYearUnsafe(
    int32_t days
)
```


#### GetMonthUnsafe { function GetMonthUnsafe }

```cpp
int32_t GetMonthUnsafe(
    int32_t days
)
```


#### GetDayUnsafe { function GetDayUnsafe }

```cpp
int32_t GetDayUnsafe(
    int32_t idx
)
```


#### GetInt16Unsafe { function GetInt16Unsafe }

```cpp
int16_t GetInt16Unsafe(
    uint32_t idx
)
```


#### GetFloatUnsafe { function GetFloatUnsafe }

```cpp
float GetFloatUnsafe(
    uint32_t idx
)
```


#### GetDoubleUnsafe { function GetDoubleUnsafe }

```cpp
double GetDoubleUnsafe(
    uint32_t idx
)
```


#### GetStringUnsafe { function GetStringUnsafe }

```cpp
std::string GetStringUnsafe(
    uint32_t idx
)
```


#### IsNULL { function IsNULL }

```cpp
inline bool IsNULL(
    uint32_t idx
)
```


#### GetSize { function GetSize }

```cpp
inline uint32_t GetSize()
```


#### GetValue { function GetValue }

```cpp
int32_t GetValue(
    const int8_t * row,
    uint32_t idx,
    ::hybridse::type::Type type,
    void * val
) const
```


#### GetInteger { function GetInteger }

```cpp
int32_t GetInteger(
    const int8_t * row,
    uint32_t idx,
    ::hybridse::type::Type type,
    int64_t * val
)
```


#### GetValue { function GetValue }

```cpp
int32_t GetValue(
    const int8_t * row,
    uint32_t idx,
    const char ** val,
    uint32_t * length
) const
```


#### GetAsString { function GetAsString }

```cpp
std::string GetAsString(
    uint32_t idx
)
```


#### GetRowString { function GetRowString }

```cpp
std::string GetRowString()
```


#### GetPrimaryFieldOffset { function GetPrimaryFieldOffset }

```cpp
int32_t GetPrimaryFieldOffset(
    uint32_t idx
)
```


#### GetSchema { function GetSchema }

```cpp
inline const Schema * GetSchema() const
```


#### IsNULL { function IsNULL }

```cpp
inline bool IsNULL(
    const int8_t * row,
    uint32_t idx
) const
```


#### GetSize { function GetSize }

```cpp
static inline uint32_t GetSize(
    const int8_t * row
)
```


-------------------------------

Updated on 29 March 2021 at 17:58:50 PDT