---
title: hybridse::vm::DataHandler
summary: The basic dataset operation abstraction. 

---

# hybridse::vm::DataHandler



The basic dataset operation abstraction.  [More...](#detailed-description)


`#include <catalog.h>`

Inherits from [hybridse::codec::ListV< Row >](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md)

Inherited by [hybridse::vm::RowHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_row_handler.md), [hybridse::vm::TableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md)

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-datahandler)**() |
| virtual | **[~DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-~datahandler)**() |
| virtual const Schema * | **[GetSchema](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getschema)**() =0<br>Implemented by subclasses to return table schema.  |
| virtual const std::string & | **[GetName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getname)**() =0<br>Implemented by subclasses to return table name.  |
| virtual const std::string & | **[GetDatabase](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getdatabase)**() =0<br>Implemented by subclasses to return the name of database.  |
| virtual const [HandlerType](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) | **[GetHanlderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethanldertype)**() =0<br>Implemented by subclasses to return the type of [DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md).  |
| virtual const std::string | **[GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethandlertypename)**() =0<br>Implemented by subclasses return the name of handler type.  |
| virtual base::Status | **[GetStatus](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getstatus)**()<br>Return dataset status. Default is hybridse::common::kOk.  |

## Additional inherited members

**Public Functions inherited from [hybridse::codec::ListV< Row >](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md)**

|                | Name           |
| -------------- | -------------- |
| | **[ListV](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md#function-listv)**() |
| virtual | **[~ListV](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md#function-~listv)**() |
| virtual std::unique_ptr< [ConstIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1base_1_1_const_iterator.md)< uint64_t, V > > | **[GetIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getiterator)**() =0<br>Implemented by subclasses to return the const iterator.  |
| virtual [ConstIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1base_1_1_const_iterator.md)< uint64_t, V > * | **[GetRawIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getrawiterator)**() =0<br>Implemented by subclasses to return the const iterator raw pointer.  |
| virtual const uint64_t | **[GetCount](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getcount)**()<br>Returns the number of elements in this list.  |
| virtual V | **[At](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md#function-at)**(uint64_t pos) |


## Detailed Description

```cpp
class hybridse::vm::DataHandler;
```

The basic dataset operation abstraction. 

It contains the basic operations available on all row-based dataset handlers, such as [TableHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md), Partitionhandler. 

## Public Functions Documentation

### function DataHandler

```cpp
inline DataHandler()
```


### function ~DataHandler

```cpp
inline virtual ~DataHandler()
```


### function GetSchema

```cpp
virtual const Schema * GetSchema() =0
```

Implemented by subclasses to return table schema. 

**Reimplemented by**: [hybridse::vm::MemTableHandler::GetSchema](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getschema), [hybridse::vm::MemTimeTableHandler::GetSchema](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getschema), [hybridse::vm::MemSegmentHandler::GetSchema](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md#function-getschema), [hybridse::vm::ErrorRowHandler::GetSchema](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_error_row_handler.md#function-getschema), [hybridse::vm::ErrorTableHandler::GetSchema](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-getschema), [hybridse::vm::AysncRowHandler::GetSchema](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_aysnc_row_handler.md#function-getschema), [hybridse::vm::MemRowHandler::GetSchema](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_row_handler.md#function-getschema), [hybridse::vm::MemPartitionHandler::GetSchema](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getschema), [hybridse::vm::RequestUnionTableHandler::GetSchema](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-getschema)


### function GetName

```cpp
virtual const std::string & GetName() =0
```

Implemented by subclasses to return table name. 

**Reimplemented by**: [hybridse::vm::MemTableHandler::GetName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getname), [hybridse::vm::MemTimeTableHandler::GetName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getname), [hybridse::vm::MemSegmentHandler::GetName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md#function-getname), [hybridse::vm::ErrorRowHandler::GetName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_error_row_handler.md#function-getname), [hybridse::vm::ErrorTableHandler::GetName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-getname), [hybridse::vm::AysncRowHandler::GetName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_aysnc_row_handler.md#function-getname), [hybridse::vm::MemRowHandler::GetName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_row_handler.md#function-getname), [hybridse::vm::MemPartitionHandler::GetName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getname), [hybridse::vm::RequestUnionTableHandler::GetName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-getname)


### function GetDatabase

```cpp
virtual const std::string & GetDatabase() =0
```

Implemented by subclasses to return the name of database. 

**Reimplemented by**: [hybridse::vm::MemTableHandler::GetDatabase](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getdatabase), [hybridse::vm::MemTimeTableHandler::GetDatabase](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getdatabase), [hybridse::vm::MemSegmentHandler::GetDatabase](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md#function-getdatabase), [hybridse::vm::ErrorRowHandler::GetDatabase](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_error_row_handler.md#function-getdatabase), [hybridse::vm::ErrorTableHandler::GetDatabase](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-getdatabase), [hybridse::vm::AysncRowHandler::GetDatabase](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_aysnc_row_handler.md#function-getdatabase), [hybridse::vm::MemRowHandler::GetDatabase](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_row_handler.md#function-getdatabase), [hybridse::vm::MemPartitionHandler::GetDatabase](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getdatabase), [hybridse::vm::RequestUnionTableHandler::GetDatabase](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-getdatabase)


### function GetHanlderType

```cpp
virtual const HandlerType GetHanlderType() =0
```

Implemented by subclasses to return the type of [DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md). 

**Reimplemented by**: [hybridse::vm::RowHandler::GetHanlderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-gethanldertype), [hybridse::vm::TableHandler::GetHanlderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gethanldertype), [hybridse::vm::PartitionHandler::GetHanlderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-gethanldertype)


### function GetHandlerTypeName

```cpp
virtual const std::string GetHandlerTypeName() =0
```

Implemented by subclasses return the name of handler type. 

**Reimplemented by**: [hybridse::vm::RowHandler::GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-gethandlertypename), [hybridse::vm::ErrorRowHandler::GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_error_row_handler.md#function-gethandlertypename), [hybridse::vm::TableHandler::GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gethandlertypename), [hybridse::vm::ErrorTableHandler::GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-gethandlertypename), [hybridse::vm::PartitionHandler::GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-gethandlertypename), [hybridse::vm::MemRowHandler::GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_row_handler.md#function-gethandlertypename), [hybridse::vm::MemTableHandler::GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-gethandlertypename), [hybridse::vm::MemTimeTableHandler::GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-gethandlertypename), [hybridse::vm::Window::GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_window.md#function-gethandlertypename), [hybridse::vm::MemSegmentHandler::GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md#function-gethandlertypename), [hybridse::vm::MemPartitionHandler::GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-gethandlertypename)


### function GetStatus

```cpp
inline virtual base::Status GetStatus()
```

Return dataset status. Default is hybridse::common::kOk. 

**Reimplemented by**: [hybridse::vm::ErrorRowHandler::GetStatus](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_error_row_handler.md#function-getstatus), [hybridse::vm::ErrorTableHandler::GetStatus](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-getstatus)


-------------------------------

Updated on 29 March 2021 at 10:12:21 PDT