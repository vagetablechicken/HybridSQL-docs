---
title: hybridse::vm::TableHandler
summary: A table dataset operation abstraction. 

---

# hybridse::vm::TableHandler



A table dataset operation abstraction. 
`#include <catalog.h>`

Inherits from [hybridse::vm::DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md), [hybridse::codec::ListV< Row >](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md)

Inherited by [hybridse::vm::ErrorTableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_error_table_handler.md), [hybridse::vm::MemSegmentHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md), [hybridse::vm::MemTableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md), [hybridse::vm::MemTimeTableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md), [hybridse::vm::PartitionHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md), [hybridse::vm::RequestUnionTableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md)

## Public Functions

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

## Additional inherited members

**Public Functions inherited from [hybridse::vm::DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-datahandler)**() |
| virtual | **[~DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-~datahandler)**() |
| virtual const Schema * | **[GetSchema](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getschema)**() =0<br>Implemented by subclasses to return table schema.  |
| virtual const std::string & | **[GetName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getname)**() =0<br>Implemented by subclasses to return table name.  |
| virtual const std::string & | **[GetDatabase](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getdatabase)**() =0<br>Implemented by subclasses to return the name of database.  |
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


## Public Functions Documentation

### function TableHandler

```cpp
inline TableHandler()
```


### function ~TableHandler

```cpp
inline virtual ~TableHandler()
```


### function GetTypes

```cpp
virtual const Types & GetTypes() =0
```

Implemented by subclasses to return table column Types information. 

**Reimplemented by**: [hybridse::vm::MemSegmentHandler::GetTypes](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md#function-gettypes), [hybridse::vm::ErrorTableHandler::GetTypes](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-gettypes), [hybridse::vm::MemTableHandler::GetTypes](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-gettypes), [hybridse::vm::MemTimeTableHandler::GetTypes](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-gettypes), [hybridse::vm::MemPartitionHandler::GetTypes](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-gettypes), [hybridse::vm::RequestUnionTableHandler::GetTypes](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-gettypes)


### function GetIndex

```cpp
virtual const IndexHint & GetIndex() =0
```

Return the index information. 

**Reimplemented by**: [hybridse::vm::MemTableHandler::GetIndex](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getindex), [hybridse::vm::MemTimeTableHandler::GetIndex](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getindex), [hybridse::vm::MemSegmentHandler::GetIndex](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md#function-getindex), [hybridse::vm::ErrorTableHandler::GetIndex](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-getindex), [hybridse::vm::MemPartitionHandler::GetIndex](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getindex), [hybridse::vm::RequestUnionTableHandler::GetIndex](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-getindex)


### function GetWindowIterator

```cpp
virtual std::unique_ptr< WindowIterator > GetWindowIterator(
    const std::string & idx_name
) =0
```


**Reimplemented by**: [hybridse::vm::RequestUnionTableHandler::GetWindowIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-getwindowiterator), [hybridse::vm::ErrorTableHandler::GetWindowIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-getwindowiterator), [hybridse::vm::PartitionHandler::GetWindowIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getwindowiterator), [hybridse::vm::MemTableHandler::GetWindowIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getwindowiterator), [hybridse::vm::MemTimeTableHandler::GetWindowIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getwindowiterator), [hybridse::vm::MemSegmentHandler::GetWindowIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md#function-getwindowiterator)


Implemented by subclasses to return WindowIterator so that user can use it to iterate datasets segment by segment. 


### function GetHanlderType

```cpp
inline virtual const HandlerType GetHanlderType() override
```


**Reimplements**: [hybridse::vm::DataHandler::GetHanlderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethanldertype)


**Reimplemented by**: [hybridse::vm::PartitionHandler::GetHanlderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-gethanldertype)


Return the HandlerType of the dataset. Return HandlerType::kTableHandler by default 


### function GetPartition

```cpp
inline virtual std::shared_ptr< PartitionHandler > GetPartition(
    const std::string & index_name
)
```


Return partition handler of specify partition binding to given index. Return `null` by default. 


### function GetHandlerTypeName

```cpp
inline virtual const std::string GetHandlerTypeName() override
```

Return the name of handler and return "TableHandler" by default. 

**Reimplements**: [hybridse::vm::DataHandler::GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethandlertypename)


**Reimplemented by**: [hybridse::vm::ErrorTableHandler::GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-gethandlertypename), [hybridse::vm::PartitionHandler::GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-gethandlertypename), [hybridse::vm::MemTableHandler::GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-gethandlertypename), [hybridse::vm::MemTimeTableHandler::GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-gethandlertypename), [hybridse::vm::Window::GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#function-gethandlertypename), [hybridse::vm::MemSegmentHandler::GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md#function-gethandlertypename), [hybridse::vm::MemPartitionHandler::GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-gethandlertypename)


### function GetOrderType

```cpp
inline virtual const OrderType GetOrderType() const
```


**Reimplemented by**: [hybridse::vm::PartitionHandler::GetOrderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getordertype), [hybridse::vm::MemTableHandler::GetOrderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getordertype), [hybridse::vm::MemTimeTableHandler::GetOrderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getordertype), [hybridse::vm::MemSegmentHandler::GetOrderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md#function-getordertype), [hybridse::vm::MemPartitionHandler::GetOrderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getordertype), [hybridse::vm::RequestUnionTableHandler::GetOrderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-getordertype)


Return the order type of the dataset, and return OrderType::kNoneOrder by default. 


### function GetTablet

```cpp
inline virtual std::shared_ptr< Tablet > GetTablet(
    const std::string & index_name,
    const std::string & pk
)
```


Return `[Tablet](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_tablet.md)` binding to specify index and key. Return `null` by default. 


### function GetTablet

```cpp
inline virtual std::shared_ptr< Tablet > GetTablet(
    const std::string & index_name,
    const std::vector< std::string > & pks
)
```


Return `[Tablet](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_tablet.md)` binding to specify index and keys. Return `null` by default. 


-------------------------------

Updated on 29 March 2021 at 10:12:21 PDT