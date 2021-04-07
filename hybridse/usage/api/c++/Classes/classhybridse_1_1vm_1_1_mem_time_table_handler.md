---
title: hybridse::vm::MemTimeTableHandler

---
# hybridse::vm::MemTimeTableHandler



`#include <mem_catalog.h>`

## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[MemTimeTableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-memtimetablehandler)**()|  |
|**[MemTimeTableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-memtimetablehandler)**(const Schema * schema)|  |
|**[MemTimeTableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-memtimetablehandler)**(const std::string & table_name, const std::string & db, const Schema * schema)|  |
|**[GetTypes](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-gettypes)**() override| const [Types](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-types) & <br>Return table column Types information.  |
|**[~MemTimeTableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-~memtimetablehandler)**() override|  |
|**[GetSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getschema)**()| const Schema * <br>Return table schema.  |
|**[GetName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getname)**()| const std::string & <br>Return table name.  |
|**[GetIndex](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getindex)**()| const [IndexHint](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-indexhint) & <br>Return the index information.  |
|**[GetIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getiterator)**()| std::unique_ptr< RowIterator > <br>Return the const iterator.  |
|**[GetRawIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getrawiterator)**()| RowIterator * <br>Return the const iterator raw pointer.  |
|**[GetDatabase](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getdatabase)**()| const std::string & <br>Return the name of database.  |
|**[GetWindowIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getwindowiterator)**(const std::string & idx_name)| std::unique_ptr< [WindowIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_window_iterator.md) >  |
|**[AddRow](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-addrow)**(const uint64_t key, const [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) & v)| void  |
|**[AddFrontRow](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-addfrontrow)**(const uint64_t key, const [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) & v)| void  |
|**[PopBackRow](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-popbackrow)**()| void  |
|**[PopFrontRow](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-popfrontrow)**()| void  |
|**[GetFrontRow](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getfrontrow)**()| const std::pair< uint64_t, [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) > &  |
|**[GetBackRow](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getbackrow)**()| const std::pair< uint64_t, [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) > &  |
|**[Sort](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-sort)**(const bool is_asc)| void  |
|**[Reverse](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-reverse)**()| void  |
|**[GetCount](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getcount)**()| const uint64_t <br>Returns the number of elements in this list.  |
|**[At](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-at)**(uint64_t pos)| [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) <br>Return a the value of element by its position in the list.  |
|**[SetOrderType](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-setordertype)**(const [OrderType](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype) order_type)| void  |
|**[GetOrderType](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getordertype)**() const| const [OrderType](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype)  |
|**[GetHandlerTypeName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-gethandlertypename)**() override| const std::string <br>Return the name of handler and return "TableHandler" by default.  |



| **Protected attributes** | |
| -------------- | -------------- |
| **[table_name_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-table_name_)** | const std::string |
| **[db_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-db_)** | const std::string |
| **[schema_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-schema_)** | const Schema * |
| **[types_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-types_)** | [Types](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-types) |
| **[index_hint_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-index_hint_)** | [IndexHint](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-indexhint) |
| **[table_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-table_)** | [MemTimeTable](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-memtimetable) |
| **[order_type_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-order_type_)** | [OrderType](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype) |

## Inherited members
Inherited by [hybridse::vm::ConcatTableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_concat_table_handler.md), [hybridse::vm::Window](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window.md)
Inherited from [hybridse::vm::TableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md)
|  Inherited Public functions|            |
| -------------- | -------------- |
|**[TableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-tablehandler)**()|  |
|**[~TableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-~tablehandler)**()|  |
|**[GetHanlderType](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gethanldertype)**() override| const [HandlerType](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype)  |
|**[GetPartition](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getpartition)**(const std::string & index_name)| std::shared_ptr< [PartitionHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md) >  |
|**[GetTablet](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettablet)**(const std::string & index_name, const std::string & pk)| std::shared_ptr< [Tablet](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_tablet.md) >  |
|**[GetTablet](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettablet)**(const std::string & index_name, const std::vector< std::string > & pks)| std::shared_ptr< [Tablet](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_tablet.md) >  |

Inherited from [hybridse::vm::DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md)
|  Inherited Public functions|            |
| -------------- | -------------- |
|**[DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-datahandler)**()|  |
|**[~DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-~datahandler)**()|  |
|**[GetHanlderType](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethanldertype)**() =0| const [HandlerType](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) <br>Return the type of [DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md).  |
|**[GetStatus](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getstatus)**()| base::Status <br>Return dataset status. Default is hybridse::common::kOk.  |

Inherited from [hybridse::codec::ListV< Row >](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md)
|  Inherited Public functions|            |
| -------------- | -------------- |
|**[ListV](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-listv)**()|  |
|**[~ListV](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-~listv)**()|  |


## Public Functions

#### function MemTimeTableHandler

```cpp
MemTimeTableHandler()
```


#### function MemTimeTableHandler

