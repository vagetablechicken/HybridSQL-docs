---
title: hybridse::vm::MemPartitionHandler

---
# hybridse::vm::MemPartitionHandler



`#include <mem_catalog.h>`

## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[MemPartitionHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-mempartitionhandler)**()|  |
|**[MemPartitionHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-mempartitionhandler)**(const Schema * schema)|  |
|**[MemPartitionHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-mempartitionhandler)**(const std::string & table_name, const std::string & db, const Schema * schema)|  |
|**[~MemPartitionHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-~mempartitionhandler)**()|  |
|**[GetTypes](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-gettypes)**() override| const [Types](hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-types) & <br>Return table column Types information.  |
|**[GetIndex](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getindex)**() override| const [IndexHint](hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-indexhint) & <br>Return the index information.  |
|**[GetSchema](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getschema)**() override| const Schema * <br>Return table schema.  |
|**[GetName](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getname)**() override| const std::string & <br>Return table name.  |
|**[GetDatabase](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getdatabase)**() override| const std::string & <br>Return the name of database.  |
|**[GetWindowIterator](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getwindowiterator)**()| std::unique_ptr< [WindowIterator](hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_window_iterator.md) >  |
|**[AddRow](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-addrow)**(const std::string & key, uint64_t ts, const [Row](hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) & row)| bool  |
|**[Sort](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-sort)**(const bool is_asc)| void  |
|**[Reverse](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-reverse)**()| void  |
|**[Print](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-print)**()| void  |
|**[GetCount](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getcount)**()| const uint64_t <br>Returns the number of elements in this list.  |
|**[GetSegment](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getsegment)**(const std::string & key)| std::shared_ptr< [TableHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md) >  |
|**[SetOrderType](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-setordertype)**(const [OrderType](hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype) order_type)| void  |
|**[GetOrderType](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getordertype)**() const| const [OrderType](hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype)  |
|**[GetHandlerTypeName](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-gethandlertypename)**() override| const std::string <br>Return the name of handler, and return `"PartitionHandler"` by default.  |

## Inherited members
Inherited from [hybridse::vm::PartitionHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md)
| **Inherited public functions** |            |
| -------------- | -------------- |
|**[PartitionHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-partitionhandler)**()| |
|**[~PartitionHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-~partitionhandler)**()| |
|**[GetIterator](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getiterator)**()| virtual std::unique_ptr< RowIterator > |
|**[GetRawIterator](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getrawiterator)**()| virtual RowIterator * |
|**[GetHanlderType](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-gethanldertype)**() override| virtual const [HandlerType](hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) <br>Return HandlerType::kPartitionHandler by default. |
|**[At](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-at)**(uint64_t pos)| virtual [Row](hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) <br>Return empty row, cause partition dataset does not support At operation. |
|**[GetSegments](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getsegments)**(const std::vector< std::string > & keys)| virtual std::vector< std::shared_ptr< [TableHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md) > > |

std::enable_shared_from_this< PartitionHandler >
Inherited from [hybridse::vm::TableHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md)
| **Inherited public functions** |            |
| -------------- | -------------- |
|**[TableHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-tablehandler)**()| |
|**[~TableHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-~tablehandler)**()| virtual |
|**[GetHanlderType](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gethanldertype)**() override| virtual const [HandlerType](hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) |
|**[GetPartition](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getpartition)**(const std::string & index_name)| virtual std::shared_ptr< [PartitionHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md) > |
|**[GetTablet](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettablet)**(const std::string & index_name, const std::string & pk)| virtual std::shared_ptr< [Tablet](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_tablet.md) > |
|**[GetTablet](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettablet)**(const std::string & index_name, const std::vector< std::string > & pks)| virtual std::shared_ptr< [Tablet](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_tablet.md) > |

Inherited from [hybridse::vm::DataHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md)
| **Inherited public functions** |            |
| -------------- | -------------- |
|**[DataHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-datahandler)**()| |
|**[~DataHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-~datahandler)**()| virtual |
|**[GetHanlderType](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethanldertype)**() =0| virtual const [HandlerType](hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) <br>Return the type of [DataHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md). |
|**[GetStatus](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getstatus)**()| virtual base::Status <br>Return dataset status. Default is hybridse::common::kOk. |

