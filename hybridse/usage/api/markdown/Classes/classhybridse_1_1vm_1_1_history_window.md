---
title: hybridse::vm::HistoryWindow

---

# hybridse::vm::HistoryWindow



 [More...](#detailed-description)


`#include <mem_catalog.h>`

Inherits from [hybridse::vm::Window](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md), [hybridse::vm::MemTimeTableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md), [hybridse::vm::TableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md), [hybridse::vm::DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md), [hybridse::codec::ListV< Row >](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md)

Inherited by [hybridse::vm::CurrentHistoryWindow](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_current_history_window.md)

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[HistoryWindow](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_history_window.md#function-historywindow)**(const [WindowRange](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window_range.md) & window_range) |
| | **[~HistoryWindow](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_history_window.md#function-~historywindow)**() |
| virtual void | **[PopFrontData](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_history_window.md#function-popfrontdata)**() |
| virtual void | **[PopEffectiveData](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_history_window.md#function-popeffectivedata)**() |
| virtual bool | **[BufferData](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_history_window.md#function-bufferdata)**(uint64_t key, const [Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md) & row) |

## Protected Functions

|                | Name           |
| -------------- | -------------- |
| bool | **[BufferCurrentHistoryBuffer](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_history_window.md#function-buffercurrenthistorybuffer)**(uint64_t key, const [Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md) & row, uint64_t end_ts) |
| bool | **[BufferEffectiveWindow](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_history_window.md#function-buffereffectivewindow)**(uint64_t key, const [Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md) & row, uint64_t start_ts) |
| bool | **[BufferCurrentTimeBuffer](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_history_window.md#function-buffercurrenttimebuffer)**(uint64_t key, const [Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md) & row, uint64_t start_ts) |

## Protected Attributes

|                | Name           |
| -------------- | -------------- |
| [WindowRange](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window_range.md) | **[window_range_](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_history_window.md#variable-window_range_)**  |
| [MemTimeTable](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#typedef-memtimetable) | **[current_history_buffer_](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_history_window.md#variable-current_history_buffer_)**  |

## Additional inherited members

**Public Types inherited from [hybridse::vm::Window](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md)**

|                | Name           |
| -------------- | -------------- |
| enum| **[WindowFrameType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#enum-windowframetype)** { kFrameRows, kFrameRowsRange, kFrameRowsMergeRowsRange} |

**Public Functions inherited from [hybridse::vm::Window](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md)**

|                | Name           |
| -------------- | -------------- |
| | **[Window](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#function-window)**() |
| virtual | **[~Window](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#function-~window)**() |
| virtual std::unique_ptr< RowIterator > | **[GetIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#function-getiterator)**() override<br>Implemented by subclasses to return the const iterator.  |
| virtual RowIterator * | **[GetRawIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#function-getrawiterator)**()<br>Implemented by subclasses to return the const iterator raw pointer.  |
| virtual void | **[PopBackData](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#function-popbackdata)**() |
| virtual const uint64_t | **[GetCount](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#function-getcount)**()<br>Returns the number of elements in this list.  |
| virtual [Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md) | **[At](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#function-at)**(uint64_t pos) |
| virtual const std::string | **[GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#function-gethandlertypename)**() override<br>Return the name of handler and return "TableHandler" by default.  |
| const bool | **[instance_not_in_window](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#function-instance_not_in_window)**() const |
| void | **[set_instance_not_in_window](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#function-set_instance_not_in_window)**(const bool flag) |
| const bool | **[exclude_current_time](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#function-exclude_current_time)**() const |
| void | **[set_exclude_current_time](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#function-set_exclude_current_time)**(const bool flag) |

**Protected Attributes inherited from [hybridse::vm::Window](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md)**

|                | Name           |
| -------------- | -------------- |
| bool | **[exclude_current_time_](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#variable-exclude_current_time_)**  |
| bool | **[instance_not_in_window_](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#variable-instance_not_in_window_)**  |

**Public Functions inherited from [hybridse::vm::MemTimeTableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[MemTimeTableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-memtimetablehandler)**() |
| | **[MemTimeTableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-memtimetablehandler)**(const Schema * schema) |
| | **[MemTimeTableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-memtimetablehandler)**(const std::string & table_name, const std::string & db, const Schema * schema) |
| virtual const [Types](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#typedef-types) & | **[GetTypes](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-gettypes)**() override<br>Implemented by subclasses to return table column Types information.  |
| | **[~MemTimeTableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-~memtimetablehandler)**() override |
| virtual const Schema * | **[GetSchema](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getschema)**()<br>Implemented by subclasses to return table schema.  |
| virtual const std::string & | **[GetName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getname)**()<br>Implemented by subclasses to return table name.  |
| virtual const [IndexHint](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#typedef-indexhint) & | **[GetIndex](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getindex)**()<br>Return the index information.  |
| virtual std::unique_ptr< RowIterator > | **[GetIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getiterator)**()<br>Implemented by subclasses to return the const iterator.  |
| virtual RowIterator * | **[GetRawIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getrawiterator)**()<br>Implemented by subclasses to return the const iterator raw pointer.  |
| virtual const std::string & | **[GetDatabase](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getdatabase)**()<br>Implemented by subclasses to return the name of database.  |
| virtual std::unique_ptr< [WindowIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_window_iterator.md) > | **[GetWindowIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getwindowiterator)**(const std::string & idx_name) |
| void | **[AddRow](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-addrow)**(const uint64_t key, const [Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md) & v) |
| void | **[AddFrontRow](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-addfrontrow)**(const uint64_t key, const [Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md) & v) |
| void | **[PopBackRow](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-popbackrow)**() |
| void | **[PopFrontRow](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-popfrontrow)**() |
| virtual const std::pair< uint64_t, [Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md) > & | **[GetFrontRow](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getfrontrow)**() |
| virtual const std::pair< uint64_t, [Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md) > & | **[GetBackRow](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getbackrow)**() |
| void | **[Sort](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-sort)**(const bool is_asc) |
| void | **[Reverse](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-reverse)**() |
| virtual const uint64_t | **[GetCount](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getcount)**()<br>Returns the number of elements in this list.  |
| virtual [Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md) | **[At](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-at)**(uint64_t pos) |
| void | **[SetOrderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-setordertype)**(const [OrderType](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype) order_type) |
| virtual const [OrderType](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype) | **[GetOrderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getordertype)**() const |
| virtual const std::string | **[GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-gethandlertypename)**() override<br>Return the name of handler and return "TableHandler" by default.  |

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
| virtual const [Types](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#typedef-types) & | **[GetTypes](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettypes)**() =0<br>Implemented by subclasses to return table column Types information.  |
| virtual const [IndexHint](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#typedef-indexhint) & | **[GetIndex](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getindex)**() =0<br>Return the index information.  |
| virtual std::unique_ptr< [WindowIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_window_iterator.md) > | **[GetWindowIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getwindowiterator)**(const std::string & idx_name) =0 |
| virtual const [HandlerType](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) | **[GetHanlderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gethanldertype)**() override |
| virtual std::shared_ptr< [PartitionHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md) > | **[GetPartition](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getpartition)**(const std::string & index_name) |
| virtual const std::string | **[GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gethandlertypename)**() override<br>Return the name of handler and return "TableHandler" by default.  |
| virtual const [OrderType](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype) | **[GetOrderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getordertype)**() const |
| virtual std::shared_ptr< [Tablet](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_tablet.md) > | **[GetTablet](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettablet)**(const std::string & index_name, const std::string & pk) |
| virtual std::shared_ptr< [Tablet](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_tablet.md) > | **[GetTablet](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettablet)**(const std::string & index_name, const std::vector< std::string > & pks) |

**Public Functions inherited from [hybridse::vm::DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-datahandler)**() |
| virtual | **[~DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-~datahandler)**() |
| virtual const Schema * | **[GetSchema](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getschema)**() =0<br>Implemented by subclasses to return table schema.  |
| virtual const std::string & | **[GetName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getname)**() =0<br>Implemented by subclasses to return table name.  |
| virtual const std::string & | **[GetDatabase](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getdatabase)**() =0<br>Implemented by subclasses to return the name of database.  |
| virtual const [HandlerType](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) | **[GetHanlderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethanldertype)**() =0<br>Implemented by subclasses to return the type of [DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md).  |
| virtual const std::string | **[GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethandlertypename)**() =0<br>Implemented by subclasses return the name of handler type.  |
| virtual base::Status | **[GetStatus](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getstatus)**()<br>Return dataset status. Default is hybridse::common::kOk.  |

**Public Functions inherited from [hybridse::codec::ListV< Row >](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md)**

|                | Name           |
| -------------- | -------------- |
| | **[ListV](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md#function-listv)**() |
| virtual | **[~ListV](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md#function-~listv)**() |
| virtual std::unique_ptr< [ConstIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1base_1_1_const_iterator.md)< uint64_t, V > > | **[GetIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getiterator)**() =0<br>Implemented by subclasses to return the const iterator.  |
| virtual [ConstIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1base_1_1_const_iterator.md)< uint64_t, V > * | **[GetRawIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getrawiterator)**() =0<br>Implemented by subclasses to return the const iterator raw pointer.  |
| virtual const uint64_t | **[GetCount](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getcount)**()<br>Returns the number of elements in this list.  |
| virtual V | **[At](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md#function-at)**(uint64_t pos) |


## Detailed Description

```cpp
class hybridse::vm::HistoryWindow;
```


|start_ts.............end_ts| current_ts| |.............history window| current history buffer| 

## Public Functions Documentation

### function HistoryWindow

```cpp
inline explicit HistoryWindow(
    const WindowRange & window_range
)
```


### function ~HistoryWindow

```cpp
inline ~HistoryWindow()
```


### function PopFrontData

```cpp
inline virtual void PopFrontData()
```


**Reimplements**: [hybridse::vm::Window::PopFrontData](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#function-popfrontdata)


**Reimplemented by**: [hybridse::vm::CurrentHistoryWindow::PopFrontData](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_current_history_window.md#function-popfrontdata)


### function PopEffectiveData

```cpp
inline virtual void PopEffectiveData()
```


### function BufferData

```cpp
inline virtual bool BufferData(
    uint64_t key,
    const Row & row
)
```


**Reimplements**: [hybridse::vm::Window::BufferData](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#function-bufferdata)


**Reimplemented by**: [hybridse::vm::CurrentHistoryWindow::BufferData](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_current_history_window.md#function-bufferdata)


## Protected Functions Documentation

### function BufferCurrentHistoryBuffer

```cpp
inline bool BufferCurrentHistoryBuffer(
    uint64_t key,
    const Row & row,
    uint64_t end_ts
)
```


### function BufferEffectiveWindow

```cpp
inline bool BufferEffectiveWindow(
    uint64_t key,
    const Row & row,
    uint64_t start_ts
)
```


### function BufferCurrentTimeBuffer

```cpp
inline bool BufferCurrentTimeBuffer(
    uint64_t key,
    const Row & row,
    uint64_t start_ts
)
```


## Protected Attributes Documentation

### variable window_range_

```cpp
WindowRange window_range_;
```


### variable current_history_buffer_

```cpp
MemTimeTable current_history_buffer_;
```


-------------------------------

Updated on 29 March 2021 at 10:12:21 PDT