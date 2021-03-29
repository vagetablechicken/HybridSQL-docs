---
title: hybridse::vm::DataHandlerRepeater
summary: A implementation of DataHandlerList. 

---

# hybridse::vm::DataHandlerRepeater



A implementation of [DataHandlerList](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_list.md).  [More...](#detailed-description)


`#include <catalog.h>`

Inherits from [hybridse::vm::DataHandlerList](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_list.md)

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[DataHandlerRepeater](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_repeater.md#function-datahandlerrepeater)**(std::shared_ptr< [DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md) > data_handler, size_t size)<br>Create [DataHandlerRepeater](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_repeater.md) with a [DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md) and elements number.  |
| | **[~DataHandlerRepeater](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_repeater.md#function-~datahandlerrepeater)**() |
| virtual size_t | **[GetSize](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_repeater.md#function-getsize)**()<br>Return the number of elements.  |
| virtual std::shared_ptr< [DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md) > | **[Get](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_repeater.md#function-get)**(size_t idx)<br>Return the idx-th element. Return `null` when position is out of range.  |

## Additional inherited members

**Public Functions inherited from [hybridse::vm::DataHandlerList](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_list.md)**

|                | Name           |
| -------------- | -------------- |
| | **[DataHandlerList](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_list.md#function-datahandlerlist)**() |
| virtual | **[~DataHandlerList](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_list.md#function-~datahandlerlist)**() |


## Detailed Description

```cpp
class hybridse::vm::DataHandlerRepeater;
```

A implementation of [DataHandlerList](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_list.md). 

Actually, we just keep one data_handler_ in container where elements are repeated logically. 

## Public Functions Documentation

### function DataHandlerRepeater

```cpp
inline DataHandlerRepeater(
    std::shared_ptr< DataHandler > data_handler,
    size_t size
)
```

Create [DataHandlerRepeater](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_repeater.md) with a [DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md) and elements number. 

### function ~DataHandlerRepeater

```cpp
inline ~DataHandlerRepeater()
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