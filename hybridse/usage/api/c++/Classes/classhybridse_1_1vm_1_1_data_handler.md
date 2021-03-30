---
title: hybridse::vm::DataHandler
summary: The basic dataset operation abstraction. 

---
# hybridse::vm::DataHandler



`#include <catalog.h>`

The basic dataset operation abstraction. 
## Summary

```cpp
class hybridse::vm::DataHandler;
```
The basic dataset operation abstraction. 

It contains the basic operations available on all row-based dataset handlers, such as [TableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md), Partitionhandler. 



|  Public functions|            |
| -------------- | -------------- |
|**[DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-datahandler)**()|  |
|**[~DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-~datahandler)**()|  |
|**[GetSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getschema)**() =0| const Schema * <br>Return table schema.  |
|**[GetName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getname)**() =0| const std::string & <br>Return table name.  |
|**[GetDatabase](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getdatabase)**() =0| const std::string & <br>Return the name of database.  |
|**[GetHanlderType](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethanldertype)**() =0| const [HandlerType](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) <br>Return the type of [DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md).  |
|**[GetHandlerTypeName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethandlertypename)**() =0| const std::string <br>Return the name of handler type.  |
|**[GetStatus](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getstatus)**()| base::Status <br>Return dataset status. Default is hybridse::common::kOk.  |

## Inherited members
Inherited by [hybridse::vm::RowHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md), [hybridse::vm::TableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md)
Inherited from [hybridse::codec::ListV< Row >](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md)
| **Inherited public functions** | Name           |
| -------------- | -------------- |
|**[ListV](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-listv)**()|  |
|**[~ListV](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-~listv)**()| virtual  |
|**[GetIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getiterator)**() =0| virtual std::unique_ptr< [ConstIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_const_iterator.md)< uint64_t, V > > <br>Return the const iterator.  |
|**[GetRawIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getrawiterator)**() =0| virtual [ConstIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_const_iterator.md)< uint64_t, V > * <br>Return the const iterator raw pointer.  |
|**[GetCount](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getcount)**()| virtual const uint64_t <br>Returns the number of elements in this list.  |
|**[At](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-at)**(uint64_t pos)| virtual V <br>Return a the value of element by its position in the list.  |


## Public Functions

#### DataHandler { function DataHandler }

```cpp
inline DataHandler()
```


#### ~DataHandler { function ~DataHandler }

```cpp
inline virtual ~DataHandler()
```


#### GetSchema { function GetSchema }

```cpp
virtual const Schema * GetSchema() =0
```

Return table schema. 

**Reimplemented by**: [hybridse::vm::MemTableHandler::GetSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getschema), [hybridse::vm::MemTimeTableHandler::GetSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getschema), [hybridse::vm::MemSegmentHandler::GetSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md#function-getschema), [hybridse::vm::ErrorRowHandler::GetSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_row_handler.md#function-getschema), [hybridse::vm::ErrorTableHandler::GetSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-getschema), [hybridse::vm::AysncRowHandler::GetSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_aysnc_row_handler.md#function-getschema), [hybridse::vm::MemRowHandler::GetSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_row_handler.md#function-getschema), [hybridse::vm::MemPartitionHandler::GetSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getschema), [hybridse::vm::RequestUnionTableHandler::GetSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-getschema)


#### GetName { function GetName }

```cpp
virtual const std::string & GetName() =0
```

Return table name. 

**Reimplemented by**: [hybridse::vm::MemTableHandler::GetName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getname), [hybridse::vm::MemTimeTableHandler::GetName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getname), [hybridse::vm::MemSegmentHandler::GetName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md#function-getname), [hybridse::vm::ErrorRowHandler::GetName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_row_handler.md#function-getname), [hybridse::vm::ErrorTableHandler::GetName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-getname), [hybridse::vm::AysncRowHandler::GetName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_aysnc_row_handler.md#function-getname), [hybridse::vm::MemRowHandler::GetName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_row_handler.md#function-getname), [hybridse::vm::MemPartitionHandler::GetName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getname), [hybridse::vm::RequestUnionTableHandler::GetName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-getname)


#### GetDatabase { function GetDatabase }

```cpp
virtual const std::string & GetDatabase() =0
```

Return the name of database. 

**Reimplemented by**: [hybridse::vm::MemTableHandler::GetDatabase](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getdatabase), [hybridse::vm::MemTimeTableHandler::GetDatabase](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getdatabase), [hybridse::vm::MemSegmentHandler::GetDatabase](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md#function-getdatabase), [hybridse::vm::ErrorRowHandler::GetDatabase](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_row_handler.md#function-getdatabase), [hybridse::vm::ErrorTableHandler::GetDatabase](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-getdatabase), [hybridse::vm::AysncRowHandler::GetDatabase](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_aysnc_row_handler.md#function-getdatabase), [hybridse::vm::MemRowHandler::GetDatabase](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_row_handler.md#function-getdatabase), [hybridse::vm::MemPartitionHandler::GetDatabase](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getdatabase), [hybridse::vm::RequestUnionTableHandler::GetDatabase](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-getdatabase)


#### GetHanlderType { function GetHanlderType }

```cpp
virtual const HandlerType GetHanlderType() =0
```

Return the type of [DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md). 

**Reimplemented by**: [hybridse::vm::RowHandler::GetHanlderType](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-gethanldertype), [hybridse::vm::TableHandler::GetHanlderType](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gethanldertype), [hybridse::vm::PartitionHandler::GetHanlderType](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-gethanldertype)


#### GetHandlerTypeName { function GetHandlerTypeName }

```cpp
virtual const std::string GetHandlerTypeName() =0
```

Return the name of handler type. 

**Reimplemented by**: [hybridse::vm::RowHandler::GetHandlerTypeName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-gethandlertypename), [hybridse::vm::ErrorRowHandler::GetHandlerTypeName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_row_handler.md#function-gethandlertypename), [hybridse::vm::TableHandler::GetHandlerTypeName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gethandlertypename), [hybridse::vm::ErrorTableHandler::GetHandlerTypeName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-gethandlertypename), [hybridse::vm::PartitionHandler::GetHandlerTypeName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-gethandlertypename), [hybridse::vm::MemRowHandler::GetHandlerTypeName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_row_handler.md#function-gethandlertypename), [hybridse::vm::MemTableHandler::GetHandlerTypeName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-gethandlertypename), [hybridse::vm::MemTimeTableHandler::GetHandlerTypeName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-gethandlertypename), [hybridse::vm::Window::GetHandlerTypeName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window.md#function-gethandlertypename), [hybridse::vm::MemSegmentHandler::GetHandlerTypeName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md#function-gethandlertypename), [hybridse::vm::MemPartitionHandler::GetHandlerTypeName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-gethandlertypename)


#### GetStatus { function GetStatus }

```cpp
inline virtual base::Status GetStatus()
```

Return dataset status. Default is hybridse::common::kOk. 

**Reimplemented by**: [hybridse::vm::ErrorRowHandler::GetStatus](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_row_handler.md#function-getstatus), [hybridse::vm::ErrorTableHandler::GetStatus](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-getstatus)


-------------------------------

Updated on 29 March 2021 at 17:58:50 PDT