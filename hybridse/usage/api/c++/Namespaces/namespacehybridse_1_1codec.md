---
title: hybridse::codec

---
# hybridse::codec

## Classes

|                | Name           |
| -------------- | -------------- |
| struct | **[hybridse::codec::ColInfo](/hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_col_info.md)**  |
| class | **[hybridse::codec::ListV](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md)** <br>Basic key-value list of HybridSe.  |
| class | **[hybridse::codec::Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md)**  |
| class | **[hybridse::codec::RowBuilder](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_builder.md)**  |
| class | **[hybridse::codec::RowFormat](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_format.md)**  |
| class | **[hybridse::codec::RowSelector](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_selector.md)**  |
| class | **[hybridse::codec::RowView](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md)**  |
| class | **[hybridse::codec::SchemaCodec](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_schema_codec.md)**  |
| struct | **[hybridse::codec::StringColInfo](/hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_string_col_info.md)**  |
| class | **[hybridse::codec::WindowIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_window_iterator.md)** <br>A iterator over a Row-Iterator<[codec::Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md)> pairs dataset.  |

## Types

|                | Name           |
| -------------- | -------------- |
| typedef ::google::protobuf::RepeatedPtrField<::hybridse::type::ColumnDef > | **[Schema](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1codec.md#typedef-schema)**  |
| typedef [ConstIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_const_iterator.md)< uint64_t, [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) > | **[RowIterator](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1codec.md#typedef-rowiterator)**  |

## Functions

|                | Name           |
| -------------- | -------------- |
| const uint32_t | **[BitMapSize](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1codec.md#function-bitmapsize)**(uint32_t size) |
| const std::unordered_map<::hybridse::type::Type, uint8_t > & | **[GetTypeSizeMap](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1codec.md#function-gettypesizemap)**() |
| uint8_t | **[GetAddrLength](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1codec.md#function-getaddrlength)**(uint32_t size) |
| uint32_t | **[GetBitmapSize](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1codec.md#function-getbitmapsize)**(uint32_t column_size) |
| uint32_t | **[GetStartOffset](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1codec.md#function-getstartoffset)**(int32_t column_count) |
| void | **[FillNullStringOffset](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1codec.md#function-fillnullstringoffset)**(int8_t * buf, uint32_t start, uint32_t addr_length, uint32_t str_idx, uint32_t str_offset) |

## Attributes

|                | Name           |
| -------------- | -------------- |
| constexpr uint8_t | **[VERSION_LENGTH](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1codec.md#variable-version_length)**  |
| constexpr uint8_t | **[SIZE_LENGTH](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1codec.md#variable-size_length)**  |
| constexpr uint8_t | **[HEADER_LENGTH](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1codec.md#variable-header_length)**  |
| constexpr uint32_t | **[UINT24_MAX](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1codec.md#variable-uint24_max)**  |
| const std::string | **[NONETOKEN](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1codec.md#variable-nonetoken)**  |
| const std::string | **[EMPTY_STRING](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1codec.md#variable-empty_string)**  |
| const uint32_t | **[MAX_ROW_BYTE_SIZE](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1codec.md#variable-max_row_byte_size)**  |
| const uint32_t | **[FIELD_BYTE_SIZE](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1codec.md#variable-field_byte_size)**  |
| const uint16_t | **[HEADER_SIZE](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1codec.md#variable-header_size)**  |

## Types Documentation

### typedef Schema

```cpp
typedef ::google::protobuf::RepeatedPtrField<::hybridse::type::ColumnDef> hybridse::codec::Schema;
```


### typedef RowIterator

```cpp
typedef ConstIterator<uint64_t, Row> hybridse::codec::RowIterator;
```



## Functions Documentation

### function BitMapSize

```cpp
const uint32_t BitMapSize(
    uint32_t size
)
```


### function GetTypeSizeMap

```cpp
const std::unordered_map<::hybridse::type::Type, uint8_t > & GetTypeSizeMap()
```


### function GetAddrLength

```cpp
inline uint8_t GetAddrLength(
    uint32_t size
)
```


### function GetBitmapSize

```cpp
inline uint32_t GetBitmapSize(
    uint32_t column_size
)
```


### function GetStartOffset

```cpp
inline uint32_t GetStartOffset(
    int32_t column_count
)
```


### function FillNullStringOffset

```cpp
void FillNullStringOffset(
    int8_t * buf,
    uint32_t start,
    uint32_t addr_length,
    uint32_t str_idx,
    uint32_t str_offset
)
```



## Attributes Documentation

### variable VERSION_LENGTH

```cpp
static constexpr uint8_t VERSION_LENGTH = 2;
```


### variable SIZE_LENGTH

```cpp
static constexpr uint8_t SIZE_LENGTH = 4;
```


### variable HEADER_LENGTH

```cpp
static constexpr uint8_t HEADER_LENGTH = VERSION_LENGTH + SIZE_LENGTH;
```


### variable UINT24_MAX

```cpp
static constexpr uint32_t UINT24_MAX = (1 << 24) - 1;
```


### variable NONETOKEN

```cpp
const std::string NONETOKEN = "!N@U#L$L%";
```


### variable EMPTY_STRING

```cpp
const std::string EMPTY_STRING = "!@#$%";
```


### variable MAX_ROW_BYTE_SIZE

```cpp
const uint32_t MAX_ROW_BYTE_SIZE = 1024 * 1024;
```


### variable FIELD_BYTE_SIZE

```cpp
const uint32_t FIELD_BYTE_SIZE = 3;
```


### variable HEADER_SIZE

```cpp
const uint16_t HEADER_SIZE = 2;
```





-------------------------------

Updated on  1 April 2021 at 16:11:23 PDT