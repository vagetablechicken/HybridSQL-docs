---
title: hybridse::vm::ErrorRowHandler

---

# hybridse::vm::ErrorRowHandler




`#include <catalog.h>`

Inherits from [hybridse::vm::RowHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_row_handler.md), [hybridse::vm::DataHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md), hybridse::codec::ListV< Row >

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[ErrorRowHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_error_row_handler.md#function-errorrowhandler)**(common::StatusCode status_code, const std::string & msg_str) |
| | **[~ErrorRowHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_error_row_handler.md#function-~errorrowhandler)**() |
| virtual const Row & | **[GetValue](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_error_row_handler.md#function-getvalue)**() |
| virtual const std::string | **[GetHandlerTypeName](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_error_row_handler.md#function-gethandlertypename)**() override |
| virtual const Schema * | **[GetSchema](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_error_row_handler.md#function-getschema)**() override |
| virtual const std::string & | **[GetName](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_error_row_handler.md#function-getname)**() override |
| virtual const std::string & | **[GetDatabase](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_error_row_handler.md#function-getdatabase)**() override |
| virtual base::Status | **[GetStatus](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_error_row_handler.md#function-getstatus)**() |

## Additional inherited members

**Public Functions inherited from [hybridse::vm::RowHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_row_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[RowHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_row_handler.md#function-rowhandler)**() |
| virtual | **[~RowHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_row_handler.md#function-~rowhandler)**() |
| std::unique_ptr< RowIterator > | **[GetIterator](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_row_handler.md#function-getiterator)**() override |
| RowIterator * | **[GetRawIterator](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_row_handler.md#function-getrawiterator)**() override |
| const uint64_t | **[GetCount](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_row_handler.md#function-getcount)**() override |
| Row | **[At](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_row_handler.md#function-at)**(uint64_t pos) override |
| virtual const [HandlerType](/hybridse/usage/api/markdownNamespaces/namespacehybridse_1_1vm.md#enum-handlertype) | **[GetHanlderType](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_row_handler.md#function-gethanldertype)**() override |

**Public Functions inherited from [hybridse::vm::DataHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[DataHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md#function-datahandler)**() |
| virtual | **[~DataHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md#function-~datahandler)**() |
| virtual const [HandlerType](/hybridse/usage/api/markdownNamespaces/namespacehybridse_1_1vm.md#enum-handlertype) | **[GetHanlderType](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md#function-gethanldertype)**() =0 |


## Public Functions Documentation

### function ErrorRowHandler

```cpp
inline ErrorRowHandler(
    common::StatusCode status_code,
    const std::string & msg_str
)
```


### function ~ErrorRowHandler

```cpp
inline ~ErrorRowHandler()
```


### function GetValue

```cpp
inline virtual const Row & GetValue()
```


**Reimplements**: [hybridse::vm::RowHandler::GetValue](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_row_handler.md#function-getvalue)


### function GetHandlerTypeName

```cpp
inline virtual const std::string GetHandlerTypeName() override
```


**Return**: 

**Reimplements**: [hybridse::vm::RowHandler::GetHandlerTypeName](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_row_handler.md#function-gethandlertypename)


Implemented by subclasses return the name of handler type 


### function GetSchema

```cpp
inline virtual const Schema * GetSchema() override
```


**Return**: 

**Reimplements**: [hybridse::vm::DataHandler::GetSchema](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md#function-getschema)


Implemented by subclasses to return table schema. 


### function GetName

```cpp
inline virtual const std::string & GetName() override
```


**Return**: 

**Reimplements**: [hybridse::vm::DataHandler::GetName](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md#function-getname)


Implemented by subclasses to return table name. 


### function GetDatabase

```cpp
inline virtual const std::string & GetDatabase() override
```


**Return**: 

**Reimplements**: [hybridse::vm::DataHandler::GetDatabase](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md#function-getdatabase)


Implemented by subclasses to return the name of database. 


### function GetStatus

```cpp
inline virtual base::Status GetStatus()
```


**Return**: 

**Reimplements**: [hybridse::vm::DataHandler::GetStatus](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md#function-getstatus)


Return dataset status. Default is hybridse::common::kOk 


-------------------------------

Updated on 28 March 2021 at 19:34:48 PDT