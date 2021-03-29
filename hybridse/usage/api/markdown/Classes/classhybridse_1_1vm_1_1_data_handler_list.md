---
title: hybridse::vm::DataHandlerList
summary: A sequence of DataHandler. 

---

# hybridse::vm::DataHandlerList



A sequence of [DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md). 
`#include <catalog.h>`

Inherited by [hybridse::vm::DataHandlerRepeater](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_repeater.md), [hybridse::vm::DataHandlerVector](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_vector.md)

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[DataHandlerList](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_list.md#function-datahandlerlist)**() |
| virtual | **[~DataHandlerList](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_list.md#function-~datahandlerlist)**() |
| virtual size_t | **[GetSize](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_list.md#function-getsize)**() =0<br>Implemented by subclass to return the number of elements.  |
| virtual std::shared_ptr< [DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md) > | **[Get](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_list.md#function-get)**(size_t idx) =0<br>Implemented by subclass to return the idx-th element.  |

## Public Functions Documentation

### function DataHandlerList

```cpp
inline DataHandlerList()
```


### function ~DataHandlerList

```cpp
inline virtual ~DataHandlerList()
```


### function GetSize

```cpp
virtual size_t GetSize() =0
```

Implemented by subclass to return the number of elements. 

**Reimplemented by**: [hybridse::vm::DataHandlerVector::GetSize](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_vector.md#function-getsize), [hybridse::vm::DataHandlerRepeater::GetSize](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_repeater.md#function-getsize)


### function Get

```cpp
virtual std::shared_ptr< DataHandler > Get(
    size_t idx
) =0
```

Implemented by subclass to return the idx-th element. 

**Reimplemented by**: [hybridse::vm::DataHandlerVector::Get](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_vector.md#function-get), [hybridse::vm::DataHandlerRepeater::Get](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler_repeater.md#function-get)


-------------------------------

Updated on 29 March 2021 at 10:12:21 PDT