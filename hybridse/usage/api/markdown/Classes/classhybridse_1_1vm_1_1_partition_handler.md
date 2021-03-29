---
title: hybridse::vm::PartitionHandler

---

# hybridse::vm::PartitionHandler




`#include <catalog.h>`

Inherits from [hybridse::vm::TableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md), [hybridse::vm::DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md), hybridse::codec::ListV< Row >

Inherited by [hybridse::vm::MemPartitionHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md)

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[PartitionHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-partitionhandler)**() |
| | **[~PartitionHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-~partitionhandler)**() |
| virtual std::unique_ptr< RowIterator > | **[GetIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getiterator)**() |
| RowIterator * | **[GetRawIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getrawiterator)**() |
| virtual std::unique_ptr< WindowIterator > | **[GetWindowIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getwindowiterator)**(const std::string & idx_name) |
| virtual std::unique_ptr< WindowIterator > | **[GetWindowIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getwindowiterator)**() =0 |
| virtual const [HandlerType](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) | **[GetHanlderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-gethanldertype)**() override |
| virtual Row | **[At](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-at)**(uint64_t pos) |
| virtual std::shared_ptr< [TableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md) > | **[GetSegment](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getsegment)**(const std::string & key) |
| virtual std::vector< std::shared_ptr< [TableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md) > > | **[GetSegments](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getsegments)**(const std::vector< std::string > & keys) |
| virtual const std::string | **[GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-gethandlertypename)**() override |
| virtual const [OrderType](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype) | **[GetOrderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getordertype)**() const |

## Additional inherited members

**Public Functions inherited from [hybridse::vm::TableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[TableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-tablehandler)**() |
| virtual | **[~TableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-~tablehandler)**() |
| virtual const [Types](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#typedef-types) & | **[GetTypes](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettypes)**() =0 |
| virtual const [IndexHint](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#typedef-indexhint) & | **[GetIndex](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getindex)**() =0 |
| virtual std::shared_ptr< [PartitionHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md) > | **[GetPartition](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getpartition)**(const std::string & index_name) |
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
| virtual base::Status | **[GetStatus](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getstatus)**() |


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


**Reimplements**: [hybridse::vm::TableHandler::GetWindowIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getwindowiterator)


### function GetWindowIterator

```cpp
virtual std::unique_ptr< WindowIterator > GetWindowIterator() =0
```


**Reimplemented by**: [hybridse::vm::MemPartitionHandler::GetWindowIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getwindowiterator)


### function GetHanlderType

```cpp
inline virtual const HandlerType GetHanlderType() override
```


**Return**: 

**Reimplements**: [hybridse::vm::TableHandler::GetHanlderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gethanldertype)


Implemented by subclasses to return the type of [DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md). 


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


**Reimplemented by**: [hybridse::vm::MemPartitionHandler::GetSegment](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getsegment)


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

**Reimplements**: [hybridse::vm::TableHandler::GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gethandlertypename)


**Reimplemented by**: [hybridse::vm::MemPartitionHandler::GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-gethandlertypename)


Implemented by subclasses return the name of handler type 


### function GetOrderType

```cpp
inline virtual const OrderType GetOrderType() const
```


**Reimplements**: [hybridse::vm::TableHandler::GetOrderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getordertype)


**Reimplemented by**: [hybridse::vm::MemPartitionHandler::GetOrderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getordertype)


-------------------------------

Updated on 28 March 2021 at 19:41:19 PDT