Inherited from [hybridse::codec::ListV< Row >](hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md)
| **Inherited public functions** |            |
| -------------- | -------------- |
|**[ListV](hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-listv)**()| |
|**[~ListV](hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-~listv)**()| virtual |
|**[GetIterator](hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getiterator)**() =0| virtual std::unique_ptr< [ConstIterator](hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_const_iterator.md)< uint64_t, V > > <br>Return the const iterator. |
|**[GetRawIterator](hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getrawiterator)**() =0| virtual [ConstIterator](hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_const_iterator.md)< uint64_t, V > * <br>Return the const iterator raw pointer. |
|**[At](hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-at)**(uint64_t pos)| virtual V <br>Return a the value of element by its position in the list. |


## Public Functions

#### function MemPartitionHandler

```cpp
MemPartitionHandler()
```


#### function MemPartitionHandler

```cpp
explicit MemPartitionHandler(
    const Schema * schema
)
```


#### function MemPartitionHandler

```cpp
MemPartitionHandler(
    const std::string & table_name,
    const std::string & db,
    const Schema * schema
)
```


#### function ~MemPartitionHandler

```cpp
~MemPartitionHandler()
```


#### function GetTypes

```cpp
virtual const Types & GetTypes() override
```

Return table column Types information. 

**Reimplements**: [hybridse::vm::TableHandler::GetTypes](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettypes)


#### function GetIndex

```cpp
virtual const IndexHint & GetIndex() override
```

Return the index information. 

**Reimplements**: [hybridse::vm::TableHandler::GetIndex](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getindex)


#### function GetSchema

```cpp
virtual const Schema * GetSchema() override
```

Return table schema. 

**Reimplements**: [hybridse::vm::DataHandler::GetSchema](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getschema)


#### function GetName

```cpp
virtual const std::string & GetName() override
```

Return table name. 

**Reimplements**: [hybridse::vm::DataHandler::GetName](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getname)


#### function GetDatabase

```cpp
virtual const std::string & GetDatabase() override
```

Return the name of database. 

**Reimplements**: [hybridse::vm::DataHandler::GetDatabase](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getdatabase)


#### function GetWindowIterator

```cpp
virtual std::unique_ptr< WindowIterator > GetWindowIterator()
```


**Reimplements**: [hybridse::vm::PartitionHandler::GetWindowIterator](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getwindowiterator)


Return WindowIterator to iterate datasets segment-by-segment. 


#### function AddRow

```cpp
bool AddRow(
    const std::string & key,
    uint64_t ts,
    const Row & row
)
```


#### function Sort

```cpp
void Sort(
    const bool is_asc
)
```


#### function Reverse

```cpp
void Reverse()
```


#### function Print

```cpp
void Print()
```


#### function GetCount

```cpp
inline virtual const uint64_t GetCount()
```

Returns the number of elements in this list. 

**Reimplements**: [hybridse::codec::ListV::GetCount](hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getcount)


It count element by traverse the list 


#### function GetSegment

```cpp
inline virtual std::shared_ptr< TableHandler > GetSegment(
    const std::string & key
)
```


**Reimplements**: [hybridse::vm::PartitionHandler::GetSegment](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getsegment)


Return Return table handler of specific segment binding to given key. Return `null` by default. 


#### function SetOrderType

```cpp
inline void SetOrderType(
    const OrderType order_type
)
```


#### function GetOrderType

```cpp
inline virtual const OrderType GetOrderType() const
```


**Reimplements**: [hybridse::vm::PartitionHandler::GetOrderType](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getordertype)


Return order type of the dataset, and return kNoneOrder by default. 


#### function GetHandlerTypeName

```cpp
inline virtual const std::string GetHandlerTypeName() override
```

Return the name of handler, and return `"PartitionHandler"` by default. 

**Reimplements**: [hybridse::vm::PartitionHandler::GetHandlerTypeName](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-gethandlertypename)


-------------------------------

Updated on  6 April 2021 at 08:47:46 PDT