---
title: hybridse::vm::DataHandlerList

---

# hybridse::vm::DataHandlerList




`#include <catalog.h>`

Inherited by [hybridse::vm::DataHandlerRepeater](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler_repeater.md), [hybridse::vm::DataHandlerVector](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler_vector.md)

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[DataHandlerList](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler_list.md#function-datahandlerlist)**() |
| virtual | **[~DataHandlerList](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler_list.md#function-~datahandlerlist)**() |
| virtual size_t | **[GetSize](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler_list.md#function-getsize)**() =0 |
| virtual std::shared_ptr< [DataHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md) > | **[Get](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler_list.md#function-get)**(size_t idx) =0 |

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


**Reimplemented by**: [hybridse::vm::DataHandlerVector::GetSize](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler_vector.md#function-getsize), [hybridse::vm::DataHandlerRepeater::GetSize](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler_repeater.md#function-getsize)


### function Get

```cpp
virtual std::shared_ptr< DataHandler > Get(
    size_t idx
) =0
```


**Reimplemented by**: [hybridse::vm::DataHandlerVector::Get](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler_vector.md#function-get), [hybridse::vm::DataHandlerRepeater::Get](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler_repeater.md#function-get)


-------------------------------

Updated on 28 March 2021 at 19:34:48 PDT