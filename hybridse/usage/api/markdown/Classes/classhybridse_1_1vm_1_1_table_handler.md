---
title: hybridse::vm::TableHandler

---

# hybridse::vm::TableHandler




`#include <catalog.h>`

Inherits from [hybridse::vm::DataHandler](/Classes/classhybridse_1_1vm_1_1_data_handler.md), hybridse::codec::ListV< Row >

Inherited by [hybridse::vm::ErrorTableHandler](/Classes/classhybridse_1_1vm_1_1_error_table_handler.md), [hybridse::vm::MemSegmentHandler](/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md), [hybridse::vm::MemTableHandler](/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md), [hybridse::vm::MemTimeTableHandler](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md), [hybridse::vm::PartitionHandler](/Classes/classhybridse_1_1vm_1_1_partition_handler.md), [hybridse::vm::RequestUnionTableHandler](/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md)

## Public Functions

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

## Additional inherited members

**Public Functions inherited from [hybridse::vm::DataHandler](/Classes/classhybridse_1_1vm_1_1_data_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[DataHandler](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-datahandler)**() |
| virtual | **[~DataHandler](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-~datahandler)**() |
| virtual const Schema * | **[GetSchema](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getschema)**() =0 |
| virtual const std::string & | **[GetName](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getname)**() =0 |
| virtual const std::string & | **[GetDatabase](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getdatabase)**() =0 |
| virtual base::Status | **[GetStatus](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getstatus)**() |


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


**Reimplemented by**: [hybridse::vm::MemSegmentHandler::GetTypes](/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md#function-gettypes), [hybridse::vm::ErrorTableHandler::GetTypes](/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-gettypes), [hybridse::vm::MemTableHandler::GetTypes](/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-gettypes), [hybridse::vm::MemTimeTableHandler::GetTypes](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-gettypes), [hybridse::vm::MemPartitionHandler::GetTypes](/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-gettypes), [hybridse::vm::RequestUnionTableHandler::GetTypes](/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-gettypes)


### function GetIndex

```cpp
virtual const IndexHint & GetIndex() =0
```


**Reimplemented by**: [hybridse::vm::MemTableHandler::GetIndex](/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getindex), [hybridse::vm::MemTimeTableHandler::GetIndex](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getindex), [hybridse::vm::MemSegmentHandler::GetIndex](/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md#function-getindex), [hybridse::vm::ErrorTableHandler::GetIndex](/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-getindex), [hybridse::vm::MemPartitionHandler::GetIndex](/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getindex), [hybridse::vm::RequestUnionTableHandler::GetIndex](/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-getindex)


### function GetWindowIterator

```cpp
virtual std::unique_ptr< WindowIterator > GetWindowIterator(
    const std::string & idx_name
) =0
```


**Reimplemented by**: [hybridse::vm::RequestUnionTableHandler::GetWindowIterator](/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-getwindowiterator), [hybridse::vm::ErrorTableHandler::GetWindowIterator](/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-getwindowiterator), [hybridse::vm::PartitionHandler::GetWindowIterator](/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getwindowiterator), [hybridse::vm::MemTableHandler::GetWindowIterator](/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getwindowiterator), [hybridse::vm::MemTimeTableHandler::GetWindowIterator](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getwindowiterator), [hybridse::vm::MemSegmentHandler::GetWindowIterator](/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md#function-getwindowiterator)


### function GetHanlderType

```cpp
inline virtual const HandlerType GetHanlderType() override
```


**Return**: 

**Reimplements**: [hybridse::vm::DataHandler::GetHanlderType](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethanldertype)


**Reimplemented by**: [hybridse::vm::PartitionHandler::GetHanlderType](/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-gethanldertype)


Implemented by subclasses to return the type of [DataHandler](/Classes/classhybridse_1_1vm_1_1_data_handler.md). 


### function GetPartition

```cpp
inline virtual std::shared_ptr< PartitionHandler > GetPartition(
    const std::string & index_name
)
```


### function GetHandlerTypeName

```cpp
inline virtual const std::string GetHandlerTypeName() override
```


**Return**: 

**Reimplements**: [hybridse::vm::DataHandler::GetHandlerTypeName](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethandlertypename)


**Reimplemented by**: [hybridse::vm::ErrorTableHandler::GetHandlerTypeName](/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-gethandlertypename), [hybridse::vm::PartitionHandler::GetHandlerTypeName](/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-gethandlertypename), [hybridse::vm::MemTableHandler::GetHandlerTypeName](/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-gethandlertypename), [hybridse::vm::MemTimeTableHandler::GetHandlerTypeName](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-gethandlertypename), [hybridse::vm::Window::GetHandlerTypeName](/Classes/classhybridse_1_1vm_1_1_window.md#function-gethandlertypename), [hybridse::vm::MemSegmentHandler::GetHandlerTypeName](/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md#function-gethandlertypename), [hybridse::vm::MemPartitionHandler::GetHandlerTypeName](/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-gethandlertypename)


Implemented by subclasses return the name of handler type 


### function GetOrderType

```cpp
inline virtual const OrderType GetOrderType() const
```


**Reimplemented by**: [hybridse::vm::PartitionHandler::GetOrderType](/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getordertype), [hybridse::vm::MemTableHandler::GetOrderType](/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getordertype), [hybridse::vm::MemTimeTableHandler::GetOrderType](/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getordertype), [hybridse::vm::MemSegmentHandler::GetOrderType](/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md#function-getordertype), [hybridse::vm::MemPartitionHandler::GetOrderType](/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getordertype), [hybridse::vm::RequestUnionTableHandler::GetOrderType](/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-getordertype)


### function GetTablet

```cpp
inline virtual std::shared_ptr< Tablet > GetTablet(
    const std::string & index_name,
    const std::string & pk
)
```


### function GetTablet

```cpp
inline virtual std::shared_ptr< Tablet > GetTablet(
    const std::string & index_name,
    const std::vector< std::string > & pks
)
```


-------------------------------

Updated on 28 March 2021 at 19:23:48 PDT