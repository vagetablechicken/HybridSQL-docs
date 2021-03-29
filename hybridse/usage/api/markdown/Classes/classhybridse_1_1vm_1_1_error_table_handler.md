---
title: hybridse::vm::ErrorTableHandler

---

# hybridse::vm::ErrorTableHandler




`#include <catalog.h>`

Inherits from [hybridse::vm::TableHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_table_handler.md), [hybridse::vm::DataHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md), hybridse::codec::ListV< Row >

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[ErrorTableHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_error_table_handler.md#function-errortablehandler)**() |
| | **[ErrorTableHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_error_table_handler.md#function-errortablehandler)**(common::StatusCode status_code, const std::string & msg_str) |
| | **[~ErrorTableHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_error_table_handler.md#function-~errortablehandler)**() |
| virtual const [Types](/hybridse/usage/api/markdownNamespaces/namespacehybridse_1_1vm.md#typedef-types) & | **[GetTypes](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_error_table_handler.md#function-gettypes)**() override |
| virtual const Schema * | **[GetSchema](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_error_table_handler.md#function-getschema)**() override |
| virtual const std::string & | **[GetName](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_error_table_handler.md#function-getname)**() override |
| virtual const [IndexHint](/hybridse/usage/api/markdownNamespaces/namespacehybridse_1_1vm.md#typedef-indexhint) & | **[GetIndex](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_error_table_handler.md#function-getindex)**() override |
| virtual const std::string & | **[GetDatabase](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_error_table_handler.md#function-getdatabase)**() override |
| std::unique_ptr< RowIterator > | **[GetIterator](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_error_table_handler.md#function-getiterator)**() |
| RowIterator * | **[GetRawIterator](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_error_table_handler.md#function-getrawiterator)**() |
| virtual std::unique_ptr< WindowIterator > | **[GetWindowIterator](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_error_table_handler.md#function-getwindowiterator)**(const std::string & idx_name) |
| virtual Row | **[At](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_error_table_handler.md#function-at)**(uint64_t pos) |
| const uint64_t | **[GetCount](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_error_table_handler.md#function-getcount)**() override |
| virtual const std::string | **[GetHandlerTypeName](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_error_table_handler.md#function-gethandlertypename)**() override |
| virtual base::Status | **[GetStatus](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_error_table_handler.md#function-getstatus)**() |

## Protected Attributes

|                | Name           |
| -------------- | -------------- |
| base::Status | **[status_](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_error_table_handler.md#variable-status_)**  |
| const std::string | **[table_name_](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_error_table_handler.md#variable-table_name_)**  |
| const std::string | **[db_](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_error_table_handler.md#variable-db_)**  |
| const Schema * | **[schema_](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_error_table_handler.md#variable-schema_)**  |
| [Types](/hybridse/usage/api/markdownNamespaces/namespacehybridse_1_1vm.md#typedef-types) | **[types_](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_error_table_handler.md#variable-types_)**  |
| [IndexHint](/hybridse/usage/api/markdownNamespaces/namespacehybridse_1_1vm.md#typedef-indexhint) | **[index_hint_](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_error_table_handler.md#variable-index_hint_)**  |
| [OrderType](/hybridse/usage/api/markdownNamespaces/namespacehybridse_1_1vm.md#enum-ordertype) | **[order_type_](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_error_table_handler.md#variable-order_type_)**  |

## Additional inherited members

**Public Functions inherited from [hybridse::vm::TableHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_table_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[TableHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_table_handler.md#function-tablehandler)**() |
| virtual | **[~TableHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_table_handler.md#function-~tablehandler)**() |
| virtual const [HandlerType](/hybridse/usage/api/markdownNamespaces/namespacehybridse_1_1vm.md#enum-handlertype) | **[GetHanlderType](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_table_handler.md#function-gethanldertype)**() override |
| virtual std::shared_ptr< [PartitionHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_partition_handler.md) > | **[GetPartition](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_table_handler.md#function-getpartition)**(const std::string & index_name) |
| virtual const [OrderType](/hybridse/usage/api/markdownNamespaces/namespacehybridse_1_1vm.md#enum-ordertype) | **[GetOrderType](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_table_handler.md#function-getordertype)**() const |
| virtual std::shared_ptr< [Tablet](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_tablet.md) > | **[GetTablet](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_table_handler.md#function-gettablet)**(const std::string & index_name, const std::string & pk) |
| virtual std::shared_ptr< [Tablet](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_tablet.md) > | **[GetTablet](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_table_handler.md#function-gettablet)**(const std::string & index_name, const std::vector< std::string > & pks) |

**Public Functions inherited from [hybridse::vm::DataHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[DataHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md#function-datahandler)**() |
| virtual | **[~DataHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md#function-~datahandler)**() |
| virtual const [HandlerType](/hybridse/usage/api/markdownNamespaces/namespacehybridse_1_1vm.md#enum-handlertype) | **[GetHanlderType](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md#function-gethanldertype)**() =0 |


## Public Functions Documentation

### function ErrorTableHandler

```cpp
inline ErrorTableHandler()
```


### function ErrorTableHandler

```cpp
inline ErrorTableHandler(
    common::StatusCode status_code,
    const std::string & msg_str
)
```


### function ~ErrorTableHandler

```cpp
inline ~ErrorTableHandler()
```


### function GetTypes

```cpp
inline virtual const Types & GetTypes() override
```


**Reimplements**: [hybridse::vm::TableHandler::GetTypes](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_table_handler.md#function-gettypes)


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


### function GetIndex

```cpp
inline virtual const IndexHint & GetIndex() override
```


**Reimplements**: [hybridse::vm::TableHandler::GetIndex](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_table_handler.md#function-getindex)


### function GetDatabase

```cpp
inline virtual const std::string & GetDatabase() override
```


**Return**: 

**Reimplements**: [hybridse::vm::DataHandler::GetDatabase](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md#function-getdatabase)


Implemented by subclasses to return the name of database. 


### function GetIterator

```cpp
inline std::unique_ptr< RowIterator > GetIterator()
```


### function GetRawIterator

```cpp
inline RowIterator * GetRawIterator()
```


### function GetWindowIterator

```cpp
inline virtual std::unique_ptr< WindowIterator > GetWindowIterator(
    const std::string & idx_name
)
```


**Reimplements**: [hybridse::vm::TableHandler::GetWindowIterator](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_table_handler.md#function-getwindowiterator)


### function At

```cpp
inline virtual Row At(
    uint64_t pos
)
```


### function GetCount

```cpp
inline const uint64_t GetCount() override
```


### function GetHandlerTypeName

```cpp
inline virtual const std::string GetHandlerTypeName() override
```


**Return**: 

**Reimplements**: [hybridse::vm::TableHandler::GetHandlerTypeName](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_table_handler.md#function-gethandlertypename)


Implemented by subclasses return the name of handler type 


### function GetStatus

```cpp
inline virtual base::Status GetStatus()
```


**Return**: 

**Reimplements**: [hybridse::vm::DataHandler::GetStatus](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md#function-getstatus)


Return dataset status. Default is hybridse::common::kOk 


## Protected Attributes Documentation

### variable status_

```cpp
base::Status status_;
```


### variable table_name_

```cpp
const std::string table_name_;
```


### variable db_

```cpp
const std::string db_;
```


### variable schema_

```cpp
const Schema * schema_;
```


### variable types_

```cpp
Types types_;
```


### variable index_hint_

```cpp
IndexHint index_hint_;
```


### variable order_type_

```cpp
OrderType order_type_;
```


-------------------------------

Updated on 28 March 2021 at 19:34:48 PDT