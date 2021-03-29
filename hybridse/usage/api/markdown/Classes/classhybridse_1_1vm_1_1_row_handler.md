---
title: hybridse::vm::RowHandler

---

# hybridse::vm::RowHandler




`#include <catalog.h>`

Inherits from [hybridse::vm::DataHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md), hybridse::codec::ListV< Row >

Inherited by [hybridse::vm::AysncRowHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_aysnc_row_handler.md), [hybridse::vm::ErrorRowHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_error_row_handler.md), [hybridse::vm::MemRowHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_row_handler.md)

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[RowHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_row_handler.md#function-rowhandler)**() |
| virtual | **[~RowHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_row_handler.md#function-~rowhandler)**() |
| std::unique_ptr< RowIterator > | **[GetIterator](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_row_handler.md#function-getiterator)**() override |
| RowIterator * | **[GetRawIterator](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_row_handler.md#function-getrawiterator)**() override |
| const uint64_t | **[GetCount](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_row_handler.md#function-getcount)**() override |
| Row | **[At](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_row_handler.md#function-at)**(uint64_t pos) override |
| virtual const [HandlerType](/hybridse/usage/api/markdownNamespaces/namespacehybridse_1_1vm.md#enum-handlertype) | **[GetHanlderType](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_row_handler.md#function-gethanldertype)**() override |
| virtual const Row & | **[GetValue](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_row_handler.md#function-getvalue)**() =0 |
| virtual const std::string | **[GetHandlerTypeName](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_row_handler.md#function-gethandlertypename)**() override |

## Additional inherited members

**Public Functions inherited from [hybridse::vm::DataHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[DataHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md#function-datahandler)**() |
| virtual | **[~DataHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md#function-~datahandler)**() |
| virtual const Schema * | **[GetSchema](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md#function-getschema)**() =0 |
| virtual const std::string & | **[GetName](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md#function-getname)**() =0 |
| virtual const std::string & | **[GetDatabase](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md#function-getdatabase)**() =0 |
| virtual base::Status | **[GetStatus](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md#function-getstatus)**() |


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
inline std::unique_ptr< RowIterator > GetIterator() override
```


### function GetRawIterator

```cpp
inline RowIterator * GetRawIterator() override
```


### function GetCount

```cpp
inline const uint64_t GetCount() override
```


### function At

```cpp
inline Row At(
    uint64_t pos
) override
```


### function GetHanlderType

```cpp
inline virtual const HandlerType GetHanlderType() override
```


**Return**: 

**Reimplements**: [hybridse::vm::DataHandler::GetHanlderType](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md#function-gethanldertype)


Implemented by subclasses to return the type of [DataHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md). 


### function GetValue

```cpp
virtual const Row & GetValue() =0
```


**Reimplemented by**: [hybridse::vm::ErrorRowHandler::GetValue](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_error_row_handler.md#function-getvalue), [hybridse::vm::AysncRowHandler::GetValue](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_aysnc_row_handler.md#function-getvalue), [hybridse::vm::MemRowHandler::GetValue](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_row_handler.md#function-getvalue)


### function GetHandlerTypeName

```cpp
inline virtual const std::string GetHandlerTypeName() override
```


**Return**: 

**Reimplements**: [hybridse::vm::DataHandler::GetHandlerTypeName](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md#function-gethandlertypename)


**Reimplemented by**: [hybridse::vm::ErrorRowHandler::GetHandlerTypeName](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_error_row_handler.md#function-gethandlertypename), [hybridse::vm::MemRowHandler::GetHandlerTypeName](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_row_handler.md#function-gethandlertypename)


Implemented by subclasses return the name of handler type 


-------------------------------

Updated on 28 March 2021 at 19:34:49 PDT