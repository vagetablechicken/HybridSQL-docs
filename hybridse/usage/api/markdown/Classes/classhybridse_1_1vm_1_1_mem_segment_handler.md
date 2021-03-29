---
title: hybridse::vm::MemSegmentHandler

---

# hybridse::vm::MemSegmentHandler




`#include <mem_catalog.h>`

Inherits from [hybridse::vm::TableHandler](/Classes/classhybridse_1_1vm_1_1_table_handler.md), [hybridse::vm::DataHandler](/Classes/classhybridse_1_1vm_1_1_data_handler.md), hybridse::codec::ListV< Row >

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[MemSegmentHandler](/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md#function-memsegmenthandler)**(std::shared_ptr< [PartitionHandler](/Classes/classhybridse_1_1vm_1_1_partition_handler.md) > partition_hander, const std::string & key) |
| virtual | **[~MemSegmentHandler](/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md#function-~memsegmenthandler)**() |
| virtual const vm::Schema * | **[GetSchema](/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md#function-getschema)**() |
| virtual const std::string & | **[GetName](/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md#function-getname)**() |
| virtual const std::string & | **[GetDatabase](/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md#function-getdatabase)**() |
| virtual const [vm::Types](/Namespaces/namespacehybridse_1_1vm.md#typedef-types) & | **[GetTypes](/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md#function-gettypes)**() |
| virtual const [vm::IndexHint](/Namespaces/namespacehybridse_1_1vm.md#typedef-indexhint) & | **[GetIndex](/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md#function-getindex)**() |
| virtual const [OrderType](/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype) | **[GetOrderType](/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md#function-getordertype)**() const |
| std::unique_ptr< vm::RowIterator > | **[GetIterator](/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md#function-getiterator)**() |
| RowIterator * | **[GetRawIterator](/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md#function-getrawiterator)**() override |
| virtual std::unique_ptr< vm::WindowIterator > | **[GetWindowIterator](/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md#function-getwindowiterator)**(const std::string & idx_name) |
| virtual const uint64_t | **[GetCount](/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md#function-getcount)**() |
| Row | **[At](/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md#function-at)**(uint64_t pos) override |
| virtual const std::string | **[GetHandlerTypeName](/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md#function-gethandlertypename)**() override |

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

### function MemSegmentHandler

```cpp
inline MemSegmentHandler(
    std::shared_ptr< PartitionHandler > partition_hander,
    const std::string & key
)
```


### function ~MemSegmentHandler

```cpp
inline virtual ~MemSegmentHandler()
```


### function GetSchema

```cpp
inline virtual const vm::Schema * GetSchema()
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


### function GetDatabase

```cpp
inline virtual const std::string & GetDatabase()
```


**Return**: 

**Reimplements**: [hybridse::vm::DataHandler::GetDatabase](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getdatabase)


Implemented by subclasses to return the name of database. 


### function GetTypes

```cpp
inline virtual const vm::Types & GetTypes()
```


**Reimplements**: [hybridse::vm::TableHandler::GetTypes](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettypes)


### function GetIndex

```cpp
inline virtual const vm::IndexHint & GetIndex()
```


**Reimplements**: [hybridse::vm::TableHandler::GetIndex](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getindex)


### function GetOrderType

```cpp
inline virtual const OrderType GetOrderType() const
```


**Reimplements**: [hybridse::vm::TableHandler::GetOrderType](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getordertype)


### function GetIterator

```cpp
inline std::unique_ptr< vm::RowIterator > GetIterator()
```


### function GetRawIterator

```cpp
inline RowIterator * GetRawIterator() override
```


### function GetWindowIterator

```cpp
inline virtual std::unique_ptr< vm::WindowIterator > GetWindowIterator(
    const std::string & idx_name
)
```


**Reimplements**: [hybridse::vm::TableHandler::GetWindowIterator](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getwindowiterator)


### function GetCount

```cpp
inline virtual const uint64_t GetCount()
```


### function At

```cpp
inline Row At(
    uint64_t pos
) override
```


### function GetHandlerTypeName

```cpp
inline virtual const std::string GetHandlerTypeName() override
```


**Return**: 

**Reimplements**: [hybridse::vm::TableHandler::GetHandlerTypeName](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gethandlertypename)


Implemented by subclasses return the name of handler type 


-------------------------------

Updated on 28 March 2021 at 19:23:48 PDT