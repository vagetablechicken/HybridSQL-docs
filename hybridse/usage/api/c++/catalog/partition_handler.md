# PartitionHandler

## Summary

PartitionHandler is dataset operation abstraction. It inherit from `TableHandler` and  should be implemented by subclasses.

| Constructors and Destructors          | Description                                       |
| :------------------------------------ | ------------------------------------------------- |
| [PartitionHandler](#PartitionHandler) | inherit from [`TableHandler`](./table_handler.md) |

| Public functions                          | Return type                         |
| :---------------------------------------- | ----------------------------------- |
| [GetHanlderType](#GetHanlderType)         | `const HandlerType`                 |
| [GetHandlerTypeName](#GetHandlerTypeName) | `const std::string`                 |
| [GetDatabase](#GetDatabase)               | `const std::string&`                |
| [GetName](#GetName)                       | `const std::string&`                |
| [GetSchema](#GetSchema)                   | `const Schema*`                     |
| [GetIterator](#GetIterator)               | `std::unique_ptr<RowIterator>`      |
| [GetCount](#GetCount)                     | `const uint64_t`                    |
| [GetTypes](#GetTypes)                     | `const Types`                       |
| [GetIndex](#GetIndex)                     | `const IndexHint&`                  |
| [GetOrderType](#GetOrderType)             | `const OrderType`                   |
| [GetWindowIterator](#GetWindowIterator)   | `std::unique_ptr<WindowIterator>`   |
| [GetPartition](#GetPartition)             | `std::shared_ptr<PartitionHandler>` |
| [GetTablet](#GetTablet)                   | `std::shared_ptr<Tablet>`           |
|                                           |                                     |

## Public functions

#### GetHanlderType

```c++
PartitionHandler()
```

Constructor of PartitionHandler

#### GetHanlderType

Return `HandlerType::kPartitionHandler`

#### GetHandlerTypeName

```c++
virtual const std::string GetHandlerTypeName()
```

Return the name of handler, and default is `"PartitionHandler"`

#### GetDatabase

```c++
const std::string& GetDatabase()
```

Implemented by subclasses  to return database name.

#### GetSchema

```c++
const Schema* GetSchema()
```

Implemented by subclasses to return table schema. See [Schema](./table_types.md#Schema).

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

#### GetOrderType

```c++
const OrderType GetOrderType() const 
```

Implemented by subclasses to return order type of the dataset, and default is `kNoneOrder`. See [`OrderType` ](./table_types.md#OrderType) 

#### GetTypes

```c++
const Types& GetTypes()
```

Implemented by subclasses  to return table columns info. See  [Types](./table_types.md#Types)

#### GetIndex

```c++
const IndexHint& GetIndex()
```

Implemented by subclasses  to return table index info. See [IndexHint](./table_types.md#IndexHint).

#### GetWindowIterator

```c++
std::unique_ptr<WindowIterator> GetWindowIterator(const std::string& idx_name)
```

Implemented by subclasses to return `WindowIterator` to iterate datasets one-by-one segments. See [WindowIterator](./window_iterator.md#WindowIterator).

#### GetPartition

```c++
std::shared_ptr<PartitionHandler> GetPartition(const std::string& index_name)
```

Return partition handler of specifiy partition binding to given index_name. Default return `null` partition.  See [PartitionHandler](#PartitionHandler).

#### GetTablet

```c++
virtual std::shared_ptr<Tablet> GetTablet(const std::string& index_name,
                                              const std::string& key)
```

Return  `Tablet` binding to specify index and key. Default return `null` tablet. See `Tablet`

#### GetSegment

```c++
virtual std::shared_ptr<TableHandler> GetSegment(const std::string& key)
```

Return table handler of specifiy segment binding to given key. Default return `null` partition. Defualt return `null`  table handler.  See [TableHandler](./table_handler.md/#TableHandler).

#### GetSegments

```c++
std::vector<std::shared_ptr<TableHandler>> GetSegments(
    const std::vector<std::string>& keys)
```

Return a set of table handles of specify segments binding to given keys set. See [TableHandler](./table_handler.md/#TableHandler).

## Examples

### MemPartitionHandler

The following example shows how to implement simple memory table partitions handler by inheriting from `PartitionHandler`

- Implement constructor by initialize schema and database name. 

```c++
MemPartitionHandler::MemPartitionHandler(const std::string& table_name,
                                         const std::string& db,
                                         const Schema* schema)
    : PartitionHandler(),
      table_name_(table_name),
      db_(db),
      schema_(schema),
      order_type_(kNoneOrder) {}
```

- Implement Meta information GetXXX operation 

```c++
const Schema* MemPartitionHandler::GetSchema() { return schema_; }
const std::string& MemPartitionHandler::GetName() { return table_name_; }
const std::string& MemPartitionHandler::GetDatabase() { return db_; }
const Types& MemPartitionHandler::GetTypes() { return types_; }
const IndexHint& MemPartitionHandler::GetIndex() { return index_hint_; }
```

- Implement `GetWindowIterator`  by using[ `MemWindowIterator`](./window_iterator.md#MemWindowIterator)

```c++
std::unique_ptr<WindowIterator> MemPartitionHandler::GetWindowIterator() {
    return std::unique_ptr<WindowIterator>(
        new MemWindowIterator(&partitions_, schema_));
}
```

- `GetIterator` unsupported for the sake of simplifying
- We also add operations to `AddRow` into storage for testing 



