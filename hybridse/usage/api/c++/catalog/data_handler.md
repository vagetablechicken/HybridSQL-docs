# DataHandler

`include <vm/catalog.h>`

## Summary

`DataHandler` is the basic dataset operation abstraction in HyhridSE. It contains the basic operations available on all row-based dataset handlers, such as TableHandler, Partitionhandler.

Internally, each DataHandler is characterized by properties as followed:

| Constructors and Destructors |
| :--------------------------- |
| [DataHandler](#DataHandler)  |

| Public functions                          | Return type                    |
| :---------------------------------------- | ------------------------------ |
| [GetDatabase](#GetDatabase)               | `const std::string&`           |
| [GetHanlderType](#GetHanlderType)         | `const HandlerType`            |
| [GetHandlerTypeName](#GetHandlerTypeName) | `const std::string`            |
| [GetName](#GetName)                       | `const std::string&`           |
| [GetSchema](#GetSchema)                   | `const Schema*`                |
| [GetIterator](#GetIterator)               | `std::unique_ptr<RowIterator>` |
| [GetCount](#GetCount)                     | `const uint64_t`               |

## Public functions

#### DataHanlder

```c++
DataHandler() {}
```

Constructor of DataHandle

#### GetHanlderType

```c++
virtual HandlerType GetHanlderType()
```

Implemented by subclasses  to return the Type of Handler. e.g.

```c++
enum HandlerType { kRowHandler, kTableHandler, kPartitionHandler };
```

#### GetHandlerTypeName

```c++
// get handler type name
virtual const std::string GetHandlerTypeName()
```

Implemented by subclasses return the name of handler

#### GetSchema

```c++
const Schema* GetSchema()
```

Implemented by subclasses to return table schema. See [Schema](./table_types.md#Schema)

#### GetName

```c++
const std::string& GetName()
```

Implemented by subclasses to return table name.

#### GetIterator

```c++
std::unique_ptr<RowIterator> GetIterator()
```

Implemented by subclasses to return the row Iterator for the sake of row-based dataset

#### GetCount

```c++
const uint64_t GetCount()
```

Implemented by subclasses to return the number of rows in the dataset