---
title: hybridse::vm::CurrentHistoryWindow

---

# hybridse::vm::CurrentHistoryWindow



 [More...](#detailed-description)


`#include <mem_catalog.h>`

Inherits from [hybridse::vm::HistoryWindow](/Classes/classhybridse_1_1vm_1_1_history_window.md), [hybridse::vm::Window](/Classes/classhybridse_1_1vm_1_1_window.md), [hybridse::vm::MemTimeTableHandler](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md), [hybridse::vm::TableHandler](/Classes/classhybridse_1_1vm_1_1_table_handler.md), [hybridse::vm::DataHandler](/Classes/classhybridse_1_1vm_1_1_data_handler.md), hybridse::codec::ListV< Row >

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[CurrentHistoryWindow](/Classes/classhybridse_1_1vm_1_1_current_history_window.md#function-currenthistorywindow)**(const [WindowRange](/Classes/classhybridse_1_1vm_1_1_window_range.md) & window_range) |
| | **[CurrentHistoryWindow](/Classes/classhybridse_1_1vm_1_1_current_history_window.md#function-currenthistorywindow)**(const [Window::WindowFrameType](/Classes/classhybridse_1_1vm_1_1_window.md#enum-windowframetype) window_frame, uint64_t start_offset, uint64_t max_size) |
| | **[CurrentHistoryWindow](/Classes/classhybridse_1_1vm_1_1_current_history_window.md#function-currenthistorywindow)**(const [Window::WindowFrameType](/Classes/classhybridse_1_1vm_1_1_window.md#enum-windowframetype) window_frame, uint64_t start_offset, uint64_t start_rows, uint64_t max_size) |
| | **[~CurrentHistoryWindow](/Classes/classhybridse_1_1vm_1_1_current_history_window.md#function-~currenthistorywindow)**() |
| virtual void | **[PopFrontData](/Classes/classhybridse_1_1vm_1_1_current_history_window.md#function-popfrontdata)**() |
| virtual bool | **[BufferData](/Classes/classhybridse_1_1vm_1_1_current_history_window.md#function-bufferdata)**(uint64_t key, const Row & row) |

## Additional inherited members

**Public Functions inherited from [hybridse::vm::HistoryWindow](/Classes/classhybridse_1_1vm_1_1_history_window.md)**

|                | Name           |
| -------------- | -------------- |
| | **[HistoryWindow](/Classes/classhybridse_1_1vm_1_1_history_window.md#function-historywindow)**(const [WindowRange](/Classes/classhybridse_1_1vm_1_1_window_range.md) & window_range) |
| | **[~HistoryWindow](/Classes/classhybridse_1_1vm_1_1_history_window.md#function-~historywindow)**() |
| virtual void | **[PopEffectiveData](/Classes/classhybridse_1_1vm_1_1_history_window.md#function-popeffectivedata)**() |

**Protected Functions inherited from [hybridse::vm::HistoryWindow](/Classes/classhybridse_1_1vm_1_1_history_window.md)**

|                | Name           |
| -------------- | -------------- |
| bool | **[BufferCurrentHistoryBuffer](/Classes/classhybridse_1_1vm_1_1_history_window.md#function-buffercurrenthistorybuffer)**(uint64_t key, const Row & row, uint64_t end_ts) |
| bool | **[BufferEffectiveWindow](/Classes/classhybridse_1_1vm_1_1_history_window.md#function-buffereffectivewindow)**(uint64_t key, const Row & row, uint64_t start_ts) |
| bool | **[BufferCurrentTimeBuffer](/Classes/classhybridse_1_1vm_1_1_history_window.md#function-buffercurrenttimebuffer)**(uint64_t key, const Row & row, uint64_t start_ts) |

**Protected Attributes inherited from [hybridse::vm::HistoryWindow](/Classes/classhybridse_1_1vm_1_1_history_window.md)**

|                | Name           |
| -------------- | -------------- |
| [WindowRange](/Classes/classhybridse_1_1vm_1_1_window_range.md) | **[window_range_](/Classes/classhybridse_1_1vm_1_1_history_window.md#variable-window_range_)**  |
| [MemTimeTable](/Namespaces/namespacehybridse_1_1vm.md#typedef-memtimetable) | **[current_history_buffer_](/Classes/classhybridse_1_1vm_1_1_history_window.md#variable-current_history_buffer_)**  |

**Public Types inherited from [hybridse::vm::Window](/Classes/classhybridse_1_1vm_1_1_window.md)**

|                | Name           |
| -------------- | -------------- |
| enum| **[WindowFrameType](/Classes/classhybridse_1_1vm_1_1_window.md#enum-windowframetype)** { kFrameRows, kFrameRowsRange, kFrameRowsMergeRowsRange} |

**Public Functions inherited from [hybridse::vm::Window](/Classes/classhybridse_1_1vm_1_1_window.md)**

|                | Name           |
| -------------- | -------------- |
| | **[Window](/Classes/classhybridse_1_1vm_1_1_window.md#function-window)**() |
| virtual | **[~Window](/Classes/classhybridse_1_1vm_1_1_window.md#function-~window)**() |
| std::unique_ptr< RowIterator > | **[GetIterator](/Classes/classhybridse_1_1vm_1_1_window.md#function-getiterator)**() override |
| RowIterator * | **[GetRawIterator](/Classes/classhybridse_1_1vm_1_1_window.md#function-getrawiterator)**() |
| virtual void | **[PopBackData](/Classes/classhybridse_1_1vm_1_1_window.md#function-popbackdata)**() |
| virtual const uint64_t | **[GetCount](/Classes/classhybridse_1_1vm_1_1_window.md#function-getcount)**() |
| virtual Row | **[At](/Classes/classhybridse_1_1vm_1_1_window.md#function-at)**(uint64_t pos) |
| virtual const std::string | **[GetHandlerTypeName](/Classes/classhybridse_1_1vm_1_1_window.md#function-gethandlertypename)**() override |
| const bool | **[instance_not_in_window](/Classes/classhybridse_1_1vm_1_1_window.md#function-instance_not_in_window)**() const |
| void | **[set_instance_not_in_window](/Classes/classhybridse_1_1vm_1_1_window.md#function-set_instance_not_in_window)**(const bool flag) |
| const bool | **[exclude_current_time](/Classes/classhybridse_1_1vm_1_1_window.md#function-exclude_current_time)**() const |
| void | **[set_exclude_current_time](/Classes/classhybridse_1_1vm_1_1_window.md#function-set_exclude_current_time)**(const bool flag) |

**Protected Attributes inherited from [hybridse::vm::Window](/Classes/classhybridse_1_1vm_1_1_window.md)**

|                | Name           |
| -------------- | -------------- |
| bool | **[exclude_current_time_](/Classes/classhybridse_1_1vm_1_1_window.md#variable-exclude_current_time_)**  |
| bool | **[instance_not_in_window_](/Classes/classhybridse_1_1vm_1_1_window.md#variable-instance_not_in_window_)**  |

**Public Functions inherited from [hybridse::vm::MemTimeTableHandler](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[MemTimeTableHandler](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-memtimetablehandler)**() |
| | **[MemTimeTableHandler](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-memtimetablehandler)**(const Schema * schema) |
| | **[MemTimeTableHandler](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-memtimetablehandler)**(const std::string & table_name, const std::string & db, const Schema * schema) |
| virtual const [Types](/Namespaces/namespacehybridse_1_1vm.md#typedef-types) & | **[GetTypes](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-gettypes)**() override |
| | **[~MemTimeTableHandler](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-~memtimetablehandler)**() override |
| virtual const Schema * | **[GetSchema](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getschema)**() |
| virtual const std::string & | **[GetName](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getname)**() |
| virtual const [IndexHint](/Namespaces/namespacehybridse_1_1vm.md#typedef-indexhint) & | **[GetIndex](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getindex)**() |
| std::unique_ptr< RowIterator > | **[GetIterator](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getiterator)**() |
| RowIterator * | **[GetRawIterator](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getrawiterator)**() |
| virtual const std::string & | **[GetDatabase](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getdatabase)**() |
| virtual std::unique_ptr< WindowIterator > | **[GetWindowIterator](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getwindowiterator)**(const std::string & idx_name) |
| void | **[AddRow](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-addrow)**(const uint64_t key, const Row & v) |
| void | **[AddFrontRow](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-addfrontrow)**(const uint64_t key, const Row & v) |
| void | **[PopBackRow](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-popbackrow)**() |
| void | **[PopFrontRow](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-popfrontrow)**() |
| virtual const std::pair< uint64_t, Row > & | **[GetFrontRow](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getfrontrow)**() |
| virtual const std::pair< uint64_t, Row > & | **[GetBackRow](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getbackrow)**() |
| void | **[Sort](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-sort)**(const bool is_asc) |
| void | **[Reverse](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-reverse)**() |
| virtual const uint64_t | **[GetCount](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getcount)**() |
| virtual Row | **[At](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-at)**(uint64_t pos) |
| void | **[SetOrderType](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-setordertype)**(const [OrderType](/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype) order_type) |
| virtual const [OrderType](/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype) | **[GetOrderType](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getordertype)**() const |
| virtual const std::string | **[GetHandlerTypeName](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-gethandlertypename)**() override |

**Protected Attributes inherited from [hybridse::vm::MemTimeTableHandler](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md)**

|                | Name           |
| -------------- | -------------- |
| const std::string | **[table_name_](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-table_name_)**  |
| const std::string | **[db_](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-db_)**  |
| const Schema * | **[schema_](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-schema_)**  |
| [Types](/Namespaces/namespacehybridse_1_1vm.md#typedef-types) | **[types_](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-types_)**  |
| [IndexHint](/Namespaces/namespacehybridse_1_1vm.md#typedef-indexhint) | **[index_hint_](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-index_hint_)**  |
| [MemTimeTable](/Namespaces/namespacehybridse_1_1vm.md#typedef-memtimetable) | **[table_](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-table_)**  |
| [OrderType](/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype) | **[order_type_](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-order_type_)**  |

**Public Functions inherited from [hybridse::vm::TableHandler](/Classes/classhybridse_1_1vm_1_1_table_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[TableHandler](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-tablehandler)**() |
| virtual | **[~TableHandler](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-~tablehandler)**() |
| virtual const [Types](/Namespaces/namespacehybridse_1_1vm.md#typedef-types) & | **[GetTypes](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettypes)**() =0 |
| virtual const [IndexHint](/Namespaces/namespacehybridse_1_1vm.md#typedef-indexhint) & | **[GetIndex](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getindex)**() =0 |
| virtual std::unique_ptr< WindowIterator > | **[GetWindowIterator](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getwindowiterator)**(const std::string & idx_name) =0 |
| virtual const [HandlerType](/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) | **[GetHanlderType](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gethanldertype)**() override |
| virtual std::shared_ptr< [PartitionHandler](/Classes/classhybridse_1_1vm_1_1_partition_handler.md) > | **[GetPartition](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getpartition)**(const std::string & index_name) |
| virtual const std::string | **[GetHandlerTypeName](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gethandlertypename)**() override |
| virtual const [OrderType](/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype) | **[GetOrderType](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getordertype)**() const |
| virtual std::shared_ptr< [Tablet](/Classes/classhybridse_1_1vm_1_1_tablet.md) > | **[GetTablet](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettablet)**(const std::string & index_name, const std::string & pk) |
| virtual std::shared_ptr< [Tablet](/Classes/classhybridse_1_1vm_1_1_tablet.md) > | **[GetTablet](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettablet)**(const std::string & index_name, const std::vector< std::string > & pks) |

**Public Functions inherited from [hybridse::vm::DataHandler](/Classes/classhybridse_1_1vm_1_1_data_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[DataHandler](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-datahandler)**() |
| virtual | **[~DataHandler](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-~datahandler)**() |
| virtual const Schema * | **[GetSchema](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getschema)**() =0 |
| virtual const std::string & | **[GetName](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getname)**() =0 |
| virtual const std::string & | **[GetDatabase](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getdatabase)**() =0 |
| virtual const [HandlerType](/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) | **[GetHanlderType](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethanldertype)**() =0 |
| virtual const std::string | **[GetHandlerTypeName](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethandlertypename)**() =0 |
| virtual base::Status | **[GetStatus](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getstatus)**() |


## Detailed Description

```cpp
class hybridse::vm::CurrentHistoryWindow;
```


|start_ts....................................current_ts| |................................current history window| current history window is effective window there is no current_history_buffer_ 

## Public Functions Documentation

### function CurrentHistoryWindow

```cpp
inline explicit CurrentHistoryWindow(
    const WindowRange & window_range
)
```


### function CurrentHistoryWindow

```cpp
inline explicit CurrentHistoryWindow(
    const Window::WindowFrameType window_frame,
    uint64_t start_offset,
    uint64_t max_size
)
```


### function CurrentHistoryWindow

```cpp
inline explicit CurrentHistoryWindow(
    const Window::WindowFrameType window_frame,
    uint64_t start_offset,
    uint64_t start_rows,
    uint64_t max_size
)
```


### function ~CurrentHistoryWindow

```cpp
inline ~CurrentHistoryWindow()
```


### function PopFrontData

```cpp
inline virtual void PopFrontData()
```


**Reimplements**: [hybridse::vm::HistoryWindow::PopFrontData](/Classes/classhybridse_1_1vm_1_1_history_window.md#function-popfrontdata)


### function BufferData

```cpp
inline virtual bool BufferData(
    uint64_t key,
    const Row & row
)
```


**Reimplements**: [hybridse::vm::HistoryWindow::BufferData](/Classes/classhybridse_1_1vm_1_1_history_window.md#function-bufferdata)


-------------------------------

Updated on 28 March 2021 at 19:23:48 PDT