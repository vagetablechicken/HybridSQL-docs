---
title: hybridse::vm::DataHandlerVector
summary: A implementation of DataHandlerList. 

---
# hybridse::vm::DataHandlerVector



`#include <catalog.h>`

A implementation of [DataHandlerList](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_list.md). 
## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[DataHandlerVector](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_vector.md#function-datahandlervector)**()|  |
|**[~DataHandlerVector](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_vector.md#function-~datahandlervector)**()|  |
|**[Add](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_vector.md#function-add)**(std::shared_ptr< [DataHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md) > data_handler)| void  |
|**[GetSize](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_vector.md#function-getsize)**()| size_t <br>Return the number of elements.  |
|**[Get](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_vector.md#function-get)**(size_t idx)| std::shared_ptr< [DataHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md) > <br>Return the idx-th element. Return `null` when position is out of range.  |

## Inherited members
Inherited from [hybridse::vm::DataHandlerList](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_list.md)
| **Inherited public functions** |            |
| -------------- | -------------- |
|**[DataHandlerList](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_list.md#function-datahandlerlist)**()| |
|**[~DataHandlerList](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_list.md#function-~datahandlerlist)**()| virtual |


## Public Functions

#### function DataHandlerVector

```cpp
inline DataHandlerVector()
```


#### function ~DataHandlerVector

```cpp
inline ~DataHandlerVector()
```


#### function Add

```cpp
inline void Add(
    std::shared_ptr< DataHandler > data_handler
)
```


#### function GetSize

```cpp
inline virtual size_t GetSize()
```

Return the number of elements. 

**Reimplements**: [hybridse::vm::DataHandlerList::GetSize](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_list.md#function-getsize)


#### function Get

```cpp
inline virtual std::shared_ptr< DataHandler > Get(
    size_t idx
)
```

Return the idx-th element. Return `null` when position is out of range. 

**Reimplements**: [hybridse::vm::DataHandlerList::Get](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_list.md#function-get)


-------------------------------

Updated on  6 April 2021 at 08:47:46 PDT