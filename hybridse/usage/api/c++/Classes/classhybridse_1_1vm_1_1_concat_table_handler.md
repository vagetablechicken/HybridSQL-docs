---
title: hybridse::vm::ConcatTableHandler

---
# hybridse::vm::ConcatTableHandler



`#include <mem_catalog.h>`

## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[ConcatTableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_concat_table_handler.md#function-concattablehandler)**(std::shared_ptr< [TableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md) > left, size_t left_slices, std::shared_ptr< [TableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md) > right, size_t right_slices)|  |
|**[~ConcatTableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_concat_table_handler.md#function-~concattablehandler)**()|  |
|**[At](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_concat_table_handler.md#function-at)**(uint64_t pos) override| [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) <br>Return a the value of element by its position in the list.  |
|**[GetIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_concat_table_handler.md#function-getiterator)**()| std::unique_ptr< RowIterator > <br>Return the const iterator.  |
|**[GetRawIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_concat_table_handler.md#function-getrawiterator)**()| RowIterator * <br>Return the const iterator raw pointer.  |
|**[GetCount](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_concat_table_handler.md#function-getcount)**()| const uint64_t <br>Returns the number of elements in this list.  |

## Inherited members
Inherited from [hybridse::vm::MemTimeTableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md)
}

|  Inherited Public functions|            |
| -------------- | -------------- |
|**[MemTimeTableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-memtimetablehandler)**()|  |
|**[MemTimeTableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-memtimetablehandler)**(const Schema * schema)|  |
|**[MemTimeTableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-memtimetablehandler)**(const std::string & table_name, const std::string & db, const Schema * schema)|  |
|**[GetTypes](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-gettypes)**() override| const [Types](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-types) & <br>Return table column Types information.  |
|**[~MemTimeTableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-~memtimetablehandler)**() override|  |
|**[GetSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getschema)**()| const Schema * <br>Return table schema.  |
|**[GetName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getname)**()| const std::string & <br>Return table name.  |
|**[GetIndex](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getindex)**()| const [IndexHint](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-indexhint) & <br>Return the index information.  |
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
|**[SetOrderType](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-setordertype)**(const [OrderType](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype) order_type)| void  |
|**[GetOrderType](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getordertype)**() const| const [OrderType](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype)  |
|**[GetHandlerTypeName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-gethandlertypename)**() override| const std::string <br>Return the name of handler and return "TableHandler" by default.  |

|**Inherited protected attributes**| |
| -------------- | -------------- |
| **[table_name_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-table_name_)**|const std::string  |
| **[db_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-db_)**|const std::string  |
| **[schema_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-schema_)**|const Schema *  |
| **[types_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-types_)**|[Types](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-types)  |
| **[index_hint_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-index_hint_)**|[IndexHint](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-indexhint)  |
| **[table_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-table_)**|[MemTimeTable](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-memtimetable)  |
| **[order_type_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#variable-order_type_)**|[OrderType](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype)  |

Inherited from [hybridse::vm::TableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md)
}

|  Inherited Public functions|            |
| -------------- | -------------- |
|**[TableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-tablehandler)**()|  |
|**[~TableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-~tablehandler)**()|  |
|**[GetTypes](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettypes)**() =0| const [Types](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-types) & <br>Return table column Types information.  |
|**[GetIndex](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getindex)**() =0| const [IndexHint](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-indexhint) & <br>Return the index information.  |
|**[GetWindowIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getwindowiterator)**(const std::string & idx_name) =0| std::unique_ptr< [WindowIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_window_iterator.md) >  |
|**[GetHanlderType](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gethanldertype)**() override| const [HandlerType](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype)  |
|**[GetPartition](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getpartition)**(const std::string & index_name)| std::shared_ptr< [PartitionHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md) >  |
|**[GetHandlerTypeName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gethandlertypename)**() override| const std::string <br>Return the name of handler and return "TableHandler" by default.  |
|**[GetOrderType](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getordertype)**() const| const [OrderType](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype)  |
|**[GetTablet](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettablet)**(const std::string & index_name, const std::string & pk)| std::shared_ptr< [Tablet](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_tablet.md) >  |
|**[GetTablet](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettablet)**(const std::string & index_name, const std::vector< std::string > & pks)| std::shared_ptr< [Tablet](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_tablet.md) >  |

Inherited from [hybridse::vm::DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md)
}

|  Inherited Public functions|            |
| -------------- | -------------- |
|**[DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-datahandler)**()|  |
|**[~DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-~datahandler)**()|  |
|**[GetSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getschema)**() =0| const Schema * <br>Return table schema.  |
|**[GetName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getname)**() =0| const std::string & <br>Return table name.  |
|**[GetDatabase](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getdatabase)**() =0| const std::string & <br>Return the name of database.  |
|**[GetHanlderType](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethanldertype)**() =0| const [HandlerType](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) <br>Return the type of [DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md).  |
|**[GetHandlerTypeName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethandlertypename)**() =0| const std::string <br>Return the name of handler type.  |
|**[GetStatus](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getstatus)**()| base::Status <br>Return dataset status. Default is hybridse::common::kOk.  |

Inherited from [hybridse::codec::ListV< Row >](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md)
}

|  Inherited Public functions|            |
| -------------- | -------------- |
|**[ListV](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-listv)**()|  |
|**[~ListV](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-~listv)**()|  |


## Public Functions

#### function ConcatTableHandler

```cpp
inline ConcatTableHandler(
    std::shared_ptr< TableHandler > left,
    size_t left_slices,
    std::shared_ptr< TableHandler > right,
    size_t right_slices
)
```


#### function ~ConcatTableHandler

```cpp
inline ~ConcatTableHandler()
```


#### function At

```cpp
inline virtual Row At(
    uint64_t pos
) override
```

Return a the value of element by its position in the list. 

**Parameters**: 

  * **pos** is element position in the list 


**Reimplements**: [hybridse::vm::MemTimeTableHandler::At](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-at)


#### function GetIterator

```cpp
inline virtual std::unique_ptr< RowIterator > GetIterator()
```

Return the const iterator. 

**Reimplements**: [hybridse::vm::MemTimeTableHandler::GetIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getiterator)


#### function GetRawIterator

```cpp
inline virtual RowIterator * GetRawIterator()
```

Return the const iterator raw pointer. 

**Reimplements**: [hybridse::vm::MemTimeTableHandler::GetRawIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getrawiterator)


#### function GetCount

```cpp
inline virtual const uint64_t GetCount()
```

Returns the number of elements in this list. 

**Reimplements**: [hybridse::vm::MemTimeTableHandler::GetCount](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getcount)


It count element by traverse the list 


-------------------------------

Updated on  6 April 2021 at 09:17:26 PDT