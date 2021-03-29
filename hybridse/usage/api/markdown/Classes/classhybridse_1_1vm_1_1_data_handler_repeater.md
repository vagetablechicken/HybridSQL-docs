---
title: hybridse::vm::DataHandlerRepeater

---

# hybridse::vm::DataHandlerRepeater




`#include <catalog.h>`

Inherits from [hybridse::vm::DataHandlerList](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_list.md)

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[DataHandlerRepeater](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_repeater.md#function-datahandlerrepeater)**(std::shared_ptr< [DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md) > data_handler, size_t size) |
| | **[~DataHandlerRepeater](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_repeater.md#function-~datahandlerrepeater)**() |
| virtual size_t | **[GetSize](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_repeater.md#function-getsize)**() |
| virtual std::shared_ptr< [DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md) > | **[Get](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_repeater.md#function-get)**(size_t idx) |

## Additional inherited members

**Public Functions inherited from [hybridse::vm::DataHandlerList](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_list.md)**

|                | Name           |
| -------------- | -------------- |
| | **[DataHandlerList](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_list.md#function-datahandlerlist)**() |
| virtual | **[~DataHandlerList](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_list.md#function-~datahandlerlist)**() |


## Public Functions Documentation

### function DataHandlerRepeater

```cpp
inline DataHandlerRepeater(
    std::shared_ptr< DataHandler > data_handler,
    size_t size
)
```


### function ~DataHandlerRepeater

```cpp
inline ~DataHandlerRepeater()
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