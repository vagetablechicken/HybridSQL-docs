---
title: hybridse::vm::MemRowHandler

---

# hybridse::vm::MemRowHandler




`#include <mem_catalog.h>`

Inherits from [hybridse::vm::RowHandler](/Classes/classhybridse_1_1vm_1_1_row_handler.md), [hybridse::vm::DataHandler](/Classes/classhybridse_1_1vm_1_1_data_handler.md), hybridse::codec::ListV< Row >

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[MemRowHandler](/Classes/classhybridse_1_1vm_1_1_mem_row_handler.md#function-memrowhandler)**(const Row row) |
| | **[MemRowHandler](/Classes/classhybridse_1_1vm_1_1_mem_row_handler.md#function-memrowhandler)**(const Row row, const vm::Schema * schema) |
| | **[~MemRowHandler](/Classes/classhybridse_1_1vm_1_1_mem_row_handler.md#function-~memrowhandler)**() |
| virtual const Schema * | **[GetSchema](/Classes/classhybridse_1_1vm_1_1_mem_row_handler.md#function-getschema)**() override |
| virtual const std::string & | **[GetName](/Classes/classhybridse_1_1vm_1_1_mem_row_handler.md#function-getname)**() override |
| virtual const std::string & | **[GetDatabase](/Classes/classhybridse_1_1vm_1_1_mem_row_handler.md#function-getdatabase)**() override |
| virtual const Row & | **[GetValue](/Classes/classhybridse_1_1vm_1_1_mem_row_handler.md#function-getvalue)**() override |
| virtual const std::string | **[GetHandlerTypeName](/Classes/classhybridse_1_1vm_1_1_mem_row_handler.md#function-gethandlertypename)**() override |

## Additional inherited members

**Public Functions inherited from [hybridse::vm::RowHandler](/Classes/classhybridse_1_1vm_1_1_row_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[RowHandler](/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-rowhandler)**() |
| virtual | **[~RowHandler](/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-~rowhandler)**() |
| std::unique_ptr< RowIterator > | **[GetIterator](/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-getiterator)**() override |
| RowIterator * | **[GetRawIterator](/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-getrawiterator)**() override |
| const uint64_t | **[GetCount](/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-getcount)**() override |
| Row | **[At](/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-at)**(uint64_t pos) override |
| virtual const [HandlerType](/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) | **[GetHanlderType](/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-gethanldertype)**() override |

**Public Functions inherited from [hybridse::vm::DataHandler](/Classes/classhybridse_1_1vm_1_1_data_handler.md)**

|                | Name           |
| -------------- | -------------- |
| | **[DataHandler](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-datahandler)**() |
| virtual | **[~DataHandler](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-~datahandler)**() |
| virtual const [HandlerType](/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype) | **[GetHanlderType](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-gethanldertype)**() =0 |
| virtual base::Status | **[GetStatus](/Classes/classhybridse_1_1vm_1_1_data_handler.md#function-getstatus)**() |


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


### function GetValue

```cpp
inline virtual const Row & GetValue() override
```


**Reimplements**: [hybridse::vm::RowHandler::GetValue](/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-getvalue)


### function GetHandlerTypeName

```cpp
inline virtual const std::string GetHandlerTypeName() override
```


**Return**: 

**Reimplements**: [hybridse::vm::RowHandler::GetHandlerTypeName](/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-gethandlertypename)


Implemented by subclasses return the name of handler type 


-------------------------------

Updated on 28 March 2021 at 19:23:48 PDT