---
title: hybridse::vm::IndexSt

---
# hybridse::vm::IndexSt



`#include <catalog.h>`

## Summary


| Public attributes|    |
| -------------- | -------------- |
| std::string | **[name](/hybridse/usage/api/c++/Classes/structhybridse_1_1vm_1_1_index_st.md#variable-name)** <br>index name  |
| uint32_t | **[index](/hybridse/usage/api/c++/Classes/structhybridse_1_1vm_1_1_index_st.md#variable-index)** <br>position of index  |
| uint32_t | **[ts_pos](/hybridse/usage/api/c++/Classes/structhybridse_1_1vm_1_1_index_st.md#variable-ts_pos)** <br>second key column position  |
| std::vector< [ColInfo](/hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_col_info.md) > | **[keys](/hybridse/usage/api/c++/Classes/structhybridse_1_1vm_1_1_index_st.md#variable-keys)** <br>first keys set  |

## Public Attributes

### name

```cpp
std::string name;
```

index name 

### index

```cpp
uint32_t index;
```

position of index 

### ts_pos

```cpp
uint32_t ts_pos;
```

second key column position 

### keys

```cpp
std::vector< ColInfo > keys;
```

first keys set 

-------------------------------

Updated on 29 March 2021 at 18:02:27 PDT