---
title: hybridse::codec::SchemaCodec

---

# hybridse::codec::SchemaCodec




`#include <fe_schema_codec.h>`

## Public Functions

|                | Name           |
| -------------- | -------------- |
| bool | **[Encode](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_schema_codec.md#function-encode)**(const vm::Schema & schema, std::string * buffer) |
| bool | **[Decode](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_schema_codec.md#function-decode)**(const std::string & buf, vm::Schema * schema) |

## Public Functions Documentation

### function Encode

```cpp
static inline bool Encode(
    const vm::Schema & schema,
    std::string * buffer
)
```


### function Decode

```cpp
static inline bool Decode(
    const std::string & buf,
    vm::Schema * schema
)
```


-------------------------------

Updated on 29 March 2021 at 10:12:21 PDT