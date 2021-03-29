---
title: hybridse::vm::RowHandler
summary: A row operation abstraction. 

---

# hybridse::vm::RowHandler



A row operation abstraction. 
`#include <catalog.h>`

Inherits from [hybridse::vm::DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md), [hybridse::codec::ListV< Row >](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md)

Inherited by [hybridse::vm::AysncRowHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_aysnc_row_handler.md), [hybridse::vm::ErrorRowHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_error_row_handler.md), [hybridse::vm::MemRowHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_row_handler.md)

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[RowHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-rowhandler)**() |
| virtual | **[~RowHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-~rowhandler)**() |
| virtual std::unique_ptr< RowIterator > | **[GetIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-getiterator)**() override<br>Return `null` since GetIterator isn't supported for a row.  |
| virtual RowIterator * | **[GetRawIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-getrawiterator)**() override<br>Return `null` since GetRawIterator isn't supported for a row,.  |
| virtual const uint64_t | **[GetCount](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-getcount)**() override<br>Return 0 since Getcount isn't supported for a row.  |
| virtual [Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md) | **[At](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-at)**(uint64_t pos) override<br>Return 0 since Getcount isn't supported for a row.  |
| virtual const [HandlerType](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) | **[GetHanlderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-gethanldertype)**() override |
| virtual const [Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md) & | **[GetValue](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-getvalue)**() =0<br>Implemented by subclasses to return value of row.  |
| virtual const std::string | **[GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-gethandlertypename)**() override |

## Additional inherited members

**Public Functions inherited from [hybridse::vm::DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-datahandler)**() |
| virtual | **[~DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-~datahandler)**() |
| virtual const Schema * | **[GetSchema](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getschema)**() =0<br>Implemented by subclasses to return table schema.  |
| virtual const std::string & | **[GetName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getname)**() =0<br>Implemented by subclasses to return table name.  |
| virtual const std::string & | **[GetDatabase](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getdatabase)**() =0<br>Implemented by subclasses to return the name of database.  |
| virtual base::Status | **[GetStatus](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getstatus)**()<br>Return dataset status. Default is hybridse::common::kOk.  |

**Public Functions inherited from [hybridse::codec::ListV< Row >](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md)**

|                | Name           |
| -------------- | -------------- |
| | **[ListV](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md#function-listv)**() |
| virtual | **[~ListV](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md#function-~listv)**() |


## Public Functions Documentation

### function RowHandler

```cpp
inline RowHandler()
```


### function ~RowHandler

```cpp
inline virtual ~RowHandler()
```


### function GetIterator

```cpp
inline virtual std::unique_ptr< RowIterator > GetIterator() override
```

Return `null` since GetIterator isn't supported for a row. 

**Reimplements**: [hybridse::codec::ListV::GetIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getiterator)


### function GetRawIterator

```cpp
inline virtual RowIterator * GetRawIterator() override
```

Return `null` since GetRawIterator isn't supported for a row,. 

**Reimplements**: [hybridse::codec::ListV::GetRawIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getrawiterator)


### function GetCount

```cpp
inline virtual const uint64_t GetCount() override
```

Return 0 since Getcount isn't supported for a row. 

**Reimplements**: [hybridse::codec::ListV::GetCount](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getcount)


### function At

```cpp
inline virtual Row At(
    uint64_t pos
) override
```

Return 0 since Getcount isn't supported for a row. 

**Reimplements**: [hybridse::codec::ListV::At](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md#function-at)


### function GetHanlderType

```cpp
inline virtual const HandlerType GetHanlderType() override
```


**Reimplements**: [hybridse::vm::DataHandler::GetHanlderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethanldertype)


Return the HandlerType of the row handler. Return HandlerType::kRowHandler by default 


### function GetValue

```cpp
virtual const Row & GetValue() =0
```

Implemented by subclasses to return value of row. 

**Reimplemented by**: [hybridse::vm::ErrorRowHandler::GetValue](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_error_row_handler.md#function-getvalue), [hybridse::vm::AysncRowHandler::GetValue](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_aysnc_row_handler.md#function-getvalue), [hybridse::vm::MemRowHandler::GetValue](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_row_handler.md#function-getvalue)


### function GetHandlerTypeName

```cpp
inline virtual const std::string GetHandlerTypeName() override
```


**Reimplements**: [hybridse::vm::DataHandler::GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethandlertypename)


**Reimplemented by**: [hybridse::vm::ErrorRowHandler::GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_error_row_handler.md#function-gethandlertypename), [hybridse::vm::MemRowHandler::GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_row_handler.md#function-gethandlertypename)


Return the name of handler type. Return `"RowHandler"` by default. 


-------------------------------

Updated on 29 March 2021 at 10:12:21 PDT