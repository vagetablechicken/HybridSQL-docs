---
title: hybridse::vm::AysncRowHandler

---

# hybridse::vm::AysncRowHandler




`#include <catalog.h>`

Inherits from [hybridse::vm::RowHandler](/Classes/classhybridse_1_1vm_1_1_row_handler.md), [hybridse::vm::DataHandler](/Classes/classhybridse_1_1vm_1_1_data_handler.md), hybridse::codec::ListV< Row >

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[AysncRowHandler](/Classes/classhybridse_1_1vm_1_1_aysnc_row_handler.md#function-aysncrowhandler)**(size_t idx, std::shared_ptr< [TableHandler](/Classes/classhybridse_1_1vm_1_1_table_handler.md) > aysnc_table_handler) |
| virtual | **[~AysncRowHandler](/Classes/classhybridse_1_1vm_1_1_aysnc_row_handler.md#function-~aysncrowhandler)**() |
| virtual const Row & | **[GetValue](/Classes/classhybridse_1_1vm_1_1_aysnc_row_handler.md#function-getvalue)**() override |
| virtual const Schema * | **[GetSchema](/Classes/classhybridse_1_1vm_1_1_aysnc_row_handler.md#function-getschema)**() override |
| virtual const std::string & | **[GetName](/Classes/classhybridse_1_1vm_1_1_aysnc_row_handler.md#function-getname)**() override |
| virtual const std::string & | **[GetDatabase](/Classes/classhybridse_1_1vm_1_1_aysnc_row_handler.md#function-getdatabase)**() override |

## Public Attributes

|                | Name           |
| -------------- | -------------- |
| base::Status | **[status_](/Classes/classhybridse_1_1vm_1_1_aysnc_row_handler.md#variable-status_)**  |
| std::string | **[table_name_](/Classes/classhybridse_1_1vm_1_1_aysnc_row_handler.md#variable-table_name_)**  |
| std::string | **[db_](/Classes/classhybridse_1_1vm_1_1_aysnc_row_handler.md#variable-db_)**  |
| const Schema * | **[schema_](/Classes/classhybridse_1_1vm_1_1_aysnc_row_handler.md#variable-schema_)**  |
| size_t | **[idx_](/Classes/classhybridse_1_1vm_1_1_aysnc_row_handler.md#variable-idx_)**  |
| std::shared_ptr< [TableHandler](/Classes/classhybridse_1_1vm_1_1_table_handler.md) > | **[aysnc_table_handler_](/Classes/classhybridse_1_1vm_1_1_aysnc_row_handler.md#variable-aysnc_table_handler_)**  |
| Row | **[value_](/Classes/classhybridse_1_1vm_1_1_aysnc_row_handler.md#variable-value_)**  |

## Additional inherited members

**Public Functions inherited from [hybridse::vm::RowHandler](/Classes/classhybridse_1_1vm_1_1_row_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[RowHandler](/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-rowhandler)**() |
| virtual | **[~RowHandler](/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-~rowhandler)**() |
| std::unique_ptr< RowIterator > | **[GetIterator](/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-getiterator)**() override |
| RowIterator * | **[GetRawIterator](/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-getrawiterator)**() override |
| const uint64_t | **[GetCount](/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-getcount)**() override |
| Row | **[At](/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-at)**(uint64_t pos) override |
| virtual const [HandlerType](/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) | **[GetHanlderType](/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-gethanldertype)**() override |
| virtual const std::string | **[GetHandlerTypeName](/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-gethandlertypename)**() override |

**Public Functions inherited from [hybridse::vm::DataHandler](/Classes/classhybridse_1_1vm_1_1_data_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[DataHandler](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-datahandler)**() |
| virtual | **[~DataHandler](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-~datahandler)**() |
| virtual const [HandlerType](/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) | **[GetHanlderType](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethanldertype)**() =0 |
| virtual const std::string | **[GetHandlerTypeName](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethandlertypename)**() =0 |
| virtual base::Status | **[GetStatus](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getstatus)**() |


## Public Functions Documentation

### function AysncRowHandler

```cpp
inline AysncRowHandler(
    size_t idx,
    std::shared_ptr< TableHandler > aysnc_table_handler
)
```


### function ~AysncRowHandler

```cpp
inline virtual ~AysncRowHandler()
```


### function GetValue

```cpp
inline virtual const Row & GetValue() override
```


**Reimplements**: [hybridse::vm::RowHandler::GetValue](/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-getvalue)


### function GetSchema

```cpp
inline virtual const Schema * GetSchema() override
```


**Return**: 

**Reimplements**: [hybridse::vm::DataHandler::GetSchema](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getschema)


Implemented by subclasses to return table schema. 


### function GetName

```cpp
inline virtual const std::string & GetName() override
```


**Return**: 

**Reimplements**: [hybridse::vm::DataHandler::GetName](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getname)


Implemented by subclasses to return table name. 


### function GetDatabase

```cpp
inline virtual const std::string & GetDatabase() override
```


**Return**: 

**Reimplements**: [hybridse::vm::DataHandler::GetDatabase](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getdatabase)


Implemented by subclasses to return the name of database. 


## Public Attributes Documentation

### variable status_

```cpp
base::Status status_;
```


### variable table_name_

```cpp
std::string table_name_;
```


### variable db_

```cpp
std::string db_;
```


### variable schema_

```cpp
const Schema * schema_;
```


### variable idx_

```cpp
size_t idx_;
```


### variable aysnc_table_handler_

```cpp
std::shared_ptr< TableHandler > aysnc_table_handler_;
```


### variable value_

```cpp
Row value_;
```


-------------------------------

Updated on 28 March 2021 at 19:23:48 PDT