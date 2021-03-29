---
title: hybridse::vm::MemRowHandler

---

# hybridse::vm::MemRowHandler




`#include <mem_catalog.h>`

Inherits from [hybridse::vm::RowHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_row_handler.md), [hybridse::vm::DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md), [hybridse::codec::ListV< Row >](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md)

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[MemRowHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_row_handler.md#function-memrowhandler)**(const [Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md) row) |
| | **[MemRowHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_row_handler.md#function-memrowhandler)**(const [Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md) row, const vm::Schema * schema) |
| | **[~MemRowHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_row_handler.md#function-~memrowhandler)**() |
| virtual const Schema * | **[GetSchema](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_row_handler.md#function-getschema)**() override<br>Implemented by subclasses to return table schema.  |
| virtual const std::string & | **[GetName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_row_handler.md#function-getname)**() override<br>Implemented by subclasses to return table name.  |
| virtual const std::string & | **[GetDatabase](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_row_handler.md#function-getdatabase)**() override<br>Implemented by subclasses to return the name of database.  |
| virtual const [Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md) & | **[GetValue](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_row_handler.md#function-getvalue)**() override<br>Implemented by subclasses to return value of row.  |
| virtual const std::string | **[GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_row_handler.md#function-gethandlertypename)**() override |

## Additional inherited members

**Public Functions inherited from [hybridse::vm::RowHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_row_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[RowHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-rowhandler)**() |
| virtual | **[~RowHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-~rowhandler)**() |
| virtual std::unique_ptr< RowIterator > | **[GetIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-getiterator)**() override<br>Return `null` since GetIterator isn't supported for a row.  |
| virtual RowIterator * | **[GetRawIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-getrawiterator)**() override<br>Return `null` since GetRawIterator isn't supported for a row,.  |
| virtual const uint64_t | **[GetCount](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-getcount)**() override<br>Return 0 since Getcount isn't supported for a row.  |
| virtual [Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md) | **[At](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-at)**(uint64_t pos) override<br>Return 0 since Getcount isn't supported for a row.  |
| virtual const [HandlerType](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) | **[GetHanlderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-gethanldertype)**() override |

**Public Functions inherited from [hybridse::vm::DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-datahandler)**() |
| virtual | **[~DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-~datahandler)**() |
| virtual const [HandlerType](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) | **[GetHanlderType](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethanldertype)**() =0<br>Implemented by subclasses to return the type of [DataHandler](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md).  |
| virtual base::Status | **[GetStatus](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getstatus)**()<br>Return dataset status. Default is hybridse::common::kOk.  |

**Public Functions inherited from [hybridse::codec::ListV< Row >](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md)**

|                | Name           |
| -------------- | -------------- |
| | **[ListV](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md#function-listv)**() |
| virtual | **[~ListV](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md#function-~listv)**() |
| virtual std::unique_ptr< [ConstIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1base_1_1_const_iterator.md)< uint64_t, V > > | **[GetIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getiterator)**() =0<br>Implemented by subclasses to return the const iterator.  |
| virtual [ConstIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1base_1_1_const_iterator.md)< uint64_t, V > * | **[GetRawIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getrawiterator)**() =0<br>Implemented by subclasses to return the const iterator raw pointer.  |
| virtual const uint64_t | **[GetCount](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getcount)**()<br>Returns the number of elements in this list.  |
| virtual V | **[At](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_list_v.md#function-at)**(uint64_t pos) |


## Public Functions Documentation

### function MemRowHandler

```cpp
inline explicit MemRowHandler(
    const Row row
)
```


### function MemRowHandler

```cpp
inline MemRowHandler(
    const Row row,
    const vm::Schema * schema
)
```


### function ~MemRowHandler

```cpp
inline ~MemRowHandler()
```


### function GetSchema

```cpp
inline virtual const Schema * GetSchema() override
```

Implemented by subclasses to return table schema. 

**Reimplements**: [hybridse::vm::DataHandler::GetSchema](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getschema)


### function GetName

```cpp
inline virtual const std::string & GetName() override
```

Implemented by subclasses to return table name. 

**Reimplements**: [hybridse::vm::DataHandler::GetName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getname)


### function GetDatabase

```cpp
inline virtual const std::string & GetDatabase() override
```

Implemented by subclasses to return the name of database. 

**Reimplements**: [hybridse::vm::DataHandler::GetDatabase](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getdatabase)


### function GetValue

```cpp
inline virtual const Row & GetValue() override
```

Implemented by subclasses to return value of row. 

**Reimplements**: [hybridse::vm::RowHandler::GetValue](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-getvalue)


### function GetHandlerTypeName

```cpp
inline virtual const std::string GetHandlerTypeName() override
```


**Reimplements**: [hybridse::vm::RowHandler::GetHandlerTypeName](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-gethandlertypename)


Return the name of handler type. Return `"RowHandler"` by default. 


-------------------------------

Updated on 29 March 2021 at 10:12:21 PDT