---
title: hybridse::vm::DataHandlerVector
summary: A implementation of DataHandlerList. 

---

# hybridse::vm::DataHandlerVector



A implementation of [DataHandlerList](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_list.md). 
`#include <catalog.h>`

Inherits from [hybridse::vm::DataHandlerList](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_list.md)

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[DataHandlerVector](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_vector.md#function-datahandlervector)**() |
| | **[~DataHandlerVector](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_vector.md#function-~datahandlervector)**() |
| void | **[Add](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_vector.md#function-add)**(std::shared_ptr< [DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md) > data_handler) |
| virtual size_t | **[GetSize](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_vector.md#function-getsize)**()<br>Return the number of elements.  |
| virtual std::shared_ptr< [DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md) > | **[Get](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_vector.md#function-get)**(size_t idx)<br>Return the idx-th element. Return `null` when position is out of range.  |

## Additional inherited members

**Public Functions inherited from [hybridse::vm::DataHandlerList](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_list.md)**

|                | Name           |
| -------------- | -------------- |
| | **[DataHandlerList](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_list.md#function-datahandlerlist)**() |
| virtual | **[~DataHandlerList](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_list.md#function-~datahandlerlist)**() |


## Public Functions Documentation

### function DataHandlerVector

```cpp
inline DataHandlerVector()
```


### function ~DataHandlerVector

```cpp
inline ~DataHandlerVector()
```


### function Add

```cpp
inline void Add(
    std::shared_ptr< DataHandler > data_handler
)
```


### function GetSize

```cpp
inline virtual size_t GetSize()
```

Return the number of elements. 

**Reimplements**: [hybridse::vm::DataHandlerList::GetSize](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_list.md#function-getsize)


### function Get

```cpp
inline virtual std::shared_ptr< DataHandler > Get(
    size_t idx
)
```

Return the idx-th element. Return `null` when position is out of range. 

**Reimplements**: [hybridse::vm::DataHandlerList::Get](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_list.md#function-get)


-------------------------------

Updated on 29 March 2021 at 10:12:21 PDT