---
title: hybridse::vm::DataHandlerList

---

# hybridse::vm::DataHandlerList




`#include <catalog.h>`

Inherited by [hybridse::vm::DataHandlerRepeater](/Classes/classhybridse_1_1vm_1_1_data_handler_repeater.md), [hybridse::vm::DataHandlerVector](/Classes/classhybridse_1_1vm_1_1_data_handler_vector.md)

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[DataHandlerList](/Classes/classhybridse_1_1vm_1_1_data_handler_list.md#function-datahandlerlist)**() |
| virtual | **[~DataHandlerList](/Classes/classhybridse_1_1vm_1_1_data_handler_list.md#function-~datahandlerlist)**() |
| virtual size_t | **[GetSize](/Classes/classhybridse_1_1vm_1_1_data_handler_list.md#function-getsize)**() =0 |
| virtual std::shared_ptr< [DataHandler](/Classes/classhybridse_1_1vm_1_1_data_handler.md) > | **[Get](/Classes/classhybridse_1_1vm_1_1_data_handler_list.md#function-get)**(size_t idx) =0 |

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


**Reimplemented by**: [hybridse::vm::DataHandlerVector::GetSize](/Classes/classhybridse_1_1vm_1_1_data_handler_vector.md#function-getsize), [hybridse::vm::DataHandlerRepeater::GetSize](/Classes/classhybridse_1_1vm_1_1_data_handler_repeater.md#function-getsize)


### function Get

```cpp
virtual std::shared_ptr< DataHandler > Get(
    size_t idx
) =0
```


**Reimplemented by**: [hybridse::vm::DataHandlerVector::Get](/Classes/classhybridse_1_1vm_1_1_data_handler_vector.md#function-get), [hybridse::vm::DataHandlerRepeater::Get](/Classes/classhybridse_1_1vm_1_1_data_handler_repeater.md#function-get)


-------------------------------

Updated on 28 March 2021 at 19:23:48 PDT