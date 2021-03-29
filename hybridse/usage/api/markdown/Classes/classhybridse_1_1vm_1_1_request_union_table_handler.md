---
title: hybridse::vm::RequestUnionTableHandler

---

# hybridse::vm::RequestUnionTableHandler



 [More...](#detailed-description)


`#include <mem_catalog.h>`

Inherits from [hybridse::vm::TableHandler](/Classes/classhybridse_1_1vm_1_1_table_handler.md), [hybridse::vm::DataHandler](/Classes/classhybridse_1_1vm_1_1_data_handler.md), hybridse::codec::ListV< Row >

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[RequestUnionTableHandler](/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-requestuniontablehandler)**(uint64_t request_ts, const Row & request_row, const std::shared_ptr< [TableHandler](/Classes/classhybridse_1_1vm_1_1_table_handler.md) > & window) |
| | **[~RequestUnionTableHandler](/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-~requestuniontablehandler)**() |
| std::unique_ptr< RowIterator > | **[GetIterator](/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-getiterator)**() override |
| RowIterator * | **[GetRawIterator](/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-getrawiterator)**() override |
| virtual const [Types](/Namespaces/namespacehybridse_1_1vm.md#typedef-types) & | **[GetTypes](/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-gettypes)**() override |
| virtual const [IndexHint](/Namespaces/namespacehybridse_1_1vm.md#typedef-indexhint) & | **[GetIndex](/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-getindex)**() override |
| virtual std::unique_ptr< WindowIterator > | **[GetWindowIterator](/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-getwindowiterator)**(const std::string & ) |
| virtual const [OrderType](/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype) | **[GetOrderType](/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-getordertype)**() const |
| virtual const Schema * | **[GetSchema](/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-getschema)**() override |
| virtual const std::string & | **[GetName](/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-getname)**() override |
| virtual const std::string & | **[GetDatabase](/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-getdatabase)**() override |

## Additional inherited members

**Public Functions inherited from [hybridse::vm::TableHandler](/Classes/classhybridse_1_1vm_1_1_table_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[TableHandler](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-tablehandler)**() |
| virtual | **[~TableHandler](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-~tablehandler)**() |
| virtual const [HandlerType](/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) | **[GetHanlderType](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gethanldertype)**() override |
| virtual std::shared_ptr< [PartitionHandler](/Classes/classhybridse_1_1vm_1_1_partition_handler.md) > | **[GetPartition](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getpartition)**(const std::string & index_name) |
| virtual const std::string | **[GetHandlerTypeName](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gethandlertypename)**() override |
| virtual std::shared_ptr< [Tablet](/Classes/classhybridse_1_1vm_1_1_tablet.md) > | **[GetTablet](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettablet)**(const std::string & index_name, const std::string & pk) |
| virtual std::shared_ptr< [Tablet](/Classes/classhybridse_1_1vm_1_1_tablet.md) > | **[GetTablet](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettablet)**(const std::string & index_name, const std::vector< std::string > & pks) |

**Public Functions inherited from [hybridse::vm::DataHandler](/Classes/classhybridse_1_1vm_1_1_data_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[DataHandler](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-datahandler)**() |
| virtual | **[~DataHandler](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-~datahandler)**() |
| virtual const [HandlerType](/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) | **[GetHanlderType](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethanldertype)**() =0 |
| virtual const std::string | **[GetHandlerTypeName](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethandlertypename)**() =0 |
| virtual base::Status | **[GetStatus](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getstatus)**() |


## Detailed Description

```cpp
class hybridse::vm::RequestUnionTableHandler;
```


Result table handler specified for request union: (1) The first row is fixed to be the request row (2) O(1) time construction 

## Public Functions Documentation

### function RequestUnionTableHandler

```cpp
inline RequestUnionTableHandler(
    uint64_t request_ts,
    const Row & request_row,
    const std::shared_ptr< TableHandler > & window
)
```


### function ~RequestUnionTableHandler

```cpp
inline ~RequestUnionTableHandler()
```


### function GetIterator

```cpp
inline std::unique_ptr< RowIterator > GetIterator() override
```


### function GetRawIterator

```cpp
RowIterator * GetRawIterator() override
```


### function GetTypes

```cpp
inline virtual const Types & GetTypes() override
```


**Reimplements**: [hybridse::vm::TableHandler::GetTypes](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettypes)


### function GetIndex

```cpp
inline virtual const IndexHint & GetIndex() override
```


**Reimplements**: [hybridse::vm::TableHandler::GetIndex](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getindex)


### function GetWindowIterator

```cpp
inline virtual std::unique_ptr< WindowIterator > GetWindowIterator(
    const std::string & 
)
```


**Reimplements**: [hybridse::vm::TableHandler::GetWindowIterator](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getwindowiterator)


### function GetOrderType

```cpp
inline virtual const OrderType GetOrderType() const
```


**Reimplements**: [hybridse::vm::TableHandler::GetOrderType](/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getordertype)


### function GetSchema

```cpp
inline virtual const Schema * GetSchema() override
```


**Return**: 

**Reimplements**: [hybridse::vm::DataHandler::GetSchema](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getschema)


Implemented by subclasses to return table schema. 


### function GetName

```cpp
inline virtual const std::string & GetName() override
```


**Return**: 

**Reimplements**: [hybridse::vm::DataHandler::GetName](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getname)


Implemented by subclasses to return table name. 


### function GetDatabase

```cpp
inline virtual const std::string & GetDatabase() override
```


**Return**: 

**Reimplements**: [hybridse::vm::DataHandler::GetDatabase](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getdatabase)


Implemented by subclasses to return the name of database. 


-------------------------------

Updated on 28 March 2021 at 19:23:48 PDT