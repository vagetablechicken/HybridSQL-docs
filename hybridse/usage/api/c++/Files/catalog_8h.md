---
title: /Users/chenjing/work/4paradigm/HybridSE/include/vm/catalog.h

---
# /Users/chenjing/work/4paradigm/HybridSE/include/vm/catalog.h

## Namespaces

| Name           |
| -------------- |
| **[hybridse](hybridse/usage/api/c++/Namespaces/namespacehybridse.md)**  |
| **[hybridse::vm](hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md)**  |

## Classes

|                | Name           |
| -------------- | -------------- |
| struct | **[hybridse::vm::IndexSt](hybridse/usage/api/c++/Classes/structhybridse_1_1vm_1_1_index_st.md)**  |
| class | **[hybridse::vm::DataHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md)** <br>The basic dataset operation abstraction.  |
| class | **[hybridse::vm::DataHandlerList](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_list.md)** <br>A sequence of [DataHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md).  |
| class | **[hybridse::vm::DataHandlerVector](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_vector.md)** <br>A implementation of [DataHandlerList](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_list.md).  |
| class | **[hybridse::vm::DataHandlerRepeater](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_repeater.md)** <br>A implementation of [DataHandlerList](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_list.md).  |
| class | **[hybridse::vm::RowHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md)** <br>A row operation abstraction.  |
| class | **[hybridse::vm::ErrorRowHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_row_handler.md)** <br>A row's error handler, representing a error row.  |
| class | **[hybridse::vm::TableHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md)** <br>A table dataset operation abstraction.  |
| class | **[hybridse::vm::ErrorTableHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_table_handler.md)** <br>A table dataset's error handler, representing a error table.  |
| class | **[hybridse::vm::PartitionHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md)** <br>The abstraction of partition dataset operation.  |
| class | **[hybridse::vm::AysncRowHandler](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_aysnc_row_handler.md)** <br>A wrapper of table handler which is used as a asynchronous row handler.  |
| class | **[hybridse::vm::Tablet](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_tablet.md)** <br>A component responsible to Query subtask.  |
| class | **[hybridse::vm::Catalog](hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_catalog.md)** <br>A [Catalog]() handler which defines a set of operation for, e.g, database, table and index management.  |




## Source code

