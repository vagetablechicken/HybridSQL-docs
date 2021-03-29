---
title: hybridse::vm::DataHandlerVector

---

# hybridse::vm::DataHandlerVector




`#include <catalog.h>`

Inherits from [hybridse::vm::DataHandlerList](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_list.md)

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[DataHandlerVector](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_vector.md#function-datahandlervector)**() |
| | **[~DataHandlerVector](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_vector.md#function-~datahandlervector)**() |
| void | **[Add](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_vector.md#function-add)**(std::shared_ptr< [DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md) > data_handler) |
| virtual size_t | **[GetSize](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_vector.md#function-getsize)**() |
| virtual std::shared_ptr< [DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md) > | **[Get](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_vector.md#function-get)**(size_t idx) |

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


**Reimplements**: [hybridse::vm::DataHandlerList::GetSize](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_list.md#function-getsize)


### function Get

```cpp
inline virtual std::shared_ptr< DataHandler > Get(
    size_t idx
)
```


**Reimplements**: [hybridse::vm::DataHandlerList::Get](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_list.md#function-get)


-------------------------------

Updated on 28 March 2021 at 19:41:19 PDT