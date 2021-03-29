---
title: hybridse::vm::ErrorTableHandler

---

# hybridse::vm::ErrorTableHandler




`#include <catalog.h>`

Inherits from [hybridse::vm::TableHandler](/Classes/classhybridse_1_1vm_1_1_table_handler.md), [hybridse::vm::DataHandler](/Classes/classhybridse_1_1vm_1_1_data_handler.md), hybridse::codec::ListV< Row >

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[ErrorTableHandler](/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-errortablehandler)**() |
| | **[ErrorTableHandler](/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-errortablehandler)**(common::StatusCode status_code, const std::string & msg_str) |
| | **[~ErrorTableHandler](/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-~errortablehandler)**() |
| virtual const [Types](/Namespaces/namespacehybridse_1_1vm.md#typedef-types) & | **[GetTypes](/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-gettypes)**() override |
| virtual const Schema * | **[GetSchema](/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-getschema)**() override |
| virtual const std::string & | **[GetName](/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-getname)**() override |
| virtual const [IndexHint](/Namespaces/namespacehybridse_1_1vm.md#typedef-indexhint) & | **[GetIndex](/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-getindex)**() override |
| virtual const std::string & | **[GetDatabase](/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-getdatabase)**() override |
| std::unique_ptr< RowIterator > | **[GetIterator](/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-getiterator)**() |
| RowIterator * | **[GetRawIterator](/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-getrawiterator)**() |
| virtual std::unique_ptr< WindowIterator > | **[GetWindowIterator](/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-getwindowiterator)**(const std::string & idx_name) |
| virtual Row | **[At](/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-at)**(uint64_t pos) |
| const uint64_t | **[GetCount](/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-getcount)**() override |
| virtual const std::string | **[GetHandlerTypeName](/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-gethandlertypename)**() override |
| virtual base::Status | **[GetStatus](/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-getstatus)**() |

## Protected Attributes

|                | Name           |
| -------------- | -------------- |
| base::Status | **[status_](/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#variable-status_)**  |
| const std::string | **[table_name_](/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#variable-table_name_)**  |
| const std::string | **[db_](/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#variable-db_)**  |
| const Schema * | **[schema_](/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#variable-schema_)**  |
| [Types](/Namespaces/namespacehybridse_1_1vm.md#typedef-types) | **[types_](/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#variable-types_)**  |
| [IndexHint](/Namespaces/namespacehybridse_1_1vm.md#typedef-indexhint) | **[index_hint_](/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#variable-index_hint_)**  |
| [OrderType](/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype) | **[order_type_](/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#variable-order_type_)**  |

## Additional inherited members

**Public Functions inherited from [hybridse::vm::TableHandler](/Classes/classhybridse_1_1vm_1_1_table_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[TableHandler](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-tablehandler)**() |
| virtual | **[~TableHandler](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-~tablehandler)**() |
| virtual const [HandlerType](/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) | **[GetHanlderType](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gethanldertype)**() override |
| virtual std::shared_ptr< [PartitionHandler](/Classes/classhybridse_1_1vm_1_1_partition_handler.md) > | **[GetPartition](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getpartition)**(const std::string & index_name) |
| virtual const [OrderType](/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype) | **[GetOrderType](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getordertype)**() const |
| virtual std::shared_ptr< [Tablet](/Classes/classhybridse_1_1vm_1_1_tablet.md) > | **[GetTablet](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettablet)**(const std::string & index_name, const std::string & pk) |
| virtual std::shared_ptr< [Tablet](/Classes/classhybridse_1_1vm_1_1_tablet.md) > | **[GetTablet](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettablet)**(const std::string & index_name, const std::vector< std::string > & pks) |

**Public Functions inherited from [hybridse::vm::DataHandler](/Classes/classhybridse_1_1vm_1_1_data_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[DataHandler](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-datahandler)**() |
| virtual | **[~DataHandler](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-~datahandler)**() |
| virtual const [HandlerType](/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) | **[GetHanlderType](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethanldertype)**() =0 |


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


**Reimplements**: [hybridse::vm::TableHandler::GetTypes](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettypes)


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


### function GetIndex

```cpp
inline virtual const IndexHint & GetIndex() override
```


**Reimplements**: [hybridse::vm::TableHandler::GetIndex](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getindex)


### function GetDatabase

```cpp
inline virtual const std::string & GetDatabase() override
```


**Return**: 

**Reimplements**: [hybridse::vm::DataHandler::GetDatabase](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getdatabase)


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


**Reimplements**: [hybridse::vm::TableHandler::GetWindowIterator](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getwindowiterator)


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

**Reimplements**: [hybridse::vm::TableHandler::GetHandlerTypeName](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gethandlertypename)


Implemented by subclasses return the name of handler type 


### function GetStatus

```cpp
inline virtual base::Status GetStatus()
```


**Return**: 

**Reimplements**: [hybridse::vm::DataHandler::GetStatus](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getstatus)


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

Updated on 28 March 2021 at 19:23:48 PDT