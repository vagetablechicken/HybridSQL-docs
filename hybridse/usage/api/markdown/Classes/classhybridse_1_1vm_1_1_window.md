---
title: hybridse::vm::Window

---

# hybridse::vm::Window




`#include <mem_catalog.h>`

Inherits from [hybridse::vm::MemTimeTableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md), [hybridse::vm::TableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md), [hybridse::vm::DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md), hybridse::codec::ListV< Row >

Inherited by [hybridse::vm::HistoryWindow](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_history_window.md)

## Public Types

|                | Name           |
| -------------- | -------------- |
| enum| **[WindowFrameType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#enum-windowframetype)** { kFrameRows, kFrameRowsRange, kFrameRowsMergeRowsRange} |

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[Window](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#function-window)**() |
| virtual | **[~Window](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#function-~window)**() |
| std::unique_ptr< RowIterator > | **[GetIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#function-getiterator)**() override |
| RowIterator * | **[GetRawIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#function-getrawiterator)**() |
| virtual bool | **[BufferData](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#function-bufferdata)**(uint64_t key, const Row & row) =0 |
| virtual void | **[PopBackData](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#function-popbackdata)**() |
| virtual void | **[PopFrontData](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#function-popfrontdata)**() =0 |
| virtual const uint64_t | **[GetCount](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#function-getcount)**() |
| virtual Row | **[At](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#function-at)**(uint64_t pos) |
| virtual const std::string | **[GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#function-gethandlertypename)**() override |
| const bool | **[instance_not_in_window](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#function-instance_not_in_window)**() const |
| void | **[set_instance_not_in_window](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#function-set_instance_not_in_window)**(const bool flag) |
| const bool | **[exclude_current_time](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#function-exclude_current_time)**() const |
| void | **[set_exclude_current_time](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#function-set_exclude_current_time)**(const bool flag) |

## Protected Attributes

|                | Name           |
| -------------- | -------------- |
| bool | **[exclude_current_time_](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#variable-exclude_current_time_)**  |
| bool | **[instance_not_in_window_](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#variable-instance_not_in_window_)**  |

## Additional inherited members

**Public Functions inherited from [hybridse::vm::MemTimeTableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md)**

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
| void | **[SetOrderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-setordertype)**(const [OrderType](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype) order_type) |
| virtual const [OrderType](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype) | **[GetOrderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getordertype)**() const |

**Protected Attributes inherited from [hybridse::vm::MemTimeTableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md)**

|                | Name           |
| -------------- | -------------- |
| const std::string | **[table_name_](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-table_name_)**  |
| const std::string | **[db_](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-db_)**  |
| const Schema * | **[schema_](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-schema_)**  |
| [Types](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#typedef-types) | **[types_](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-types_)**  |
| [IndexHint](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#typedef-indexhint) | **[index_hint_](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-index_hint_)**  |
| [MemTimeTable](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#typedef-memtimetable) | **[table_](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-table_)**  |
| [OrderType](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype) | **[order_type_](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-order_type_)**  |

**Public Functions inherited from [hybridse::vm::TableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[TableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-tablehandler)**() |
| virtual | **[~TableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-~tablehandler)**() |
| virtual const [Types](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#typedef-types) & | **[GetTypes](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettypes)**() =0 |
| virtual const [IndexHint](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#typedef-indexhint) & | **[GetIndex](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getindex)**() =0 |
| virtual std::unique_ptr< WindowIterator > | **[GetWindowIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getwindowiterator)**(const std::string & idx_name) =0 |
| virtual const [HandlerType](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) | **[GetHanlderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gethanldertype)**() override |
| virtual std::shared_ptr< [PartitionHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md) > | **[GetPartition](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getpartition)**(const std::string & index_name) |
| virtual const [OrderType](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype) | **[GetOrderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getordertype)**() const |
| virtual std::shared_ptr< [Tablet](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_tablet.md) > | **[GetTablet](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettablet)**(const std::string & index_name, const std::string & pk) |
| virtual std::shared_ptr< [Tablet](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_tablet.md) > | **[GetTablet](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettablet)**(const std::string & index_name, const std::vector< std::string > & pks) |

**Public Functions inherited from [hybridse::vm::DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-datahandler)**() |
| virtual | **[~DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-~datahandler)**() |
| virtual const Schema * | **[GetSchema](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getschema)**() =0 |
| virtual const std::string & | **[GetName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getname)**() =0 |
| virtual const std::string & | **[GetDatabase](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getdatabase)**() =0 |
| virtual const [HandlerType](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) | **[GetHanlderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethanldertype)**() =0 |
| virtual base::Status | **[GetStatus](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getstatus)**() |


## Public Types Documentation

### enum WindowFrameType

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| kFrameRows | |   |
| kFrameRowsRange | |   |
| kFrameRowsMergeRowsRange | |   |




## Public Functions Documentation

### function Window

```cpp
inline Window()
```


### function ~Window

```cpp
inline virtual ~Window()
```


### function GetIterator

```cpp
inline std::unique_ptr< RowIterator > GetIterator() override
```


### function GetRawIterator

```cpp
inline RowIterator * GetRawIterator()
```


### function BufferData

```cpp
virtual bool BufferData(
    uint64_t key,
    const Row & row
) =0
```


**Reimplemented by**: [hybridse::vm::HistoryWindow::BufferData](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_history_window.md#function-bufferdata), [hybridse::vm::CurrentHistoryWindow::BufferData](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_current_history_window.md#function-bufferdata)


### function PopBackData

```cpp
inline virtual void PopBackData()
```


### function PopFrontData

```cpp
virtual void PopFrontData() =0
```


**Reimplemented by**: [hybridse::vm::HistoryWindow::PopFrontData](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_history_window.md#function-popfrontdata), [hybridse::vm::CurrentHistoryWindow::PopFrontData](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_current_history_window.md#function-popfrontdata)


### function GetCount

```cpp
inline virtual const uint64_t GetCount()
```


**Reimplements**: [hybridse::vm::MemTimeTableHandler::GetCount](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getcount)


### function At

```cpp
inline virtual Row At(
    uint64_t pos
)
```


**Reimplements**: [hybridse::vm::MemTimeTableHandler::At](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-at)


### function GetHandlerTypeName

```cpp
inline virtual const std::string GetHandlerTypeName() override
```


**Return**: 

**Reimplements**: [hybridse::vm::MemTimeTableHandler::GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-gethandlertypename)


Implemented by subclasses return the name of handler type 


### function instance_not_in_window

```cpp
inline const bool instance_not_in_window() const
```


### function set_instance_not_in_window

```cpp
inline void set_instance_not_in_window(
    const bool flag
)
```


### function exclude_current_time

```cpp
inline const bool exclude_current_time() const
```


### function set_exclude_current_time

```cpp
inline void set_exclude_current_time(
    const bool flag
)
```


## Protected Attributes Documentation

### variable exclude_current_time_

```cpp
bool exclude_current_time_;
```


### variable instance_not_in_window_

```cpp
bool instance_not_in_window_;
```


-------------------------------

Updated on 28 March 2021 at 19:41:19 PDT