```cpp
explicit MemTimeTableHandler(
    const Schema * schema
)
```


#### function MemTimeTableHandler

```cpp
MemTimeTableHandler(
    const std::string & table_name,
    const std::string & db,
    const Schema * schema
)
```


#### function GetTypes

```cpp
virtual const Types & GetTypes() override
```

Return table column Types information. 

**Reimplements**: [hybridse::vm::TableHandler::GetTypes](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettypes)


#### function ~MemTimeTableHandler

```cpp
~MemTimeTableHandler() override
```


#### function GetSchema

```cpp
inline virtual const Schema * GetSchema()
```

Return table schema. 

**Reimplements**: [hybridse::vm::DataHandler::GetSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getschema)


#### function GetName

```cpp
inline virtual const std::string & GetName()
```

Return table name. 

**Reimplements**: [hybridse::vm::DataHandler::GetName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getname)


#### function GetIndex

```cpp
inline virtual const IndexHint & GetIndex()
```

Return the index information. 

**Reimplements**: [hybridse::vm::TableHandler::GetIndex](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getindex)


#### function GetIterator

```cpp
virtual std::unique_ptr< RowIterator > GetIterator()
```

Return the const iterator. 

**Reimplements**: [hybridse::codec::ListV::GetIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getiterator)


**Reimplemented by**: [hybridse::vm::ConcatTableHandler::GetIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_concat_table_handler.md#function-getiterator), [hybridse::vm::Window::GetIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window.md#function-getiterator)


#### function GetRawIterator

```cpp
virtual RowIterator * GetRawIterator()
```

Return the const iterator raw pointer. 

**Reimplements**: [hybridse::codec::ListV::GetRawIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getrawiterator)


**Reimplemented by**: [hybridse::vm::Window::GetRawIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window.md#function-getrawiterator), [hybridse::vm::ConcatTableHandler::GetRawIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_concat_table_handler.md#function-getrawiterator)


#### function GetDatabase

```cpp
inline virtual const std::string & GetDatabase()
```

Return the name of database. 

**Reimplements**: [hybridse::vm::DataHandler::GetDatabase](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getdatabase)


#### function GetWindowIterator

```cpp
virtual std::unique_ptr< WindowIterator > GetWindowIterator(
    const std::string & idx_name
)
```


**Reimplements**: [hybridse::vm::TableHandler::GetWindowIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getwindowiterator)


Return WindowIterator so that user can use it to iterate datasets segment by segment. 

#### function AddRow

```cpp
void AddRow(
    const uint64_t key,
    const Row & v
)
```


#### function AddFrontRow

```cpp
void AddFrontRow(
    const uint64_t key,
    const Row & v
)
```


#### function PopBackRow

```cpp
void PopBackRow()
```


#### function PopFrontRow

```cpp
void PopFrontRow()
```


#### function GetFrontRow

```cpp
inline virtual const std::pair< uint64_t, Row > & GetFrontRow()
```


#### function GetBackRow

```cpp
inline virtual const std::pair< uint64_t, Row > & GetBackRow()
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


#### function GetCount

```cpp
inline virtual const uint64_t GetCount()
```

Returns the number of elements in this list. 

**Reimplements**: [hybridse::codec::ListV::GetCount](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getcount)


**Reimplemented by**: [hybridse::vm::Window::GetCount](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window.md#function-getcount), [hybridse::vm::ConcatTableHandler::GetCount](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_concat_table_handler.md#function-getcount)


It count element by traverse the list 

#### function At

```cpp
inline virtual Row At(
    uint64_t pos
)
```

Return a the value of element by its position in the list. 

**Parameters**: 

  * **pos** is element position in the list 


**Reimplements**: [hybridse::codec::ListV::At](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-at)


**Reimplemented by**: [hybridse::vm::Window::At](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window.md#function-at), [hybridse::vm::ConcatTableHandler::At](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_concat_table_handler.md#function-at)


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


**Reimplements**: [hybridse::vm::TableHandler::GetOrderType](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getordertype)


Return the order type of the dataset, and return OrderType::kNoneOrder by default. 

#### function GetHandlerTypeName

```cpp
inline virtual const std::string GetHandlerTypeName() override
```

Return the name of handler and return "TableHandler" by default. 

**Reimplements**: [hybridse::vm::TableHandler::GetHandlerTypeName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gethandlertypename)


**Reimplemented by**: [hybridse::vm::Window::GetHandlerTypeName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window.md#function-gethandlertypename)


## Protected Attributes

### variable table_name_

```cpp
const std::string table_name_;
```


### variable db_

```cpp
const std::string db_;
```


### variable schema_

```cpp
const Schema * schema_;
```


### variable types_

```cpp
Types types_;
```


### variable index_hint_

```cpp
IndexHint index_hint_;
```


### variable table_

```cpp
MemTimeTable table_;
```


### variable order_type_

```cpp
OrderType order_type_;
```


-------------------------------

Updated on  6 April 2021 at 19:38:01 PDT