---
title: hybridse::vm::DataHandlerList
summary: A sequence of DataHandler. 

---
# hybridse::vm::DataHandlerList



`#include <catalog.h>`

A sequence of [DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md). 
## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[DataHandlerList](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_list.md#function-datahandlerlist)**()|  |
|**[~DataHandlerList](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_list.md#function-~datahandlerlist)**()|  |
|**[GetSize](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_list.md#function-getsize)**() =0| size_t <br>Return the number of elements.  |
|**[Get](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_list.md#function-get)**(size_t idx) =0| std::shared_ptr< [DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md) > <br>Return the idx-th element.  |

## Public Functions

#### function DataHandlerList

```cpp
inline DataHandlerList()
```


#### function ~DataHandlerList

```cpp
inline virtual ~DataHandlerList()
```


#### function GetSize

```cpp
virtual size_t GetSize() =0
```

Return the number of elements. 

**Reimplemented by**: [hybridse::vm::DataHandlerVector::GetSize](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_vector.md#function-getsize), [hybridse::vm::DataHandlerRepeater::GetSize](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_repeater.md#function-getsize)


#### function Get

```cpp
virtual std::shared_ptr< DataHandler > Get(
    size_t idx
) =0
```

Return the idx-th element. 

**Reimplemented by**: [hybridse::vm::DataHandlerVector::Get](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_vector.md#function-get), [hybridse::vm::DataHandlerRepeater::Get](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_repeater.md#function-get)


-------------------------------

Updated on  6 April 2021 at 09:17:26 PDT