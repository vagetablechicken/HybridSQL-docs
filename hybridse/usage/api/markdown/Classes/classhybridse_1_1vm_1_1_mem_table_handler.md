---
title: hybridse::vm::MemTableHandler

---

# hybridse::vm::MemTableHandler




`#include <mem_catalog.h>`

Inherits from [hybridse::vm::TableHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_table_handler.md), [hybridse::vm::DataHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md), hybridse::codec::ListV< Row >

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[MemTableHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_table_handler.md#function-memtablehandler)**() |
| | **[MemTableHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_table_handler.md#function-memtablehandler)**(const Schema * schema) |
| | **[MemTableHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_table_handler.md#function-memtablehandler)**(const std::string & table_name, const std::string & db, const Schema * schema) |
| | **[~MemTableHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_table_handler.md#function-~memtablehandler)**() override |
| virtual const [Types](/hybridse/usage/api/markdownNamespaces/namespacehybridse_1_1vm.md#typedef-types) & | **[GetTypes](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_table_handler.md#function-gettypes)**() override |
| virtual const Schema * | **[GetSchema](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getschema)**() |
| virtual const std::string & | **[GetName](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getname)**() |
| virtual const [IndexHint](/hybridse/usage/api/markdownNamespaces/namespacehybridse_1_1vm.md#typedef-indexhint) & | **[GetIndex](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getindex)**() |
| virtual const std::string & | **[GetDatabase](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getdatabase)**() |
| std::unique_ptr< RowIterator > | **[GetIterator](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getiterator)**() override |
| RowIterator * | **[GetRawIterator](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getrawiterator)**() override |
| virtual std::unique_ptr< WindowIterator > | **[GetWindowIterator](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getwindowiterator)**(const std::string & idx_name) |
| void | **[AddRow](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_table_handler.md#function-addrow)**(const Row & row) |
| void | **[Reverse](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_table_handler.md#function-reverse)**() |
| virtual const uint64_t | **[GetCount](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getcount)**() |
| virtual Row | **[At](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_table_handler.md#function-at)**(uint64_t pos) |
| virtual const [OrderType](/hybridse/usage/api/markdownNamespaces/namespacehybridse_1_1vm.md#enum-ordertype) | **[GetOrderType](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getordertype)**() const |
| void | **[SetOrderType](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_table_handler.md#function-setordertype)**(const [OrderType](/hybridse/usage/api/markdownNamespaces/namespacehybridse_1_1vm.md#enum-ordertype) order_type) |
| virtual const std::string | **[GetHandlerTypeName](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_table_handler.md#function-gethandlertypename)**() override |

## Protected Functions

|                | Name           |
| -------------- | -------------- |
| void | **[Resize](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_table_handler.md#function-resize)**(const size_t size) |
| bool | **[SetRow](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_table_handler.md#function-setrow)**(const size_t idx, const Row & row) |

## Protected Attributes

|                | Name           |
| -------------- | -------------- |
| const std::string | **[table_name_](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_table_handler.md#variable-table_name_)**  |
| const std::string | **[db_](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_table_handler.md#variable-db_)**  |
| const Schema * | **[schema_](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_table_handler.md#variable-schema_)**  |
| [Types](/hybridse/usage/api/markdownNamespaces/namespacehybridse_1_1vm.md#typedef-types) | **[types_](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_table_handler.md#variable-types_)**  |
| [IndexHint](/hybridse/usage/api/markdownNamespaces/namespacehybridse_1_1vm.md#typedef-indexhint) | **[index_hint_](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_table_handler.md#variable-index_hint_)**  |
| [MemTable](/hybridse/usage/api/markdownNamespaces/namespacehybridse_1_1vm.md#typedef-memtable) | **[table_](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_table_handler.md#variable-table_)**  |
| [OrderType](/hybridse/usage/api/markdownNamespaces/namespacehybridse_1_1vm.md#enum-ordertype) | **[order_type_](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_table_handler.md#variable-order_type_)**  |

## Additional inherited members

**Public Functions inherited from [hybridse::vm::TableHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_table_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[TableHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_table_handler.md#function-tablehandler)**() |
| virtual | **[~TableHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_table_handler.md#function-~tablehandler)**() |
| virtual const [HandlerType](/hybridse/usage/api/markdownNamespaces/namespacehybridse_1_1vm.md#enum-handlertype) | **[GetHanlderType](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_table_handler.md#function-gethanldertype)**() override |
| virtual std::shared_ptr< [PartitionHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_partition_handler.md) > | **[GetPartition](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_table_handler.md#function-getpartition)**(const std::string & index_name) |
| virtual std::shared_ptr< [Tablet](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_tablet.md) > | **[GetTablet](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_table_handler.md#function-gettablet)**(const std::string & index_name, const std::string & pk) |
| virtual std::shared_ptr< [Tablet](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_tablet.md) > | **[GetTablet](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_table_handler.md#function-gettablet)**(const std::string & index_name, const std::vector< std::string > & pks) |

**Public Functions inherited from [hybridse::vm::DataHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[DataHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md#function-datahandler)**() |
| virtual | **[~DataHandler](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md#function-~datahandler)**() |
| virtual const [HandlerType](/hybridse/usage/api/markdownNamespaces/namespacehybridse_1_1vm.md#enum-handlertype) | **[GetHanlderType](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md#function-gethanldertype)**() =0 |
| virtual base::Status | **[GetStatus](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md#function-getstatus)**() |


## Public Functions Documentation

### function MemTableHandler

```cpp
MemTableHandler()
```


### function MemTableHandler

```cpp
explicit MemTableHandler(
    const Schema * schema
)
```


### function MemTableHandler

```cpp
MemTableHandler(
    const std::string & table_name,
    const std::string & db,
    const Schema * schema
)
```


### function ~MemTableHandler

```cpp
~MemTableHandler() override
```


### function GetTypes

```cpp
inline virtual const Types & GetTypes() override
```


**Reimplements**: [hybridse::vm::TableHandler::GetTypes](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_table_handler.md#function-gettypes)


### function GetSchema

```cpp
inline virtual const Schema * GetSchema()
```


**Return**: 

**Reimplements**: [hybridse::vm::DataHandler::GetSchema](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md#function-getschema)


Implemented by subclasses to return table schema. 


### function GetName

```cpp
inline virtual const std::string & GetName()
```


**Return**: 

**Reimplements**: [hybridse::vm::DataHandler::GetName](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md#function-getname)


Implemented by subclasses to return table name. 


### function GetIndex

```cpp
inline virtual const IndexHint & GetIndex()
```


**Reimplements**: [hybridse::vm::TableHandler::GetIndex](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_table_handler.md#function-getindex)


### function GetDatabase

```cpp
inline virtual const std::string & GetDatabase()
```


**Return**: 

**Reimplements**: [hybridse::vm::DataHandler::GetDatabase](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_data_handler.md#function-getdatabase)


Implemented by subclasses to return the name of database. 


### function GetIterator

```cpp
std::unique_ptr< RowIterator > GetIterator() override
```


### function GetRawIterator

```cpp
RowIterator * GetRawIterator() override
```


### function GetWindowIterator

```cpp
virtual std::unique_ptr< WindowIterator > GetWindowIterator(
    const std::string & idx_name
)
```


**Reimplements**: [hybridse::vm::TableHandler::GetWindowIterator](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_table_handler.md#function-getwindowiterator)


### function AddRow

```cpp
void AddRow(
    const Row & row
)
```


### function Reverse

```cpp
void Reverse()
```


### function GetCount

```cpp
inline virtual const uint64_t GetCount()
```


### function At

```cpp
inline virtual Row At(
    uint64_t pos
)
```


### function GetOrderType

```cpp
inline virtual const OrderType GetOrderType() const
```


**Reimplements**: [hybridse::vm::TableHandler::GetOrderType](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_table_handler.md#function-getordertype)


### function SetOrderType

```cpp
inline void SetOrderType(
    const OrderType order_type
)
```


### function GetHandlerTypeName

```cpp
inline virtual const std::string GetHandlerTypeName() override
```


**Return**: 

**Reimplements**: [hybridse::vm::TableHandler::GetHandlerTypeName](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_table_handler.md#function-gethandlertypename)


Implemented by subclasses return the name of handler type 


## Protected Functions Documentation

### function Resize

```cpp
void Resize(
    const size_t size
)
```


### function SetRow

```cpp
bool SetRow(
    const size_t idx,
    const Row & row
)
```


## Protected Attributes Documentation

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


### variable table_

```cpp
MemTable table_;
```


### variable order_type_

```cpp
OrderType order_type_;
```


-------------------------------

Updated on 28 March 2021 at 19:34:49 PDT