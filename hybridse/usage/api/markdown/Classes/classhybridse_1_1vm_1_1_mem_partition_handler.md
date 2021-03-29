---
title: hybridse::vm::MemPartitionHandler

---

# hybridse::vm::MemPartitionHandler




`#include <mem_catalog.h>`

Inherits from [hybridse::vm::PartitionHandler](/Classes/classhybridse_1_1vm_1_1_partition_handler.md), std::enable_shared_from_this< PartitionHandler >, [hybridse::vm::TableHandler](/Classes/classhybridse_1_1vm_1_1_table_handler.md), [hybridse::vm::DataHandler](/Classes/classhybridse_1_1vm_1_1_data_handler.md)

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[MemPartitionHandler](/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-mempartitionhandler)**() |
| | **[MemPartitionHandler](/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-mempartitionhandler)**(const Schema * schema) |
| | **[MemPartitionHandler](/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-mempartitionhandler)**(const std::string & table_name, const std::string & db, const Schema * schema) |
| | **[~MemPartitionHandler](/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-~mempartitionhandler)**() |
| virtual const [Types](/Namespaces/namespacehybridse_1_1vm.md#typedef-types) & | **[GetTypes](/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-gettypes)**() override |
| virtual const [IndexHint](/Namespaces/namespacehybridse_1_1vm.md#typedef-indexhint) & | **[GetIndex](/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getindex)**() override |
| virtual const Schema * | **[GetSchema](/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getschema)**() override |
| virtual const std::string & | **[GetName](/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getname)**() override |
| virtual const std::string & | **[GetDatabase](/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getdatabase)**() override |
| virtual std::unique_ptr< WindowIterator > | **[GetWindowIterator](/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getwindowiterator)**() |
| bool | **[AddRow](/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-addrow)**(const std::string & key, uint64_t ts, const Row & row) |
| void | **[Sort](/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-sort)**(const bool is_asc) |
| void | **[Reverse](/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-reverse)**() |
| void | **[Print](/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-print)**() |
| virtual const uint64_t | **[GetCount](/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getcount)**() |
| virtual std::shared_ptr< [TableHandler](/Classes/classhybridse_1_1vm_1_1_table_handler.md) > | **[GetSegment](/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getsegment)**(const std::string & key) |
| void | **[SetOrderType](/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-setordertype)**(const [OrderType](/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype) order_type) |
| virtual const [OrderType](/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype) | **[GetOrderType](/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getordertype)**() const |
| virtual const std::string | **[GetHandlerTypeName](/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-gethandlertypename)**() override |

## Additional inherited members

**Public Functions inherited from [hybridse::vm::PartitionHandler](/Classes/classhybridse_1_1vm_1_1_partition_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[PartitionHandler](/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-partitionhandler)**() |
| | **[~PartitionHandler](/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-~partitionhandler)**() |
| virtual std::unique_ptr< RowIterator > | **[GetIterator](/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getiterator)**() |
| RowIterator * | **[GetRawIterator](/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getrawiterator)**() |
| virtual const [HandlerType](/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) | **[GetHanlderType](/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-gethanldertype)**() override |
| virtual Row | **[At](/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-at)**(uint64_t pos) |
| virtual std::vector< std::shared_ptr< [TableHandler](/Classes/classhybridse_1_1vm_1_1_table_handler.md) > > | **[GetSegments](/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getsegments)**(const std::vector< std::string > & keys) |

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

### function MemPartitionHandler

```cpp
MemPartitionHandler()
```


### function MemPartitionHandler

```cpp
explicit MemPartitionHandler(
    const Schema * schema
)
```


### function MemPartitionHandler

```cpp
MemPartitionHandler(
    const std::string & table_name,
    const std::string & db,
    const Schema * schema
)
```


### function ~MemPartitionHandler

```cpp
~MemPartitionHandler()
```


### function GetTypes

```cpp
virtual const Types & GetTypes() override
```


**Reimplements**: [hybridse::vm::TableHandler::GetTypes](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettypes)


### function GetIndex

```cpp
virtual const IndexHint & GetIndex() override
```


**Reimplements**: [hybridse::vm::TableHandler::GetIndex](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getindex)


### function GetSchema

```cpp
virtual const Schema * GetSchema() override
```


**Return**: 

**Reimplements**: [hybridse::vm::DataHandler::GetSchema](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getschema)


Implemented by subclasses to return table schema. 


### function GetName

```cpp
virtual const std::string & GetName() override
```


**Return**: 

**Reimplements**: [hybridse::vm::DataHandler::GetName](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getname)


Implemented by subclasses to return table name. 


### function GetDatabase

```cpp
virtual const std::string & GetDatabase() override
```


**Return**: 

**Reimplements**: [hybridse::vm::DataHandler::GetDatabase](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getdatabase)


Implemented by subclasses to return the name of database. 


### function GetWindowIterator

```cpp
virtual std::unique_ptr< WindowIterator > GetWindowIterator()
```


**Reimplements**: [hybridse::vm::PartitionHandler::GetWindowIterator](/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getwindowiterator)


### function AddRow

```cpp
bool AddRow(
    const std::string & key,
    uint64_t ts,
    const Row & row
)
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


### function Print

```cpp
void Print()
```


### function GetCount

```cpp
inline virtual const uint64_t GetCount()
```


### function GetSegment

```cpp
inline virtual std::shared_ptr< TableHandler > GetSegment(
    const std::string & key
)
```


**Reimplements**: [hybridse::vm::PartitionHandler::GetSegment](/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getsegment)


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


**Reimplements**: [hybridse::vm::PartitionHandler::GetOrderType](/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getordertype)


### function GetHandlerTypeName

```cpp
inline virtual const std::string GetHandlerTypeName() override
```


**Return**: 

**Reimplements**: [hybridse::vm::PartitionHandler::GetHandlerTypeName](/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-gethandlertypename)


Implemented by subclasses return the name of handler type 


-------------------------------

Updated on 28 March 2021 at 19:23:48 PDT