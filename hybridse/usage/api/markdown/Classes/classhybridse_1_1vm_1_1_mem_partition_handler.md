---
title: hybridse::vm::MemPartitionHandler

---

# hybridse::vm::MemPartitionHandler




`#include <mem_catalog.h>`

Inherits from [hybridse::vm::PartitionHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md), std::enable_shared_from_this< PartitionHandler >, [hybridse::vm::TableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md), [hybridse::vm::DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md), [hybridse::codec::ListV< Row >](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md)

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[MemPartitionHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-mempartitionhandler)**() |
| | **[MemPartitionHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-mempartitionhandler)**(const Schema * schema) |
| | **[MemPartitionHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-mempartitionhandler)**(const std::string & table_name, const std::string & db, const Schema * schema) |
| | **[~MemPartitionHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-~mempartitionhandler)**() |
| virtual const [Types](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#typedef-types) & | **[GetTypes](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-gettypes)**() override<br>Implemented by subclasses to return table column Types information.  |
| virtual const [IndexHint](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#typedef-indexhint) & | **[GetIndex](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getindex)**() override<br>Return the index information.  |
| virtual const Schema * | **[GetSchema](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getschema)**() override<br>Implemented by subclasses to return table schema.  |
| virtual const std::string & | **[GetName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getname)**() override<br>Implemented by subclasses to return table name.  |
| virtual const std::string & | **[GetDatabase](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getdatabase)**() override<br>Implemented by subclasses to return the name of database.  |
| virtual std::unique_ptr< [WindowIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_window_iterator.md) > | **[GetWindowIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getwindowiterator)**() |
| bool | **[AddRow](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-addrow)**(const std::string & key, uint64_t ts, const [Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md) & row) |
| void | **[Sort](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-sort)**(const bool is_asc) |
| void | **[Reverse](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-reverse)**() |
| void | **[Print](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-print)**() |
| virtual const uint64_t | **[GetCount](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getcount)**()<br>Returns the number of elements in this list.  |
| virtual std::shared_ptr< [TableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md) > | **[GetSegment](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getsegment)**(const std::string & key) |
| void | **[SetOrderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-setordertype)**(const [OrderType](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype) order_type) |
| virtual const [OrderType](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype) | **[GetOrderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getordertype)**() const |
| virtual const std::string | **[GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-gethandlertypename)**() override<br>Return the name of handler, and return `"PartitionHandler"` by default.  |

## Additional inherited members

**Public Functions inherited from [hybridse::vm::PartitionHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[PartitionHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-partitionhandler)**() |
| | **[~PartitionHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-~partitionhandler)**() |
| virtual std::unique_ptr< RowIterator > | **[GetIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getiterator)**() |
| virtual RowIterator * | **[GetRawIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getrawiterator)**() |
| virtual const [HandlerType](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) | **[GetHanlderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-gethanldertype)**() override<br>Return HandlerType::kPartitionHandler by default.  |
| virtual [Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md) | **[At](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-at)**(uint64_t pos)<br>Return empty row, cause partition dataset does not support At operation.  |
| virtual std::vector< std::shared_ptr< [TableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md) > > | **[GetSegments](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getsegments)**(const std::vector< std::string > & keys) |

**Public Functions inherited from [hybridse::vm::TableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[TableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-tablehandler)**() |
| virtual | **[~TableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-~tablehandler)**() |
| virtual const [HandlerType](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) | **[GetHanlderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gethanldertype)**() override |
| virtual std::shared_ptr< [PartitionHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md) > | **[GetPartition](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getpartition)**(const std::string & index_name) |
| virtual std::shared_ptr< [Tablet](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_tablet.md) > | **[GetTablet](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettablet)**(const std::string & index_name, const std::string & pk) |
| virtual std::shared_ptr< [Tablet](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_tablet.md) > | **[GetTablet](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettablet)**(const std::string & index_name, const std::vector< std::string > & pks) |

**Public Functions inherited from [hybridse::vm::DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-datahandler)**() |
| virtual | **[~DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-~datahandler)**() |
| virtual const [HandlerType](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) | **[GetHanlderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethanldertype)**() =0<br>Implemented by subclasses to return the type of [DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md).  |
| virtual base::Status | **[GetStatus](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getstatus)**()<br>Return dataset status. Default is hybridse::common::kOk.  |

**Public Functions inherited from [hybridse::codec::ListV< Row >](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md)**

|                | Name           |
| -------------- | -------------- |
| | **[ListV](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md#function-listv)**() |
| virtual | **[~ListV](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md#function-~listv)**() |
| virtual std::unique_ptr< [ConstIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1base_1_1_const_iterator.md)< uint64_t, V > > | **[GetIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getiterator)**() =0<br>Implemented by subclasses to return the const iterator.  |
| virtual [ConstIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1base_1_1_const_iterator.md)< uint64_t, V > * | **[GetRawIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getrawiterator)**() =0<br>Implemented by subclasses to return the const iterator raw pointer.  |
| virtual V | **[At](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md#function-at)**(uint64_t pos) |


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

Implemented by subclasses to return table column Types information. 

**Reimplements**: [hybridse::vm::TableHandler::GetTypes](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettypes)


### function GetIndex

```cpp
virtual const IndexHint & GetIndex() override
```

Return the index information. 

**Reimplements**: [hybridse::vm::TableHandler::GetIndex](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getindex)


### function GetSchema

```cpp
virtual const Schema * GetSchema() override
```

Implemented by subclasses to return table schema. 

**Reimplements**: [hybridse::vm::DataHandler::GetSchema](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getschema)


### function GetName

```cpp
virtual const std::string & GetName() override
```

Implemented by subclasses to return table name. 

**Reimplements**: [hybridse::vm::DataHandler::GetName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getname)


### function GetDatabase

```cpp
virtual const std::string & GetDatabase() override
```

Implemented by subclasses to return the name of database. 

**Reimplements**: [hybridse::vm::DataHandler::GetDatabase](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getdatabase)


### function GetWindowIterator

```cpp
virtual std::unique_ptr< WindowIterator > GetWindowIterator()
```


**Reimplements**: [hybridse::vm::PartitionHandler::GetWindowIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getwindowiterator)


Implemented by subclasses to return WindowIterator to iterate datasets segment-by-segment. 


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

Returns the number of elements in this list. 

**Reimplements**: [hybridse::codec::ListV::GetCount](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getcount)


It count element by traverse the list 


### function GetSegment

```cpp
inline virtual std::shared_ptr< TableHandler > GetSegment(
    const std::string & key
)
```


**Reimplements**: [hybridse::vm::PartitionHandler::GetSegment](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getsegment)


Return Return table handler of specific segment binding to given key. Return `null` by default. 


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


**Reimplements**: [hybridse::vm::PartitionHandler::GetOrderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getordertype)


Implemented by subclasses to return order type of the dataset, and return kNoneOrder by default. 


### function GetHandlerTypeName

```cpp
inline virtual const std::string GetHandlerTypeName() override
```

Return the name of handler, and return `"PartitionHandler"` by default. 

**Reimplements**: [hybridse::vm::PartitionHandler::GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-gethandlertypename)


-------------------------------

Updated on 29 March 2021 at 10:12:21 PDT