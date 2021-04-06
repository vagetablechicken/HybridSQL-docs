---
title: hybridse::vm::PartitionHandler
summary: The abstraction of partition dataset operation. 

---
# hybridse::vm::PartitionHandler



`#include <catalog.h>`

The abstraction of partition dataset operation. 
## Summary

```cpp
class hybridse::vm::PartitionHandler;
```
The abstraction of partition dataset operation. 

A partition dataset is always organized by segments +&ndash; key1 --> segment1 partition &ndash;+&ndash; key2 --> segment2 +&ndash; key3 --> segment3 



|  Public functions|            |
| -------------- | -------------- |
|**[PartitionHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-partitionhandler)**()|  |
|**[~PartitionHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-~partitionhandler)**()|  |
|**[GetIterator](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getiterator)**()| std::unique_ptr< RowIterator >  |
|**[GetRawIterator](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getrawiterator)**()| RowIterator *  |
|**[GetWindowIterator](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getwindowiterator)**(const std::string & idx_name)| std::unique_ptr< [WindowIterator](hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_window_iterator.md) >  |
|**[GetWindowIterator](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getwindowiterator)**() =0| std::unique_ptr< [WindowIterator](hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_window_iterator.md) >  |
|**[GetHanlderType](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-gethanldertype)**() override| const [HandlerType](hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) <br>Return HandlerType::kPartitionHandler by default.  |
|**[At](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-at)**(uint64_t pos)| [Row](hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) <br>Return empty row, cause partition dataset does not support At operation.  |
|**[GetSegment](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getsegment)**(const std::string & key)| std::shared_ptr< [TableHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md) >  |
|**[GetSegments](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getsegments)**(const std::vector< std::string > & keys)| std::vector< std::shared_ptr< [TableHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md) > >  |
|**[GetHandlerTypeName](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-gethandlertypename)**() override| const std::string <br>Return the name of handler, and return `"PartitionHandler"` by default.  |
|**[GetOrderType](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getordertype)**() const| const [OrderType](hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype)  |

## Inherited members
Inherited by [hybridse::vm::MemPartitionHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md)
Inherited from [hybridse::vm::TableHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md)
| **Inherited public functions** |            |
| -------------- | -------------- |
|**[TableHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-tablehandler)**()| |
|**[~TableHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-~tablehandler)**()| virtual |
|**[GetTypes](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettypes)**() =0| virtual const [Types](hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-types) & <br>Return table column Types information. |
|**[GetIndex](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getindex)**() =0| virtual const [IndexHint](hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-indexhint) & <br>Return the index information. |
|**[GetPartition](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getpartition)**(const std::string & index_name)| virtual std::shared_ptr< [PartitionHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md) > |
|**[GetTablet](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettablet)**(const std::string & index_name, const std::string & pk)| virtual std::shared_ptr< [Tablet](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_tablet.md) > |
|**[GetTablet](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettablet)**(const std::string & index_name, const std::vector< std::string > & pks)| virtual std::shared_ptr< [Tablet](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_tablet.md) > |

Inherited from [hybridse::vm::DataHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md)
| **Inherited public functions** |            |
| -------------- | -------------- |
|**[DataHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-datahandler)**()| |
|**[~DataHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-~datahandler)**()| virtual |
|**[GetSchema](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getschema)**() =0| virtual const Schema * <br>Return table schema. |
|**[GetName](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getname)**() =0| virtual const std::string & <br>Return table name. |
|**[GetDatabase](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getdatabase)**() =0| virtual const std::string & <br>Return the name of database. |
|**[GetStatus](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getstatus)**()| virtual base::Status <br>Return dataset status. Default is hybridse::common::kOk. |

Inherited from [hybridse::codec::ListV< Row >](hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md)
| **Inherited public functions** |            |
| -------------- | -------------- |
|**[ListV](hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-listv)**()| |
|**[~ListV](hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-~listv)**()| virtual |
|**[GetCount](hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getcount)**()| virtual const uint64_t <br>Returns the number of elements in this list. |


## Public Functions

#### function PartitionHandler

```cpp
inline PartitionHandler()
```


#### function ~PartitionHandler

```cpp
inline ~PartitionHandler()
```


#### function GetIterator

```cpp
inline virtual std::unique_ptr< RowIterator > GetIterator()
```


**Reimplements**: [hybridse::codec::ListV::GetIterator](hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getiterator)


Return the iterator of row iterator. Return null by default 


#### function GetRawIterator

```cpp
inline virtual RowIterator * GetRawIterator()
```


**Reimplements**: [hybridse::codec::ListV::GetRawIterator](hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getrawiterator)


Return the iterator of row iterator Return null by default 


#### function GetWindowIterator

```cpp
inline virtual std::unique_ptr< WindowIterator > GetWindowIterator(
    const std::string & idx_name
)
```


**Reimplements**: [hybridse::vm::TableHandler::GetWindowIterator](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getwindowiterator)


Return WindowIterator so that user can use it to iterate datasets segment by segment. 


#### function GetWindowIterator

```cpp
virtual std::unique_ptr< WindowIterator > GetWindowIterator() =0
```


**Reimplemented by**: [hybridse::vm::MemPartitionHandler::GetWindowIterator](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getwindowiterator)


Return WindowIterator to iterate datasets segment-by-segment. 


#### function GetHanlderType

```cpp
inline virtual const HandlerType GetHanlderType() override
```

Return HandlerType::kPartitionHandler by default. 

**Reimplements**: [hybridse::vm::TableHandler::GetHanlderType](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gethanldertype)


#### function At

```cpp
inline virtual Row At(
    uint64_t pos
)
```

Return empty row, cause partition dataset does not support At operation. 

**Reimplements**: [hybridse::codec::ListV::At](hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-at)


#### function GetSegment

```cpp
inline virtual std::shared_ptr< TableHandler > GetSegment(
    const std::string & key
)
```


**Reimplemented by**: [hybridse::vm::MemPartitionHandler::GetSegment](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getsegment)


Return Return table handler of specific segment binding to given key. Return `null` by default. 


#### function GetSegments

```cpp
inline virtual std::vector< std::shared_ptr< TableHandler > > GetSegments(
    const std::vector< std::string > & keys
)
```


Return a sequence of table handles of specify segments binding to given keys set. 


#### function GetHandlerTypeName

```cpp
inline virtual const std::string GetHandlerTypeName() override
```

Return the name of handler, and return `"PartitionHandler"` by default. 

**Reimplements**: [hybridse::vm::TableHandler::GetHandlerTypeName](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gethandlertypename)


**Reimplemented by**: [hybridse::vm::MemPartitionHandler::GetHandlerTypeName](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-gethandlertypename)


#### function GetOrderType

```cpp
inline virtual const OrderType GetOrderType() const
```


**Reimplements**: [hybridse::vm::TableHandler::GetOrderType](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getordertype)


**Reimplemented by**: [hybridse::vm::MemPartitionHandler::GetOrderType](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getordertype)


Return order type of the dataset, and return kNoneOrder by default. 


-------------------------------

Updated on  6 April 2021 at 08:47:46 PDT