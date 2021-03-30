---
title: hybridse::vm::ErrorRowHandler
summary: A row's error handler, representing a error row. 

---
# hybridse::vm::ErrorRowHandler



`#include <catalog.h>`

A row's error handler, representing a error row. 
## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[ErrorRowHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_row_handler.md#function-errorrowhandler)**(common::StatusCode status_code, const std::string & msg_str)| <br>Creating [ErrorRowHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_row_handler.md) with status code and error msg.  |
|**[~ErrorRowHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_row_handler.md#function-~errorrowhandler)**()|  |
|**[GetValue](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_row_handler.md#function-getvalue)**()| const [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) & <br>Return empty Row as value.  |
|**[GetHandlerTypeName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_row_handler.md#function-gethandlertypename)**() override| const std::string <br>Return handler type name, and return "ErrorRowHandler" by default.  |
|**[GetSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_row_handler.md#function-getschema)**() override| const Schema * <br>Return table schema.  |
|**[GetName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_row_handler.md#function-getname)**() override| const std::string & <br>Return table name.  |
|**[GetDatabase](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_row_handler.md#function-getdatabase)**() override| const std::string & <br>Return the name of database.  |
|**[GetStatus](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_row_handler.md#function-getstatus)**()| base::Status <br>Return dataset status. Default is hybridse::common::kOk.  |

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
|**[GetIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getiterator)**() =0| virtual std::unique_ptr< [ConstIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_const_iterator.md)< uint64_t, V > > <br>Return the const iterator.  |
|**[GetRawIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getrawiterator)**() =0| virtual [ConstIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_const_iterator.md)< uint64_t, V > * <br>Return the const iterator raw pointer.  |
|**[GetCount](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getcount)**()| virtual const uint64_t <br>Returns the number of elements in this list.  |
|**[At](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-at)**(uint64_t pos)| virtual V <br>Return a the value of element by its position in the list.  |


## Public Functions

#### function ErrorRowHandler

```cpp
inline ErrorRowHandler(
    common::StatusCode status_code,
    const std::string & msg_str
)
```

Creating [ErrorRowHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_row_handler.md) with status code and error msg. 

#### function ~ErrorRowHandler

```cpp
inline ~ErrorRowHandler()
```


#### function GetValue

```cpp
inline virtual const Row & GetValue()
```

Return empty Row as value. 

**Reimplements**: [hybridse::vm::RowHandler::GetValue](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-getvalue)


#### function GetHandlerTypeName

```cpp
inline virtual const std::string GetHandlerTypeName() override
```

Return handler type name, and return "ErrorRowHandler" by default. 

**Reimplements**: [hybridse::vm::RowHandler::GetHandlerTypeName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-gethandlertypename)


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


#### function GetStatus

```cpp
inline virtual base::Status GetStatus()
```

Return dataset status. Default is hybridse::common::kOk. 

**Reimplements**: [hybridse::vm::DataHandler::GetStatus](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getstatus)


-------------------------------

Updated on 29 March 2021 at 18:05:16 PDT