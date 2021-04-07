---
title: hybridse::vm::RequestUnionTableHandler

---
# hybridse::vm::RequestUnionTableHandler



`#include <mem_catalog.h>`

## Summary

```cpp
class hybridse::vm::RequestUnionTableHandler;
```

Result table handler specified for request union: (1) The first row is fixed to be the request row (2) O(1) time construction 


|  Public functions|            |
| -------------- | -------------- |
|**[RequestUnionTableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-requestuniontablehandler)**(uint64_t request_ts, const [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) & request_row, const std::shared_ptr< [TableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md) > & window)|  |
|**[~RequestUnionTableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-~requestuniontablehandler)**()|  |
|**[GetIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-getiterator)**() override| std::unique_ptr< RowIterator > <br>Return the const iterator.  |
|**[GetRawIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-getrawiterator)**() override| RowIterator * <br>Return the const iterator raw pointer.  |
|**[GetTypes](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-gettypes)**() override| const [Types](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-types) & <br>Return table column Types information.  |
|**[GetIndex](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-getindex)**() override| const [IndexHint](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-indexhint) & <br>Return the index information.  |
|**[GetWindowIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-getwindowiterator)**(const std::string & idx_name)| std::unique_ptr< [WindowIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_window_iterator.md) >  |
|**[GetOrderType](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-getordertype)**() const| const [OrderType](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype)  |
|**[GetSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-getschema)**() override| const Schema * <br>Return table schema.  |
|**[GetName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-getname)**() override| const std::string & <br>Return table name.  |
|**[GetDatabase](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-getdatabase)**() override| const std::string & <br>Return the name of database.  |

## Inherited members

Inherited from [hybridse::vm::TableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md)

|  Inherited Public functions|            |
| -------------- | -------------- |
|**[TableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-tablehandler)**()|  |
|**[~TableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-~tablehandler)**()|  |
|**[GetHanlderType](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gethanldertype)**() override| const [HandlerType](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype)  |
|**[GetPartition](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getpartition)**(const std::string & index_name)| std::shared_ptr< [PartitionHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md) >  |
|**[GetHandlerTypeName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gethandlertypename)**() override| const std::string <br>Return the name of handler and return "TableHandler" by default.  |
|**[GetTablet](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettablet)**(const std::string & index_name, const std::string & pk)| std::shared_ptr< [Tablet](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_tablet.md) >  |
|**[GetTablet](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettablet)**(const std::string & index_name, const std::vector< std::string > & pks)| std::shared_ptr< [Tablet](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_tablet.md) >  |


Inherited from [hybridse::vm::DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md)

|  Inherited Public functions|            |
| -------------- | -------------- |
|**[DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-datahandler)**()|  |
|**[~DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-~datahandler)**()|  |
|**[GetHanlderType](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethanldertype)**() =0| const [HandlerType](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) <br>Return the type of [DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md).  |
|**[GetHandlerTypeName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethandlertypename)**() =0| const std::string <br>Return the name of handler type.  |
|**[GetStatus](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getstatus)**()| base::Status <br>Return dataset status. Default is hybridse::common::kOk.  |


Inherited from [hybridse::codec::ListV< Row >](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md)

|  Inherited Public functions|            |
| -------------- | -------------- |
|**[ListV](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-listv)**()|  |
|**[~ListV](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-~listv)**()|  |
|**[GetCount](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getcount)**()| const uint64_t <br>Returns the number of elements in this list.  |
|**[At](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-at)**(uint64_t pos)| V <br>Return a the value of element by its position in the list.  |


## Public Functions

#### function RequestUnionTableHandler

```cpp
inline RequestUnionTableHandler(
    uint64_t request_ts,
    const Row & request_row,
    const std::shared_ptr< TableHandler > & window
)
```


#### function ~RequestUnionTableHandler

```cpp
inline ~RequestUnionTableHandler()
```


#### function GetIterator

```cpp
inline virtual std::unique_ptr< RowIterator > GetIterator() override
```

Return the const iterator. 

**Reimplements**: [hybridse::codec::ListV::GetIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getiterator)


#### function GetRawIterator

```cpp
virtual RowIterator * GetRawIterator() override
```

Return the const iterator raw pointer. 

**Reimplements**: [hybridse::codec::ListV::GetRawIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getrawiterator)


#### function GetTypes

```cpp
inline virtual const Types & GetTypes() override
```

Return table column Types information. 

**Reimplements**: [hybridse::vm::TableHandler::GetTypes](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettypes)


#### function GetIndex

```cpp
inline virtual const IndexHint & GetIndex() override
```

Return the index information. 

**Reimplements**: [hybridse::vm::TableHandler::GetIndex](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getindex)


#### function GetWindowIterator

```cpp
inline virtual std::unique_ptr< WindowIterator > GetWindowIterator(
    const std::string & idx_name
)
```


**Reimplements**: [hybridse::vm::TableHandler::GetWindowIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getwindowiterator)


Return WindowIterator so that user can use it to iterate datasets segment by segment. 

#### function GetOrderType

```cpp
inline virtual const OrderType GetOrderType() const
```


**Reimplements**: [hybridse::vm::TableHandler::GetOrderType](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getordertype)


Return the order type of the dataset, and return OrderType::kNoneOrder by default. 

#### function GetSchema

```cpp
inline virtual const Schema * GetSchema() override
```

Return table schema. 

**Reimplements**: [hybridse::vm::DataHandler::GetSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getschema)


#### function GetName

```cpp
inline virtual const std::string & GetName() override
```

Return table name. 

**Reimplements**: [hybridse::vm::DataHandler::GetName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getname)


#### function GetDatabase

```cpp
inline virtual const std::string & GetDatabase() override
```

Return the name of database. 

**Reimplements**: [hybridse::vm::DataHandler::GetDatabase](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getdatabase)


