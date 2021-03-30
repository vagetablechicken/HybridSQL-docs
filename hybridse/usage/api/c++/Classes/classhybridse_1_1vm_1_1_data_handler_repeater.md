---
title: hybridse::vm::DataHandlerRepeater
summary: A implementation of DataHandlerList. 

---
# hybridse::vm::DataHandlerRepeater



`#include <catalog.h>`

A implementation of [DataHandlerList](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_list.md). 
## Summary

```cpp
class hybridse::vm::DataHandlerRepeater;
```
A implementation of [DataHandlerList](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_list.md). 

Actually, we just keep one data_handler_ in container where elements are repeated logically. 



|  Public functions|            |
| -------------- | -------------- |
|**[DataHandlerRepeater](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_repeater.md#function-datahandlerrepeater)**(std::shared_ptr< [DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md) > data_handler, size_t size)| <br>Create [DataHandlerRepeater](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_repeater.md) with a [DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md) and elements number.  |
|**[~DataHandlerRepeater](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_repeater.md#function-~datahandlerrepeater)**()|  |
|**[GetSize](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_repeater.md#function-getsize)**()| size_t <br>Return the number of elements.  |
|**[Get](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_repeater.md#function-get)**(size_t idx)| std::shared_ptr< [DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md) > <br>Return the idx-th element. Return `null` when position is out of range.  |

## Inherited members
Inherited from [hybridse::vm::DataHandlerList](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_list.md)
| **Inherited public functions** | Name           |
| -------------- | -------------- |
|**[DataHandlerList](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_list.md#function-datahandlerlist)**()|  |
|**[~DataHandlerList](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_list.md#function-~datahandlerlist)**()| virtual  |


## Public Functions

#### function DataHandlerRepeater

```cpp
inline DataHandlerRepeater(
    std::shared_ptr< DataHandler > data_handler,
    size_t size
)
```

Create [DataHandlerRepeater](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_repeater.md) with a [DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md) and elements number. 

#### function ~DataHandlerRepeater

```cpp
inline ~DataHandlerRepeater()
```


#### function GetSize

```cpp
inline virtual size_t GetSize()
```

Return the number of elements. 

**Reimplements**: [hybridse::vm::DataHandlerList::GetSize](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_list.md#function-getsize)


#### function Get

```cpp
inline virtual std::shared_ptr< DataHandler > Get(
    size_t idx
)
```

Return the idx-th element. Return `null` when position is out of range. 

**Reimplements**: [hybridse::vm::DataHandlerList::Get](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_list.md#function-get)


-------------------------------

Updated on 29 March 2021 at 18:05:16 PDT