```cpp
/*
 * Copyright 2021 4Paradigm
 *
 * Licensed under the Apache License, Version 2.0 (the "License");
 * you may not use this file except in compliance with the License.
 * You may obtain a copy of the License at
 *
 *    http://www.apache.org/licenses/LICENSE-2.0
 *
 * Unless required by applicable law or agreed to in writing, software
 * distributed under the License is distributed on an "AS IS" BASIS,
 * WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 * See the License for the specific language governing permissions and
 * limitations under the License.
 */

#ifndef INCLUDE_VM_CATALOG_H_
#define INCLUDE_VM_CATALOG_H_
#include <map>
#include <memory>
#include <set>
#include <string>
#include <utility>
#include <vector>
#include "base/fe_slice.h"
#include "base/fe_status.h"
#include "codec/fe_row_codec.h"
#include "codec/list_iterator_codec.h"
#include "codec/row.h"
#include "proto/fe_type.pb.h"
#include "sdk/base.h"

namespace hybridse {
namespace vm {

using hybridse::codec::ColInfo;
using hybridse::codec::ListV;
using hybridse::codec::Row;
using hybridse::codec::RowIterator;
using hybridse::codec::Schema;
using hybridse::codec::WindowIterator;

constexpr uint32_t INVALID_POS = UINT32_MAX;  

struct IndexSt {
    std::string name;           
    uint32_t index;             
    uint32_t ts_pos;            
    std::vector<ColInfo> keys;  
};

typedef ::google::protobuf::RepeatedPtrField<::hybridse::type::IndexDef>
    IndexList;
typedef std::map<std::string, ColInfo> Types;
typedef std::map<std::string, IndexSt> IndexHint;

class PartitionHandler;
class TableHandler;
class RowHandler;
class Tablet;

enum HandlerType { kRowHandler, kTableHandler, kPartitionHandler };
enum OrderType { kDescOrder, kAscOrder, kNoneOrder };

class DataHandler : public ListV<Row> {
 public:
    DataHandler() {}
    virtual ~DataHandler() {}
    virtual const Schema* GetSchema() = 0;

    virtual const std::string& GetName() = 0;

    virtual const std::string& GetDatabase() = 0;

    virtual const HandlerType GetHanlderType() = 0;
    virtual const std::string GetHandlerTypeName() = 0;
    virtual base::Status GetStatus() { return base::Status::OK(); }
};

class DataHandlerList {
 public:
    DataHandlerList() {}
    virtual ~DataHandlerList() {}
    virtual size_t GetSize() = 0;
    virtual std::shared_ptr<DataHandler> Get(size_t idx) = 0;
};

class DataHandlerVector : public DataHandlerList {
 public:
    DataHandlerVector() : data_handlers_() {}
    ~DataHandlerVector() {}
    void Add(std::shared_ptr<DataHandler> data_handler) {
        data_handlers_.push_back(data_handler);
    }
    size_t GetSize() { return data_handlers_.size(); }
    std::shared_ptr<DataHandler> Get(size_t idx) {
        return idx < data_handlers_.size() ? data_handlers_[idx]
                                           : std::shared_ptr<DataHandler>();
    }

 private:
    std::vector<std::shared_ptr<DataHandler>> data_handlers_;
};
class DataHandlerRepeater : public DataHandlerList {
 public:
    DataHandlerRepeater(std::shared_ptr<DataHandler> data_handler, size_t size)
        : size_(size), data_handler_(data_handler) {}
    ~DataHandlerRepeater() {}

    size_t GetSize() { return size_; }
    std::shared_ptr<DataHandler> Get(size_t idx) {
        return idx < size_ ? data_handler_ : std::shared_ptr<DataHandler>();
    }

 private:
    size_t size_;
    std::shared_ptr<DataHandler> data_handler_;
};

class RowHandler : public DataHandler {
 public:
    RowHandler() {}

    virtual ~RowHandler() {}
    std::unique_ptr<RowIterator> GetIterator() override {
        return std::unique_ptr<RowIterator>();
    }
    RowIterator* GetRawIterator() override { return nullptr; }

    const uint64_t GetCount() override { return 0; }

    Row At(uint64_t pos) override { return Row(); }

    const HandlerType GetHanlderType() override { return kRowHandler; }

    virtual const Row& GetValue() = 0;

    const std::string GetHandlerTypeName() override { return "RowHandler"; }
};

class ErrorRowHandler : public RowHandler {
 public:
    ErrorRowHandler(common::StatusCode status_code, const std::string& msg_str)
        : status_(status_code, msg_str),
          table_name_(""),
          db_(""),
          schema_(nullptr),
          row_() {}
    ~ErrorRowHandler() {}

    const Row& GetValue() final { return row_; }

    const std::string GetHandlerTypeName() override {
        return "ErrorRowHandler";
    }
    const Schema* GetSchema() override { return nullptr; }
    const std::string& GetName() override { return table_name_; }
    const std::string& GetDatabase() override { return db_; }
    virtual base::Status GetStatus() { return status_; }

 private:
    base::Status status_;
    std::string table_name_;
    std::string db_;
    const Schema* schema_;
    Row row_;
};

class TableHandler : public DataHandler {
 public:
    TableHandler() : DataHandler() {}

    virtual ~TableHandler() {}

    virtual const Types& GetTypes() = 0;

    virtual const IndexHint& GetIndex() = 0;

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

class ErrorTableHandler : public TableHandler {
 public:
    ErrorTableHandler()
        : status_(common::kCallMethodError, "error"),
          table_name_(""),
          db_(""),
          schema_(nullptr),
          types_(),
          index_hint_() {}
    ErrorTableHandler(common::StatusCode status_code,
                      const std::string& msg_str)
        : status_(status_code, msg_str),
          table_name_(""),
          db_(""),
          schema_(nullptr),
          types_(),
          index_hint_() {}
    ~ErrorTableHandler() {}

    const Types& GetTypes() override { return types_; }
    inline const Schema* GetSchema() override { return schema_; }
    inline const std::string& GetName() override { return table_name_; }
    inline const IndexHint& GetIndex() override { return index_hint_; }
    inline const std::string& GetDatabase() override { return db_; }

    std::unique_ptr<RowIterator> GetIterator() {
        return std::unique_ptr<RowIterator>();
    }
    RowIterator* GetRawIterator() { return nullptr; }
    std::unique_ptr<WindowIterator> GetWindowIterator(
        const std::string& idx_name) {
        return std::unique_ptr<WindowIterator>();
    }
    virtual Row At(uint64_t pos) { return Row(); }

    const uint64_t GetCount() override { return 0; }

    const std::string GetHandlerTypeName() override {
        return "ErrorTableHandler";
    }

    virtual base::Status GetStatus() { return status_; }

 protected:
    base::Status status_;
    const std::string table_name_;
    const std::string db_;
    const Schema* schema_;
    Types types_;
    IndexHint index_hint_;
    OrderType order_type_;
};

class PartitionHandler : public TableHandler {
 public:
    PartitionHandler() : TableHandler() {}
    ~PartitionHandler() {}

    virtual std::unique_ptr<RowIterator> GetIterator() {
        return std::unique_ptr<RowIterator>();
    }
    RowIterator* GetRawIterator() { return nullptr; }
    virtual std::unique_ptr<WindowIterator> GetWindowIterator(
        const std::string& idx_name) {
        return std::unique_ptr<WindowIterator>();
    }

    virtual std::unique_ptr<WindowIterator> GetWindowIterator() = 0;

    const HandlerType GetHanlderType() override { return kPartitionHandler; }

    virtual Row At(uint64_t pos) { return Row(); }

    virtual std::shared_ptr<TableHandler> GetSegment(const std::string& key) {
        return std::shared_ptr<TableHandler>();
    }

    virtual std::vector<std::shared_ptr<TableHandler>> GetSegments(
        const std::vector<std::string>& keys) {
        std::vector<std::shared_ptr<TableHandler>> segments;
        for (auto key : keys) {
            segments.push_back(GetSegment(key));
        }
        return segments;
    }
    const std::string GetHandlerTypeName() override {
        return "PartitionHandler";
    }
    const OrderType GetOrderType() const { return kNoneOrder; }
};

class AysncRowHandler : public RowHandler {
 public:
    AysncRowHandler(size_t idx,
                    std::shared_ptr<TableHandler> aysnc_table_handler)
        : RowHandler(),
          status_(base::Status::Running()),
          table_name_(""),
          db_(""),
          schema_(nullptr),
          idx_(idx),
          aysnc_table_handler_(aysnc_table_handler),
          value_() {
        if (!aysnc_table_handler_) {
            status_ = base::Status(hybridse::common::kNullPointer,
                                   "async table handler is null");
        }
    }
    virtual ~AysncRowHandler() {}

    const Row& GetValue() override {
        if (!status_.isRunning()) {
            return value_;
        }
        value_ = aysnc_table_handler_->At(idx_);
        status_ = aysnc_table_handler_->GetStatus();
        return value_;
    }
    const Schema* GetSchema() override { return schema_; }
    const std::string& GetName() override { return table_name_; }
    const std::string& GetDatabase() override { return db_; }

 private:
    base::Status status_;
    std::string table_name_;
    std::string db_;
    const Schema* schema_;
    size_t idx_;
    std::shared_ptr<TableHandler> aysnc_table_handler_;
    Row value_;
};

class Tablet {
 public:
    Tablet() {}
    virtual ~Tablet() {}
    virtual const std::string& GetName() const = 0;
    virtual std::shared_ptr<RowHandler> SubQuery(
        uint32_t task_id, const std::string& db, const std::string& sql,
        const hybridse::codec::Row& row, const bool is_procedure,
        const bool is_debug) = 0;
    virtual std::shared_ptr<TableHandler> SubQuery(
        uint32_t task_id, const std::string& db, const std::string& sql,
        const std::set<size_t>& common_column_indices,
        const std::vector<Row>& in_rows, const bool request_is_common,
        const bool is_procedure, const bool is_debug) = 0;
};

class Catalog {
 public:
    Catalog() {}

    virtual ~Catalog() {}

    virtual bool IndexSupport() = 0;

    virtual std::shared_ptr<type::Database> GetDatabase(
        const std::string& db) = 0;

    virtual std::shared_ptr<TableHandler> GetTable(
        const std::string& db, const std::string& table_name) = 0;

    virtual std::shared_ptr<hybridse::sdk::ProcedureInfo> GetProcedureInfo(
        const std::string& db, const std::string& sp_name) {
        return nullptr;
    }
};

}  // namespace vm
}  // namespace hybridse

#endif  // INCLUDE_VM_CATALOG_H_
```


-------------------------------

Updated on  6 April 2021 at 08:47:46 PDT
