---
title: hybridse::vm::MemTableHandler

---

# hybridse::vm::MemTableHandler




`#include <mem_catalog.h>`

Inherits from [hybridse::vm::TableHandler](/Classes/classhybridse_1_1vm_1_1_table_handler.md), [hybridse::vm::DataHandler](/Classes/classhybridse_1_1vm_1_1_data_handler.md), hybridse::codec::ListV< Row >

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[MemTableHandler](/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-memtablehandler)**() |
| | **[MemTableHandler](/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-memtablehandler)**(const Schema * schema) |
| | **[MemTableHandler](/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-memtablehandler)**(const std::string & table_name, const std::string & db, const Schema * schema) |
| | **[~MemTableHandler](/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-~memtablehandler)**() override |
| virtual const [Types](/Namespaces/namespacehybridse_1_1vm.md#typedef-types) & | **[GetTypes](/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-gettypes)**() override |
| virtual const Schema * | **[GetSchema](/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getschema)**() |
| virtual const std::string & | **[GetName](/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getname)**() |
| virtual const [IndexHint](/Namespaces/namespacehybridse_1_1vm.md#typedef-indexhint) & | **[GetIndex](/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getindex)**() |
| virtual const std::string & | **[GetDatabase](/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getdatabase)**() |
| std::unique_ptr< RowIterator > | **[GetIterator](/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getiterator)**() override |
| RowIterator * | **[GetRawIterator](/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getrawiterator)**() override |
| virtual std::unique_ptr< WindowIterator > | **[GetWindowIterator](/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getwindowiterator)**(const std::string & idx_name) |
| void | **[AddRow](/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-addrow)**(const Row & row) |
| void | **[Reverse](/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-reverse)**() |
| virtual const uint64_t | **[GetCount](/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getcount)**() |
| virtual Row | **[At](/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-at)**(uint64_t pos) |
| virtual const [OrderType](/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype) | **[GetOrderType](/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getordertype)**() const |
| void | **[SetOrderType](/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-setordertype)**(const [OrderType](/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype) order_type) |
| virtual const std::string | **[GetHandlerTypeName](/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-gethandlertypename)**() override |

## Protected Functions

|                | Name           |
| -------------- | -------------- |
| void | **[Resize](/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-resize)**(const size_t size) |
| bool | **[SetRow](/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-setrow)**(const size_t idx, const Row & row) |

## Protected Attributes

|                | Name           |
| -------------- | -------------- |
| const std::string | **[table_name_](/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#variable-table_name_)**  |
| const std::string | **[db_](/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#variable-db_)**  |
| const Schema * | **[schema_](/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#variable-schema_)**  |
| [Types](/Namespaces/namespacehybridse_1_1vm.md#typedef-types) | **[types_](/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#variable-types_)**  |
| [IndexHint](/Namespaces/namespacehybridse_1_1vm.md#typedef-indexhint) | **[index_hint_](/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#variable-index_hint_)**  |
| [MemTable](/Namespaces/namespacehybridse_1_1vm.md#typedef-memtable) | **[table_](/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#variable-table_)**  |
| [OrderType](/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype) | **[order_type_](/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#variable-order_type_)**  |

## Additional inherited members

**Public Functions inherited from [hybridse::vm::TableHandler](/Classes/classhybridse_1_1vm_1_1_table_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[TableHandler](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-tablehandler)**() |
| virtual | **[~TableHandler](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-~tablehandler)**() |
| virtual const [HandlerType](/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) | **[GetHanlderType](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gethanldertype)**() override |
| virtual std::shared_ptr< [PartitionHandler](/Classes/classhybridse_1_1vm_1_1_partition_handler.md) > | **[GetPartition](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getpartition)**(const std::string & index_name) |
| virtual std::shared_ptr< [Tablet](/Classes/classhybridse_1_1vm_1_1_tablet.md) > | **[GetTablet](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettablet)**(const std::string & index_name, const std::string & pk) |
| virtual std::shared_ptr< [Tablet](/Classes/classhybridse_1_1vm_1_1_tablet.md) > | **[GetTablet](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettablet)**(const std::string & index_name, const std::vector< std::string > & pks) |

**Public Functions inherited from [hybridse::vm::DataHandler](/Classes/classhybridse_1_1vm_1_1_data_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[DataHandler](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-datahandler)**() |
| virtual | **[~DataHandler](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-~datahandler)**() |
| virtual const [HandlerType](/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) | **[GetHanlderType](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethanldertype)**() =0 |
| virtual base::Status | **[GetStatus](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getstatus)**() |


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


**Reimplements**: [hybridse::vm::TableHandler::GetTypes](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettypes)


### function GetSchema

```cpp
inline virtual const Schema * GetSchema()
```


**Return**: 

**Reimplements**: [hybridse::vm::DataHandler::GetSchema](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getschema)


Implemented by subclasses to return table schema. 


### function GetName

```cpp
inline virtual const std::string & GetName()
```


**Return**: 

**Reimplements**: [hybridse::vm::DataHandler::GetName](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getname)


Implemented by subclasses to return table name. 


### function GetIndex

```cpp
inline virtual const IndexHint & GetIndex()
```


**Reimplements**: [hybridse::vm::TableHandler::GetIndex](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getindex)


### function GetDatabase

```cpp
inline virtual const std::string & GetDatabase()
```


**Return**: 

**Reimplements**: [hybridse::vm::DataHandler::GetDatabase](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getdatabase)


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


**Reimplements**: [hybridse::vm::TableHandler::GetWindowIterator](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getwindowiterator)


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


**Reimplements**: [hybridse::vm::TableHandler::GetOrderType](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getordertype)


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

**Reimplements**: [hybridse::vm::TableHandler::GetHandlerTypeName](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gethandlertypename)


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

Updated on 28 March 2021 at 19:23:48 PDT