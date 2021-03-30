---
title: hybridse::vm::AysncRowHandler
summary: A wrapper of table handler which is used as a asynchronous row handler. 

---
# hybridse::vm::AysncRowHandler



`#include <catalog.h>`

A wrapper of table handler which is used as a asynchronous row handler. 
## Summary

```cpp
class hybridse::vm::AysncRowHandler;
```
A wrapper of table handler which is used as a asynchronous row handler. 

[AysncRowHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_aysnc_row_handler.md) is statefull. It is running when created. GetValue is invoked, status will be changed if it is running at that moment. 



|  Public functions|            |
| -------------- | -------------- |
|**[AysncRowHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_aysnc_row_handler.md#function-aysncrowhandler)**(size_t idx, std::shared_ptr< [TableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md) > aysnc_table_handler)|  |
|**[~AysncRowHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_aysnc_row_handler.md#function-~aysncrowhandler)**()|  |
|**[GetValue](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_aysnc_row_handler.md#function-getvalue)**() override| const [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) &  |
|**[GetSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_aysnc_row_handler.md#function-getschema)**() override| const Schema * <br>Return table schema.  |
|**[GetName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_aysnc_row_handler.md#function-getname)**() override| const std::string & <br>Return table name.  |
|**[GetDatabase](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_aysnc_row_handler.md#function-getdatabase)**() override| const std::string & <br>Return the name of database.  |

## Inherited members
Inherited from [hybridse::vm::RowHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md)
| **Inherited public functions** | Name           |
| -------------- | -------------- |
|**[RowHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-rowhandler)**()|  |
|**[~RowHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-~rowhandler)**()| virtual  |
|**[GetIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-getiterator)**() override| virtual std::unique_ptr< RowIterator > <br>Return `null` since GetIterator isn't supported for a row.  |
|**[GetRawIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-getrawiterator)**() override| virtual RowIterator * <br>Return `null` since GetRawIterator isn't supported for a row,.  |
|**[GetCount](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-getcount)**() override| virtual const uint64_t <br>Return 0 since Getcount isn't supported for a row.  |
|**[At](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-at)**(uint64_t pos) override| virtual [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) <br>Return 0 since Getcount isn't supported for a row.  |
|**[GetHanlderType](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-gethanldertype)**() override| virtual const [HandlerType](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype)  |
|**[GetHandlerTypeName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-gethandlertypename)**() override| virtual const std::string  |

Inherited from [hybridse::vm::DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md)
| **Inherited public functions** | Name           |
| -------------- | -------------- |
|**[DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-datahandler)**()|  |
|**[~DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-~datahandler)**()| virtual  |
|**[GetHanlderType](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethanldertype)**() =0| virtual const [HandlerType](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) <br>Return the type of [DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md).  |
|**[GetHandlerTypeName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethandlertypename)**() =0| virtual const std::string <br>Return the name of handler type.  |
|**[GetStatus](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getstatus)**()| virtual base::Status <br>Return dataset status. Default is hybridse::common::kOk.  |

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

#### AysncRowHandler

```cpp
inline AysncRowHandler(
    size_t idx,
    std::shared_ptr< TableHandler > aysnc_table_handler
)
```


Create with given table_handler and row position index. status_ is set with common::kRunning 


#### ~AysncRowHandler

```cpp
inline virtual ~AysncRowHandler()
```


#### GetValue

```cpp
inline virtual const Row & GetValue() override
```


**Reimplements**: [hybridse::vm::RowHandler::GetValue](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-getvalue)


Return the row value. Sync row value by invoking aysnc_table_handler_->At(idx_) if status isn't common::kRunning 


#### GetSchema

```cpp
inline virtual const Schema * GetSchema() override
```

Return table schema. 

**Reimplements**: [hybridse::vm::DataHandler::GetSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getschema)


#### GetName

```cpp
inline virtual const std::string & GetName() override
```

Return table name. 

**Reimplements**: [hybridse::vm::DataHandler::GetName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getname)


#### GetDatabase

```cpp
inline virtual const std::string & GetDatabase() override
```

Return the name of database. 

**Reimplements**: [hybridse::vm::DataHandler::GetDatabase](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getdatabase)


-------------------------------

Updated on 29 March 2021 at 17:34:52 PDT