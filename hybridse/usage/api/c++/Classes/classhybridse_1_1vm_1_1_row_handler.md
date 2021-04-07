---
title: hybridse::vm::RowHandler
summary: A row operation abstraction. 

---
# hybridse::vm::RowHandler



`#include <catalog.h>`

A row operation abstraction. 
## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[RowHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-rowhandler)**()|  |
|**[~RowHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-~rowhandler)**()|  |
|**[GetIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-getiterator)**() override| std::unique_ptr< RowIterator > <br>Return `null` since GetIterator isn't supported for a row.  |
|**[GetRawIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-getrawiterator)**() override| RowIterator * <br>Return `null` since GetRawIterator isn't supported for a row,.  |
|**[GetCount](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-getcount)**() override| const uint64_t <br>Return 0 since Getcount isn't supported for a row.  |
|**[At](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-at)**(uint64_t pos) override| [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) <br>Return 0 since Getcount isn't supported for a row.  |
|**[GetHanlderType](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-gethanldertype)**() override| const [HandlerType](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype)  |
|**[GetValue](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-getvalue)**() =0| const [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) & <br>Return value of row.  |
|**[GetHandlerTypeName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-gethandlertypename)**() override| const std::string  |

## Inherited members
Inherited by [hybridse::vm::AysncRowHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_aysnc_row_handler.md), [hybridse::vm::ErrorRowHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_row_handler.md), [hybridse::vm::MemRowHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_row_handler.md)
Inherited from [hybridse::vm::DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md)
|  Inherited Public functions|            |
| -------------- | -------------- |
|**[DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-datahandler)**()|  |
|**[~DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-~datahandler)**()|  |
|**[GetSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getschema)**() =0| const Schema * <br>Return table schema.  |
|**[GetName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getname)**() =0| const std::string & <br>Return table name.  |
|**[GetDatabase](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getdatabase)**() =0| const std::string & <br>Return the name of database.  |
|**[GetStatus](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getstatus)**()| base::Status <br>Return dataset status. Default is hybridse::common::kOk.  |

Inherited from [hybridse::codec::ListV< Row >](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md)
|  Inherited Public functions|            |
| -------------- | -------------- |
|**[ListV](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-listv)**()|  |
|**[~ListV](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-~listv)**()|  |


## Public Functions

#### function RowHandler

```cpp
inline RowHandler()
```


#### function ~RowHandler

```cpp
inline virtual ~RowHandler()
```


#### function GetIterator

```cpp
inline virtual std::unique_ptr< RowIterator > GetIterator() override
```

Return `null` since GetIterator isn't supported for a row. 

**Reimplements**: [hybridse::codec::ListV::GetIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getiterator)


#### function GetRawIterator

```cpp
inline virtual RowIterator * GetRawIterator() override
```

Return `null` since GetRawIterator isn't supported for a row,. 

**Reimplements**: [hybridse::codec::ListV::GetRawIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getrawiterator)


#### function GetCount

```cpp
inline virtual const uint64_t GetCount() override
```

Return 0 since Getcount isn't supported for a row. 

**Reimplements**: [hybridse::codec::ListV::GetCount](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getcount)


#### function At

```cpp
inline virtual Row At(
    uint64_t pos
) override
```

Return 0 since Getcount isn't supported for a row. 

**Reimplements**: [hybridse::codec::ListV::At](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-at)


#### function GetHanlderType

```cpp
inline virtual const HandlerType GetHanlderType() override
```


**Reimplements**: [hybridse::vm::DataHandler::GetHanlderType](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethanldertype)


Return the HandlerType of the row handler. Return HandlerType::kRowHandler by default 

#### function GetValue

```cpp
virtual const Row & GetValue() =0
```

Return value of row. 

**Reimplemented by**: [hybridse::vm::ErrorRowHandler::GetValue](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_row_handler.md#function-getvalue), [hybridse::vm::AysncRowHandler::GetValue](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_aysnc_row_handler.md#function-getvalue), [hybridse::vm::MemRowHandler::GetValue](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_row_handler.md#function-getvalue)


#### function GetHandlerTypeName

```cpp
inline virtual const std::string GetHandlerTypeName() override
```


**Return**: name of handler type, default is `"RowHandler"`

**Reimplements**: [hybridse::vm::DataHandler::GetHandlerTypeName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethandlertypename)


**Reimplemented by**: [hybridse::vm::ErrorRowHandler::GetHandlerTypeName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_row_handler.md#function-gethandlertypename), [hybridse::vm::MemRowHandler::GetHandlerTypeName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_row_handler.md#function-gethandlertypename)


Get the name of handler type. 

-------------------------------

Updated on  6 April 2021 at 19:38:01 PDT