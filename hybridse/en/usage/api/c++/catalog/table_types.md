# Table Proto

## Type

```protobuf
enum Type {
    kBool = 0;
    kInt16 = 1;
    kInt32 = 3;
    kInt64 = 5;
    kFloat = 7;
    kDouble = 8;
    kVarchar = 9;
    kDate = 10;
    kTimestamp = 11;
    kBlob = 12;
    kNull = 101;
}
```

## ColumnDef

```protobuf
message ColumnDef {
    optional string name = 1;
    optional Type type = 2;
    optional uint32 offset = 3;
    optional bool is_not_null = 4;
    optional bool is_constant = 5 [default = false];
}
```



## IndexDef

```protobuf
message IndexDef {
    optional string name = 1;
    repeated string first_keys = 2;
    optional string second_key = 3;
    repeated string partion_keys = 4;
    repeated uint64 ttl = 5;
    optional TTLType ttl_type = 6;
    optional uint32 ts_offset = 7;
}
```



## ColInfo

```c++
struct ColInfo {
    hybridse::type::Type type;
    uint32_t idx;
    uint32_t offset;
    std::string name;
    ColInfo() {}
    ColInfo(const std::string& name, ::hybridse::type::Type type, uint32_t idx,
            uint32_t offset)
        : type(type), idx(idx), offset(offset), name(name) {}
};
```

| Field Name | Field type             | Description            |
| :--------- | ---------------------- | ---------------------- |
| `type`     | `hybridse::type::Type` | column [`Type`](#Type) |
| `idx`      | `uint32_t`             | column index           |
| `offset`   | `uint32_t`             | column offset          |
| `name`     | `std::string`          | column name            |

## IndexSt

```c++
struct IndexSt {
    std::string name;
    uint32_t index;
    uint32_t ts_pos;
    std::vector<ColInfo> keys;
};
```

| Field Name | Field type             | Description                         |
| :--------- | ---------------------- | ----------------------------------- |
| `name`     | `std::string`          | Index name                          |
| `index`    | `uint32_t`             | Position of `index`                 |
| `ts_pos`   | `uint32_t`             | Column index of ts key (second key) |
| `keys`     | `std::vector<ColInfo>` | Set of [`ColInfo`](#ColInfo)        |

## Schema

```c++
typedef ::google::protobuf::RepeatedPtrField<::hybridse::type::ColumnDef> Schema;
```

Set of [ `ColumnDef`](#ColumnDef)

### IndexHint

```c++
typedef std::map<std::string, IndexSt> IndexHint;
```

Map of [`IndexSt`](#IndexSt)

### Types

```c++
typedef std::map<std::string, ColInfo> Types;
```

