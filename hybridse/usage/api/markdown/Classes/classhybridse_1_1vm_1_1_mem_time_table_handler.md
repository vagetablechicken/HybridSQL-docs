---
title: hybridse::vm::MemTimeTableHandler

---

# hybridse::vm::MemTimeTableHandler




`#include <mem_catalog.h>`

Inherits from [hybridse::vm::TableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md), [hybridse::vm::DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md), hybridse::codec::ListV< Row >

Inherited by [hybridse::vm::ConcatTableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_concat_table_handler.md), [hybridse::vm::Window](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md)

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[MemTimeTableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-memtimetablehandler)**() |
| | **[MemTimeTableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-memtimetablehandler)**(const Schema * schema) |
| | **[MemTimeTableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-memtimetablehandler)**(const std::string & table_name, const std::string & db, const Schema * schema) |
| virtual const [Types](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#typedef-types) & | **[GetTypes](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-gettypes)**() override |
| | **[~MemTimeTableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-~memtimetablehandler)**() override |
| virtual const Schema * | **[GetSchema](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getschema)**() |
| virtual const std::string & | **[GetName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getname)**() |
| virtual const [IndexHint](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#typedef-indexhint) & | **[GetIndex](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getindex)**() |
| std::unique_ptr< RowIterator > | **[GetIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getiterator)**() |
| RowIterator * | **[GetRawIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getrawiterator)**() |
| virtual const std::string & | **[GetDatabase](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getdatabase)**() |
| virtual std::unique_ptr< WindowIterator > | **[GetWindowIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getwindowiterator)**(const std::string & idx_name) |
| void | **[AddRow](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-addrow)**(const uint64_t key, const Row & v) |
| void | **[AddFrontRow](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-addfrontrow)**(const uint64_t key, const Row & v) |
| void | **[PopBackRow](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-popbackrow)**() |
| void | **[PopFrontRow](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-popfrontrow)**() |
| virtual const std::pair< uint64_t, Row > & | **[GetFrontRow](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getfrontrow)**() |
| virtual const std::pair< uint64_t, Row > & | **[GetBackRow](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getbackrow)**() |
| void | **[Sort](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-sort)**(const bool is_asc) |
| void | **[Reverse](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-reverse)**() |
| virtual const uint64_t | **[GetCount](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getcount)**() |
| virtual Row | **[At](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-at)**(uint64_t pos) |
| void | **[SetOrderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-setordertype)**(const [OrderType](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype) order_type) |
| virtual const [OrderType](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype) | **[GetOrderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getordertype)**() const |
| virtual const std::string | **[GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-gethandlertypename)**() override |

## Protected Attributes

|                | Name           |
| -------------- | -------------- |
| const std::string | **[table_name_](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-table_name_)**  |
| const std::string | **[db_](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-db_)**  |
| const Schema * | **[schema_](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-schema_)**  |
| [Types](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#typedef-types) | **[types_](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-types_)**  |
| [IndexHint](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#typedef-indexhint) | **[index_hint_](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-index_hint_)**  |
| [MemTimeTable](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#typedef-memtimetable) | **[table_](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-table_)**  |
| [OrderType](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype) | **[order_type_](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-order_type_)**  |

## Additional inherited members

**Public Functions inherited from [hybridse::vm::TableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[TableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-tablehandler)**() |
| virtual | **[~TableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-~tablehandler)**() |
| virtual const [HandlerType](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) | **[GetHanlderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gethanldertype)**() override |
| virtual std::shared_ptr< [PartitionHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md) > | **[GetPartition](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getpartition)**(const std::string & index_name) |
| virtual std::shared_ptr< [Tablet](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_tablet.md) > | **[GetTablet](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettablet)**(const std::string & index_name, const std::string & pk) |
| virtual std::shared_ptr< [Tablet](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_tablet.md) > | **[GetTablet](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettablet)**(const std::string & index_name, const std::vector< std::string > & pks) |

**Public Functions inherited from [hybridse::vm::DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-datahandler)**() |
| virtual | **[~DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-~datahandler)**() |
| virtual const [HandlerType](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) | **[GetHanlderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethanldertype)**() =0 |
| virtual base::Status | **[GetStatus](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getstatus)**() |


## Public Functions Documentation

### function MemTimeTableHandler

```cpp
MemTimeTableHandler()
```


### function MemTimeTableHandler

```cpp
explicit MemTimeTableHandler(
    const Schema * schema
)
```


### function MemTimeTableHandler

```cpp
MemTimeTableHandler(
    const std::string & table_name,
    const std::string & db,
    const Schema * schema
)
```


### function GetTypes

```cpp
virtual const Types & GetTypes() override
```


**Reimplements**: [hybridse::vm::TableHandler::GetTypes](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettypes)


### function ~MemTimeTableHandler

```cpp
~MemTimeTableHandler() override
```


### function GetSchema

```cpp
inline virtual const Schema * GetSchema()
```


**Return**: 

**Reimplements**: [hybridse::vm::DataHandler::GetSchema](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getschema)


Implemented by subclasses to return table schema. 


### function GetName

```cpp
inline virtual const std::string & GetName()
```


**Return**: 

**Reimplements**: [hybridse::vm::DataHandler::GetName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getname)


Implemented by subclasses to return table name. 


### function GetIndex

```cpp
inline virtual const IndexHint & GetIndex()
```


**Reimplements**: [hybridse::vm::TableHandler::GetIndex](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getindex)


### function GetIterator

```cpp
std::unique_ptr< RowIterator > GetIterator()
```


### function GetRawIterator

```cpp
RowIterator * GetRawIterator()
```


### function GetDatabase

```cpp
inline virtual const std::string & GetDatabase()
```


**Return**: 

**Reimplements**: [hybridse::vm::DataHandler::GetDatabase](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getdatabase)


Implemented by subclasses to return the name of database. 


### function GetWindowIterator

```cpp
virtual std::unique_ptr< WindowIterator > GetWindowIterator(
    const std::string & idx_name
)
```


**Reimplements**: [hybridse::vm::TableHandler::GetWindowIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getwindowiterator)


### function AddRow

```cpp
void AddRow(
    const uint64_t key,
    const Row & v
)
```


### function AddFrontRow

```cpp
void AddFrontRow(
    const uint64_t key,
    const Row & v
)
```


### function PopBackRow

```cpp
void PopBackRow()
```


### function PopFrontRow

```cpp
void PopFrontRow()
```


### function GetFrontRow

```cpp
inline virtual const std::pair< uint64_t, Row > & GetFrontRow()
```


### function GetBackRow

```cpp
inline virtual const std::pair< uint64_t, Row > & GetBackRow()
```


### function Sort

```cpp
void Sort(
    const bool is_asc
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


**Reimplemented by**: [hybridse::vm::Window::GetCount](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#function-getcount), [hybridse::vm::ConcatTableHandler::GetCount](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_concat_table_handler.md#function-getcount)


### function At

```cpp
inline virtual Row At(
    uint64_t pos
)
```


**Reimplemented by**: [hybridse::vm::Window::At](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#function-at), [hybridse::vm::ConcatTableHandler::At](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_concat_table_handler.md#function-at)


### function SetOrderType

```cpp
inline void SetOrderType(
    const OrderType order_type
)
```


### function GetOrderType

```cpp
inline virtual const OrderType GetOrderType() const
```


**Reimplements**: [hybridse::vm::TableHandler::GetOrderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getordertype)


### function GetHandlerTypeName

```cpp
inline virtual const std::string GetHandlerTypeName() override
```


**Return**: 

**Reimplements**: [hybridse::vm::TableHandler::GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gethandlertypename)


**Reimplemented by**: [hybridse::vm::Window::GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#function-gethandlertypename)


Implemented by subclasses return the name of handler type 


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
MemTimeTable table_;
```


### variable order_type_

```cpp
OrderType order_type_;
```


-------------------------------

Updated on 28 March 2021 at 19:41:19 PDT