---
title: hybridse::vm::ErrorTableHandler
summary: A table dataset's error handler, representing a error table. 

---
# hybridse::vm::ErrorTableHandler



`#include <catalog.h>`

A table dataset's error handler, representing a error table. 
## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[ErrorTableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-errortablehandler)**()|  |
|**[ErrorTableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-errortablehandler)**(common::StatusCode status_code, const std::string & msg_str)| <br>Create [ErrorTableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_table_handler.md) with specific status code and message.  |
|**[~ErrorTableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-~errortablehandler)**()|  |
|**[GetTypes](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-gettypes)**() override| const [Types](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-types) & <br>Return empty column Types.  |
|**[GetSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-getschema)**() override| const Schema * <br>Return empty table Schema.  |
|**[GetName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-getname)**() override| const std::string & <br>Return empty table name.  |
|**[GetIndex](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-getindex)**() override| const [IndexHint](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-indexhint) & <br>Return empty indexn information.  |
|**[GetDatabase](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-getdatabase)**() override| const std::string & <br>Return name of database.  |
|**[GetIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-getiterator)**()| std::unique_ptr< RowIterator > <br>Return null iterator.  |
|**[GetRawIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-getrawiterator)**()| RowIterator * <br>Return null iterator.  |
|**[GetWindowIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-getwindowiterator)**(const std::string & idx_name)| std::unique_ptr< [WindowIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_window_iterator.md) > <br>Return null window iterator.  |
|**[At](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-at)**(uint64_t pos)| [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) <br>Return empty row.  |
|**[GetCount](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-getcount)**() override| const uint64_t <br>Return 0.  |
|**[GetHandlerTypeName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-gethandlertypename)**() override| const std::string <br>Return handler type name, and return "ErrorTableHandler" by default.  |
|**[GetStatus](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-getstatus)**()| base::Status <br>Return status.  |

##

| Protected attributes | |
| -------------- | -------------- |
| **[status_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#variable-status_)**
| base::Status  |
| **[table_name_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#variable-table_name_)**
| const std::string  |
| **[db_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#variable-db_)**
| const std::string  |
| **[schema_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#variable-schema_)**
| const Schema *  |
| **[types_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#variable-types_)**
| [Types](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-types)  |
| **[index_hint_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#variable-index_hint_)**
| [IndexHint](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-indexhint)  |
| **[order_type_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#variable-order_type_)**
| [OrderType](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype)  |

## Inherited members
Inherited from [hybridse::vm::TableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md)
| **Inherited public functions** | Name           |
| -------------- | -------------- |
|**[TableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-tablehandler)**()|  |
|**[~TableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-~tablehandler)**()| virtual  |
|**[GetHanlderType](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gethanldertype)**() override| virtual const [HandlerType](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype)  |
|**[GetPartition](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getpartition)**(const std::string & index_name)| virtual std::shared_ptr< [PartitionHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md) >  |
|**[GetOrderType](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getordertype)**() const| virtual const [OrderType](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype)  |
|**[GetTablet](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettablet)**(const std::string & index_name, const std::string & pk)| virtual std::shared_ptr< [Tablet](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_tablet.md) >  |
|**[GetTablet](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettablet)**(const std::string & index_name, const std::vector< std::string > & pks)| virtual std::shared_ptr< [Tablet](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_tablet.md) >  |

Inherited from [hybridse::vm::DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md)
| **Inherited public functions** | Name           |
| -------------- | -------------- |
|**[DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-datahandler)**()|  |
|**[~DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-~datahandler)**()| virtual  |
|**[GetHanlderType](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethanldertype)**() =0| virtual const [HandlerType](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) <br>Return the type of [DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md).  |

Inherited from [hybridse::codec::ListV< Row >](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md)
| **Inherited public functions** | Name           |
| -------------- | -------------- |
|**[ListV](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-listv)**()|  |
|**[~ListV](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-~listv)**()| virtual  |


## Public Functions

#### ErrorTableHandler { function ErrorTableHandler }

```cpp
inline ErrorTableHandler()
```


Create ErrorTableTable with initializing status_ with common::kCallMethodError 


#### ErrorTableHandler { function ErrorTableHandler }

```cpp
inline ErrorTableHandler(
    common::StatusCode status_code,
    const std::string & msg_str
)
```

Create [ErrorTableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_table_handler.md) with specific status code and message. 

#### ~ErrorTableHandler { function ~ErrorTableHandler }

```cpp
inline ~ErrorTableHandler()
```


#### GetTypes { function GetTypes }

```cpp
inline virtual const Types & GetTypes() override
```

Return empty column Types. 

**Reimplements**: [hybridse::vm::TableHandler::GetTypes](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gettypes)


#### GetSchema { function GetSchema }

```cpp
inline virtual const Schema * GetSchema() override
```

Return empty table Schema. 

**Reimplements**: [hybridse::vm::DataHandler::GetSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getschema)


#### GetName { function GetName }

```cpp
inline virtual const std::string & GetName() override
```

Return empty table name. 

**Reimplements**: [hybridse::vm::DataHandler::GetName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getname)


#### GetIndex { function GetIndex }

```cpp
inline virtual const IndexHint & GetIndex() override
```

Return empty indexn information. 

**Reimplements**: [hybridse::vm::TableHandler::GetIndex](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getindex)


#### GetDatabase { function GetDatabase }

```cpp
inline virtual const std::string & GetDatabase() override
```

Return name of database. 

**Reimplements**: [hybridse::vm::DataHandler::GetDatabase](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getdatabase)


#### GetIterator { function GetIterator }

```cpp
inline virtual std::unique_ptr< RowIterator > GetIterator()
```

Return null iterator. 

**Reimplements**: [hybridse::codec::ListV::GetIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getiterator)


#### GetRawIterator { function GetRawIterator }

```cpp
inline virtual RowIterator * GetRawIterator()
```

Return null iterator. 

**Reimplements**: [hybridse::codec::ListV::GetRawIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getrawiterator)


#### GetWindowIterator { function GetWindowIterator }

```cpp
inline virtual std::unique_ptr< WindowIterator > GetWindowIterator(
    const std::string & idx_name
)
```

Return null window iterator. 

**Reimplements**: [hybridse::vm::TableHandler::GetWindowIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-getwindowiterator)


#### At { function At }

```cpp
inline virtual Row At(
    uint64_t pos
)
```

Return empty row. 

**Reimplements**: [hybridse::codec::ListV::At](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-at)


#### GetCount { function GetCount }

```cpp
inline virtual const uint64_t GetCount() override
```

Return 0. 

**Reimplements**: [hybridse::codec::ListV::GetCount](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getcount)


#### GetHandlerTypeName { function GetHandlerTypeName }

```cpp
inline virtual const std::string GetHandlerTypeName() override
```

Return handler type name, and return "ErrorTableHandler" by default. 

**Reimplements**: [hybridse::vm::TableHandler::GetHandlerTypeName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md#function-gethandlertypename)


#### GetStatus { function GetStatus }

```cpp
inline virtual base::Status GetStatus()
```

Return status. 

**Reimplements**: [hybridse::vm::DataHandler::GetStatus](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getstatus)


## Protected Attributes

### status_

```cpp
base::Status status_;
```


### table_name_

```cpp
const std::string table_name_;
```


### db_

```cpp
const std::string db_;
```


### schema_

```cpp
const Schema * schema_;
```


### types_

```cpp
Types types_;
```


### index_hint_

```cpp
IndexHint index_hint_;
```


### order_type_

```cpp
OrderType order_type_;
```


-------------------------------

Updated on 29 March 2021 at 17:58:50 PDT