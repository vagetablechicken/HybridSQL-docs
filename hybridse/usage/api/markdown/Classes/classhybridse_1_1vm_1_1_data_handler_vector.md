---
title: hybridse::vm::DataHandlerVector

---

# hybridse::vm::DataHandlerVector




`#include <catalog.h>`

Inherits from [hybridse::vm::DataHandlerList](/Classes/classhybridse_1_1vm_1_1_data_handler_list.md)

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[DataHandlerVector](/Classes/classhybridse_1_1vm_1_1_data_handler_vector.md#function-datahandlervector)**() |
| | **[~DataHandlerVector](/Classes/classhybridse_1_1vm_1_1_data_handler_vector.md#function-~datahandlervector)**() |
| void | **[Add](/Classes/classhybridse_1_1vm_1_1_data_handler_vector.md#function-add)**(std::shared_ptr< [DataHandler](/Classes/classhybridse_1_1vm_1_1_data_handler.md) > data_handler) |
| virtual size_t | **[GetSize](/Classes/classhybridse_1_1vm_1_1_data_handler_vector.md#function-getsize)**() |
| virtual std::shared_ptr< [DataHandler](/Classes/classhybridse_1_1vm_1_1_data_handler.md) > | **[Get](/Classes/classhybridse_1_1vm_1_1_data_handler_vector.md#function-get)**(size_t idx) |

## Additional inherited members

**Public Functions inherited from [hybridse::vm::DataHandlerList](/Classes/classhybridse_1_1vm_1_1_data_handler_list.md)**

|                | Name           |
| -------------- | -------------- |
| | **[DataHandlerList](/Classes/classhybridse_1_1vm_1_1_data_handler_list.md#function-datahandlerlist)**() |
| virtual | **[~DataHandlerList](/Classes/classhybridse_1_1vm_1_1_data_handler_list.md#function-~datahandlerlist)**() |


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


**Reimplements**: [hybridse::vm::DataHandlerList::GetSize](/Classes/classhybridse_1_1vm_1_1_data_handler_list.md#function-getsize)


### function Get

```cpp
inline virtual std::shared_ptr< DataHandler > Get(
    size_t idx
)
```


**Reimplements**: [hybridse::vm::DataHandlerList::Get](/Classes/classhybridse_1_1vm_1_1_data_handler_list.md#function-get)


-------------------------------

Updated on 28 March 2021 at 19:23:48 PDT