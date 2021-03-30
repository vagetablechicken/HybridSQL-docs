---
title: hybridse::vm::Window

---
# hybridse::vm::Window



`#include <mem_catalog.h>`

## Summary
## Public Types

|                | Name           |
| -------------- | -------------- |
| enum| **[WindowFrameType](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window.md#enum-windowframetype)** { kFrameRows, kFrameRowsRange, kFrameRowsMergeRowsRange} |



|  Public functions|            |
| -------------- | -------------- |
|**[Window](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window.md#function-window)**()|  |
|**[~Window](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window.md#function-~window)**()|  |
|**[GetIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window.md#function-getiterator)**() override| std::unique_ptr< RowIterator > <br>Return the const iterator.  |
|**[GetRawIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window.md#function-getrawiterator)**()| RowIterator * <br>Return the const iterator raw pointer.  |
|**[BufferData](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window.md#function-bufferdata)**(uint64_t key, const [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) & row) =0| bool  |
|**[PopBackData](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window.md#function-popbackdata)**()| void  |
|**[PopFrontData](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window.md#function-popfrontdata)**() =0| void  |
|**[GetCount](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window.md#function-getcount)**()| const uint64_t <br>Returns the number of elements in this list.  |
|**[At](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window.md#function-at)**(uint64_t pos)| [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) <br>Return a the value of element by its position in the list.  |
|**[GetHandlerTypeName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window.md#function-gethandlertypename)**() override| const std::string <br>Return the name of handler and return "TableHandler" by default.  |
|**[instance_not_in_window](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window.md#function-instance_not_in_window)**() const| const bool  |
|**[set_instance_not_in_window](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window.md#function-set_instance_not_in_window)**(const bool flag)| void  |
|**[exclude_current_time](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window.md#function-exclude_current_time)**() const| const bool  |
|**[set_exclude_current_time](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window.md#function-set_exclude_current_time)**(const bool flag)| void  |

##

| Protected attributes | |
| -------------- | -------------- |
| **[exclude_current_time_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window.md#variable-exclude_current_time_)**
| bool  |
| **[instance_not_in_window_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window.md#variable-instance_not_in_window_)**
| bool  |

## Inherited members
Inherited by [hybridse::vm::HistoryWindow](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_history_window.md)
Inherited from [hybridse::vm::MemTimeTableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md)
| **Inherited public functions** | Name           |
| -------------- | -------------- |
|**[MemTimeTableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-memtimetablehandler)**()|  |
|**[MemTimeTableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-memtimetablehandler)**(const Schema * schema)|  |
|**[MemTimeTableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-memtimetablehandler)**(const std::string & table_name, const std::string & db, const Schema * schema)|  |
|**[GetTypes](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-gettypes)**() override| virtual const [Types](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-types) & <br>Return table column Types information.  |
|**[~MemTimeTableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-~memtimetablehandler)**() override|  |
|**[GetSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getschema)**()| virtual const Schema * <br>Return table schema.  |
|**[GetName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getname)**()| virtual const std::string & <br>Return table name.  |
|**[GetIndex](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getindex)**()| virtual const [IndexHint](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-indexhint) & <br>Return the index information.  |
|**[GetDatabase](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getdatabase)**()| virtual const std::string & <br>Return the name of database.  |
|**[GetWindowIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getwindowiterator)**(const std::string & idx_name)| virtual std::unique_ptr< [WindowIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_window_iterator.md) >  |
|**[AddRow](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-addrow)**(const uint64_t key, const [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) & v)| void  |
|**[AddFrontRow](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-addfrontrow)**(const uint64_t key, const [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) & v)| void  |
|**[PopBackRow](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-popbackrow)**()| void  |
|**[PopFrontRow](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-popfrontrow)**()| void  |
|**[GetFrontRow](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getfrontrow)**()| virtual const std::pair< uint64_t, [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) > &  |
|**[GetBackRow](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getbackrow)**()| virtual const std::pair< uint64_t, [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) > &  |
|**[Sort](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-sort)**(const bool is_asc)| void  |
|**[Reverse](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-reverse)**()| void  |
|**[SetOrderType](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-setordertype)**(const [OrderType](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype) order_type)| void  |
|**[GetOrderType](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getordertype)**() const| virtual const [OrderType](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype)  |

**Protected Attributes inherited from [hybridse::vm::MemTimeTableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md)**

|                | Name           |
| -------------- | -------------- |
| const std::string | **[table_name_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-table_name_)**  |
| const std::string | **[db_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-db_)**  |
| const Schema * | **[schema_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-schema_)**  |
| [Types](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-types) | **[types_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-types_)**  |
| [IndexHint](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-indexhint) | **[index_hint_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-index_hint_)**  |
| [MemTimeTable](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-memtimetable) | **[table_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-table_)**  |
| [OrderType](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype) | **[order_type_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-order_type_)**  |

Inherited from [hybridse::vm::TableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md)
| **Inherited public functions** | Name           |
| -------------- | -------------- |
|**[TableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-tablehandler)**()|  |
|**[~TableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-~tablehandler)**()| virtual  |
|**[GetTypes](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettypes)**() =0| virtual const [Types](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-types) & <br>Return table column Types information.  |
|**[GetIndex](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getindex)**() =0| virtual const [IndexHint](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-indexhint) & <br>Return the index information.  |
|**[GetWindowIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getwindowiterator)**(const std::string & idx_name) =0| virtual std::unique_ptr< [WindowIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_window_iterator.md) >  |
|**[GetHanlderType](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gethanldertype)**() override| virtual const [HandlerType](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype)  |
|**[GetPartition](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getpartition)**(const std::string & index_name)| virtual std::shared_ptr< [PartitionHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md) >  |
|**[GetOrderType](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getordertype)**() const| virtual const [OrderType](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype)  |
|**[GetTablet](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettablet)**(const std::string & index_name, const std::string & pk)| virtual std::shared_ptr< [Tablet](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_tablet.md) >  |
|**[GetTablet](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettablet)**(const std::string & index_name, const std::vector< std::string > & pks)| virtual std::shared_ptr< [Tablet](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_tablet.md) >  |

Inherited from [hybridse::vm::DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md)
| **Inherited public functions** | Name           |
| -------------- | -------------- |
|**[DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-datahandler)**()|  |
|**[~DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-~datahandler)**()| virtual  |
|**[GetSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getschema)**() =0| virtual const Schema * <br>Return table schema.  |
|**[GetName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getname)**() =0| virtual const std::string & <br>Return table name.  |
|**[GetDatabase](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getdatabase)**() =0| virtual const std::string & <br>Return the name of database.  |
|**[GetHanlderType](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethanldertype)**() =0| virtual const [HandlerType](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) <br>Return the type of [DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md).  |
|**[GetStatus](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getstatus)**()| virtual base::Status <br>Return dataset status. Default is hybridse::common::kOk.  |

Inherited from [hybridse::codec::ListV< Row >](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md)
| **Inherited public functions** | Name           |
| -------------- | -------------- |
|**[ListV](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-listv)**()|  |
|**[~ListV](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-~listv)**()| virtual  |


## Public Types

### WindowFrameType

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| kFrameRows | |   |
| kFrameRowsRange | |   |
| kFrameRowsMergeRowsRange | |   |




## Public Functions

#### Window { function Window }

```cpp
inline Window()
```


#### ~Window { function ~Window }

```cpp
inline virtual ~Window()
```


#### GetIterator { function GetIterator }

```cpp
inline virtual std::unique_ptr< RowIterator > GetIterator() override
```

Return the const iterator. 

**Reimplements**: [hybridse::vm::MemTimeTableHandler::GetIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getiterator)


#### GetRawIterator { function GetRawIterator }

```cpp
inline virtual RowIterator * GetRawIterator()
```

Return the const iterator raw pointer. 

**Reimplements**: [hybridse::vm::MemTimeTableHandler::GetRawIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getrawiterator)


#### BufferData { function BufferData }

```cpp
virtual bool BufferData(
    uint64_t key,
    const Row & row
) =0
```


**Reimplemented by**: [hybridse::vm::HistoryWindow::BufferData](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_history_window.md#function-bufferdata), [hybridse::vm::CurrentHistoryWindow::BufferData](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_current_history_window.md#function-bufferdata)


#### PopBackData { function PopBackData }

```cpp
inline virtual void PopBackData()
```


#### PopFrontData { function PopFrontData }

```cpp
virtual void PopFrontData() =0
```


**Reimplemented by**: [hybridse::vm::HistoryWindow::PopFrontData](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_history_window.md#function-popfrontdata), [hybridse::vm::CurrentHistoryWindow::PopFrontData](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_current_history_window.md#function-popfrontdata)


#### GetCount { function GetCount }

```cpp
inline virtual const uint64_t GetCount()
```

Returns the number of elements in this list. 

**Reimplements**: [hybridse::vm::MemTimeTableHandler::GetCount](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getcount)


It count element by traverse the list 


#### At { function At }

```cpp
inline virtual Row At(
    uint64_t pos
)
```

Return a the value of element by its position in the list. 

**Parameters**: 

  * **pos** is element position in the list 


**Reimplements**: [hybridse::vm::MemTimeTableHandler::At](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-at)


#### GetHandlerTypeName { function GetHandlerTypeName }

```cpp
inline virtual const std::string GetHandlerTypeName() override
```

Return the name of handler and return "TableHandler" by default. 

**Reimplements**: [hybridse::vm::MemTimeTableHandler::GetHandlerTypeName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-gethandlertypename)


#### instance_not_in_window { function instance_not_in_window }

```cpp
inline const bool instance_not_in_window() const
```


#### set_instance_not_in_window { function set_instance_not_in_window }

```cpp
inline void set_instance_not_in_window(
    const bool flag
)
```


#### exclude_current_time { function exclude_current_time }

```cpp
inline const bool exclude_current_time() const
```


#### set_exclude_current_time { function set_exclude_current_time }

```cpp
inline void set_exclude_current_time(
    const bool flag
)
```


## Protected Attributes

### exclude_current_time_

```cpp
bool exclude_current_time_;
```


### instance_not_in_window_

```cpp
bool instance_not_in_window_;
```


-------------------------------

Updated on 29 March 2021 at 17:58:51 PDT