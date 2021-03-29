---
title: hybridse::vm::PartitionHandler

---

# hybridse::vm::PartitionHandler




`#include <catalog.h>`

Inherits from [hybridse::vm::TableHandler](/Classes/classhybridse_1_1vm_1_1_table_handler.md), [hybridse::vm::DataHandler](/Classes/classhybridse_1_1vm_1_1_data_handler.md), hybridse::codec::ListV< Row >

Inherited by [hybridse::vm::MemPartitionHandler](/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md)

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[PartitionHandler](/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-partitionhandler)**() |
| | **[~PartitionHandler](/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-~partitionhandler)**() |
| virtual std::unique_ptr< RowIterator > | **[GetIterator](/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getiterator)**() |
| RowIterator * | **[GetRawIterator](/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getrawiterator)**() |
| virtual std::unique_ptr< WindowIterator > | **[GetWindowIterator](/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getwindowiterator)**(const std::string & idx_name) |
| virtual std::unique_ptr< WindowIterator > | **[GetWindowIterator](/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getwindowiterator)**() =0 |
| virtual const [HandlerType](/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) | **[GetHanlderType](/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-gethanldertype)**() override |
| virtual Row | **[At](/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-at)**(uint64_t pos) |
| virtual std::shared_ptr< [TableHandler](/Classes/classhybridse_1_1vm_1_1_table_handler.md) > | **[GetSegment](/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getsegment)**(const std::string & key) |
| virtual std::vector< std::shared_ptr< [TableHandler](/Classes/classhybridse_1_1vm_1_1_table_handler.md) > > | **[GetSegments](/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getsegments)**(const std::vector< std::string > & keys) |
| virtual const std::string | **[GetHandlerTypeName](/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-gethandlertypename)**() override |
| virtual const [OrderType](/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype) | **[GetOrderType](/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getordertype)**() const |

## Additional inherited members

**Public Functions inherited from [hybridse::vm::TableHandler](/Classes/classhybridse_1_1vm_1_1_table_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[TableHandler](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-tablehandler)**() |
| virtual | **[~TableHandler](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-~tablehandler)**() |
| virtual const [Types](/Namespaces/namespacehybridse_1_1vm.md#typedef-types) & | **[GetTypes](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettypes)**() =0 |
| virtual const [IndexHint](/Namespaces/namespacehybridse_1_1vm.md#typedef-indexhint) & | **[GetIndex](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getindex)**() =0 |
| virtual std::shared_ptr< [PartitionHandler](/Classes/classhybridse_1_1vm_1_1_partition_handler.md) > | **[GetPartition](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getpartition)**(const std::string & index_name) |
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
| virtual base::Status | **[GetStatus](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getstatus)**() |


## Public Functions Documentation

### function PartitionHandler

```cpp
inline PartitionHandler()
```


### function ~PartitionHandler

```cpp
inline ~PartitionHandler()
```


### function GetIterator

```cpp
inline virtual std::unique_ptr< RowIterator > GetIterator()
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


### function GetWindowIterator

```cpp
virtual std::unique_ptr< WindowIterator > GetWindowIterator() =0
```


**Reimplemented by**: [hybridse::vm::MemPartitionHandler::GetWindowIterator](/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getwindowiterator)


### function GetHanlderType

```cpp
inline virtual const HandlerType GetHanlderType() override
```


**Return**: 

**Reimplements**: [hybridse::vm::TableHandler::GetHanlderType](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gethanldertype)


Implemented by subclasses to return the type of [DataHandler](/Classes/classhybridse_1_1vm_1_1_data_handler.md). 


### function At

```cpp
inline virtual Row At(
    uint64_t pos
)
```


### function GetSegment

```cpp
inline virtual std::shared_ptr< TableHandler > GetSegment(
    const std::string & key
)
```


**Reimplemented by**: [hybridse::vm::MemPartitionHandler::GetSegment](/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getsegment)


### function GetSegments

```cpp
inline virtual std::vector< std::shared_ptr< TableHandler > > GetSegments(
    const std::vector< std::string > & keys
)
```


### function GetHandlerTypeName

```cpp
inline virtual const std::string GetHandlerTypeName() override
```


**Return**: 

**Reimplements**: [hybridse::vm::TableHandler::GetHandlerTypeName](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gethandlertypename)


**Reimplemented by**: [hybridse::vm::MemPartitionHandler::GetHandlerTypeName](/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-gethandlertypename)


Implemented by subclasses return the name of handler type 


### function GetOrderType

```cpp
inline virtual const OrderType GetOrderType() const
```


**Reimplements**: [hybridse::vm::TableHandler::GetOrderType](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getordertype)


**Reimplemented by**: [hybridse::vm::MemPartitionHandler::GetOrderType](/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getordertype)


-------------------------------

Updated on 28 March 2021 at 19:23:48 PDT