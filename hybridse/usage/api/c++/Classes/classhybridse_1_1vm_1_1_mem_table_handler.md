---
title: hybridse::vm::MemTableHandler

---
# hybridse::vm::MemTableHandler



`#include <mem_catalog.h>`

## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[MemTableHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-memtablehandler)**()|  |
|**[MemTableHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-memtablehandler)**(const Schema * schema)|  |
|**[MemTableHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-memtablehandler)**(const std::string & table_name, const std::string & db, const Schema * schema)|  |
|**[~MemTableHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-~memtablehandler)**() override|  |
|**[GetTypes](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-gettypes)**() override| const [Types](hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-types) & <br>Return table column Types information.  |
|**[GetSchema](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getschema)**()| const Schema * <br>Return table schema.  |
|**[GetName](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getname)**()| const std::string & <br>Return table name.  |
|**[GetIndex](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getindex)**()| const [IndexHint](hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-indexhint) & <br>Return the index information.  |
|**[GetDatabase](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getdatabase)**()| const std::string & <br>Return the name of database.  |
|**[GetIterator](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getiterator)**() override| std::unique_ptr< RowIterator > <br>Return the const iterator.  |
|**[GetRawIterator](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getrawiterator)**() override| RowIterator * <br>Return the const iterator raw pointer.  |
|**[GetWindowIterator](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getwindowiterator)**(const std::string & idx_name)| std::unique_ptr< [WindowIterator](hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_window_iterator.md) >  |
|**[AddRow](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-addrow)**(const [Row](hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) & row)| void  |
|**[Reverse](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-reverse)**()| void  |
|**[GetCount](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getcount)**()| const uint64_t <br>Returns the number of elements in this list.  |
|**[At](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-at)**(uint64_t pos)| [Row](hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) <br>Return a the value of element by its position in the list.  |
|**[GetOrderType](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getordertype)**() const| const [OrderType](hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype)  |
|**[SetOrderType](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-setordertype)**(const [OrderType](hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype) order_type)| void  |
|**[GetHandlerTypeName](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-gethandlertypename)**() override| const std::string <br>Return the name of handler and return "TableHandler" by default.  |

## Protected Functions

|Protected functions|           |
| -------------- | -------------- |
|**[Resize](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-resize)**(const size_t size)| void  |
|**[SetRow](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-setrow)**(const size_t idx, const [Row](hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) & row)| bool  |



| **Protected attributes** | |
| -------------- | -------------- |
| **[table_name_](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#variable-table_name_)** | const std::string |
| **[db_](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#variable-db_)** | const std::string |
| **[schema_](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#variable-schema_)** | const Schema * |
| **[types_](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#variable-types_)** | [Types](hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-types) |
| **[index_hint_](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#variable-index_hint_)** | [IndexHint](hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-indexhint) |
| **[table_](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#variable-table_)** | [MemTable](hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-memtable) |
| **[order_type_](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#variable-order_type_)** | [OrderType](hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype) |

## Inherited members
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


## Public Functions

#### function MemTableHandler

```cpp
MemTableHandler()
```


#### function MemTableHandler

```cpp
explicit MemTableHandler(
    const Schema * schema
)
```


#### function MemTableHandler

```cpp
MemTableHandler(
    const std::string & table_name,
    const std::string & db,
    const Schema * schema
)
```


#### function ~MemTableHandler

```cpp
~MemTableHandler() override
```


#### function GetTypes

```cpp
inline virtual const Types & GetTypes() override
```

Return table column Types information. 

**Reimplements**: [hybridse::vm::TableHandler::GetTypes](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettypes)


#### function GetSchema

```cpp
inline virtual const Schema * GetSchema()
```

Return table schema. 

**Reimplements**: [hybridse::vm::DataHandler::GetSchema](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getschema)


#### function GetName

```cpp
inline virtual const std::string & GetName()
```

Return table name. 

**Reimplements**: [hybridse::vm::DataHandler::GetName](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getname)


#### function GetIndex

```cpp
inline virtual const IndexHint & GetIndex()
```

Return the index information. 

**Reimplements**: [hybridse::vm::TableHandler::GetIndex](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getindex)


#### function GetDatabase

```cpp
inline virtual const std::string & GetDatabase()
```

Return the name of database. 

**Reimplements**: [hybridse::vm::DataHandler::GetDatabase](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getdatabase)


#### function GetIterator

```cpp
virtual std::unique_ptr< RowIterator > GetIterator() override
```

Return the const iterator. 

**Reimplements**: [hybridse::codec::ListV::GetIterator](hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getiterator)


#### function GetRawIterator

```cpp
virtual RowIterator * GetRawIterator() override
```

Return the const iterator raw pointer. 

**Reimplements**: [hybridse::codec::ListV::GetRawIterator](hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getrawiterator)


#### function GetWindowIterator

```cpp
virtual std::unique_ptr< WindowIterator > GetWindowIterator(
    const std::string & idx_name
)
```


**Reimplements**: [hybridse::vm::TableHandler::GetWindowIterator](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getwindowiterator)


Return WindowIterator so that user can use it to iterate datasets segment by segment. 


#### function AddRow

```cpp
void AddRow(
    const Row & row
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

**Reimplements**: [hybridse::codec::ListV::GetCount](hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getcount)


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


**Reimplements**: [hybridse::codec::ListV::At](hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-at)


#### function GetOrderType

```cpp
inline virtual const OrderType GetOrderType() const
```


**Reimplements**: [hybridse::vm::TableHandler::GetOrderType](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getordertype)


Return the order type of the dataset, and return OrderType::kNoneOrder by default. 


#### function SetOrderType

```cpp
inline void SetOrderType(
    const OrderType order_type
)
```


#### function GetHandlerTypeName

```cpp
inline virtual const std::string GetHandlerTypeName() override
```

Return the name of handler and return "TableHandler" by default. 

**Reimplements**: [hybridse::vm::TableHandler::GetHandlerTypeName](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gethandlertypename)


## Protected Functions

### function Resize

```cpp
void Resize(
    const size_t size
)
```


### function SetRow

```cpp
bool SetRow(
    const size_t idx,
    const Row & row
)
```


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
MemTable table_;
```


### variable order_type_

```cpp
OrderType order_type_;
```


-------------------------------

Updated on  6 April 2021 at 08:47:46 PDT