# TableHandler

`#include<vm/catalog.h>`

## Summary

TableHandler interface for HybridSE.  should his own implementation of `TableHandler`

| Constructors and Destructors  |
| :---------------------------- |
| [TableHandler](#TableHandler) |

| Public functions                      | Return type                                |
| :------------------------------------ | ------------------------------------------ |
| [IndexSupport](#IndexSupport)         | `Bool`                                     |
| [GetDatabase](#GetDatabase)           | `std::shared_ptr<type::Database`>          |
| [GetTable](#GetTable)                 | `std::shared_ptr<TableHandler>`            |
| [GetProcedureInfo](#GetProcedureInfo) | std::shared_ptr<fesql::sdk::ProcedureInfo> |

## Public functions

#### Catalog

```c++
class TableHandler : public DataHandler {
 public:
    TableHandler() : DataHandler() {}

    virtual ~TableHandler() {}

    // get the types
    virtual const Types& GetTypes() = 0;

    // get the index information
    virtual const IndexHint& GetIndex() = 0;
    // get the table iterator

    virtual std::unique_ptr<WindowIterator> GetWindowIterator(
        const std::string& idx_name) = 0;
    const HandlerType GetHanlderType() override { return kTableHandler; }
    virtual std::shared_ptr<PartitionHandler> GetPartition(
        const std::string& index_name) {
        return std::shared_ptr<PartitionHandler>();
    }
    const std::string GetHandlerTypeName() override { return "TableHandler"; }
    virtual const OrderType GetOrderType() const { return kNoneOrder; }
    virtual std::shared_ptr<Tablet> GetTablet(const std::string& index_name,
                                              const std::string& pk) {
        return std::shared_ptr<Tablet>();
    }
    virtual std::shared_ptr<Tablet> GetTablet(
        const std::string& index_name, const std::vector<std::string>& pks) {
        return std::shared_ptr<Tablet>();
    }
};
```

