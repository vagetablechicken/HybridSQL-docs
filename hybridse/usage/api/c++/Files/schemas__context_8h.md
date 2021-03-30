---
title: /Users/chenjing/work/4paradigm/HybridSE/include/vm/schemas_context.h

---
# /Users/chenjing/work/4paradigm/HybridSE/include/vm/schemas_context.h

## Namespaces

| Name           |
| -------------- |
| **[hybridse](/hybridse/usage/api/c++/Namespaces/namespacehybridse.md)**  |
| **[hybridse::vm](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md)**  |

## Classes

|                | Name           |
| -------------- | -------------- |
| class | **[hybridse::vm::SchemaSource](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schema_source.md)**  |
| class | **[hybridse::vm::SchemasContext](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schemas_context.md)**  |




## Source code

```cpp
/*
 * Copyright 2021 4Paradigm
 *
 * Licensed under the Apache License, Version 2.0 (the "License");
 * you may not use this file except in compliance with the License.
 * You may obtain a copy of the License at
 *
 *   http://www.apache.org/licenses/LICENSE-2.0
 *
 * Unless required by applicable law or agreed to in writing, software
 * distributed under the License is distributed on an "AS IS" BASIS,
 * WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 * See the License for the specific language governing permissions and
 * limitations under the License.
 */

#ifndef SRC_INCLUDE_VM_SCHEMAS_CONTEXT_H_
#define SRC_INCLUDE_VM_SCHEMAS_CONTEXT_H_
#include <map>
#include <set>
#include <string>
#include <utility>
#include <vector>
#include "base/fe_status.h"
#include "codec/fe_row_codec.h"
#include "node/sql_node.h"

namespace hybridse {
namespace vm {

// Forward decls
class PhysicalOpNode;
class PhysicalPlanContext;

class SchemaSource {
 public:
    const hybridse::codec::Schema* GetSchema() const { return schema_; }
    size_t GetColumnID(size_t idx) const;
    const std::string& GetColumnName(size_t idx) const;
    const hybridse::type::Type GetColumnType(size_t idx) const;
    const std::string& GetSourceName() const;

    // build utility
    void SetSchema(const codec::Schema* schema);
    void SetSourceName(const std::string& name);
    void SetColumnID(size_t idx, size_t column_id);
    void SetSource(size_t idx, size_t child_idx, size_t child_column_id);
    void SetNonSource(size_t idx);

    // source column tracking info
    int GetSourceColumnID(size_t idx) const;
    int GetSourceChildIdx(size_t idx) const;
    bool IsSourceColumn(size_t idx) const;
    bool IsStrictSourceColumn(size_t idx) const;

    size_t size() const;
    void Clear();

    std::string ToString() const;

 private:
    bool CheckSourceSetIndex(size_t idx) const;

    const codec::Schema* schema_;

    std::string source_name_ = "";

    // column identifier of each output column
    std::vector<size_t> column_ids_;

    // trace which child and which column id each column come from
    // -1 means the column is created from current node
    std::vector<int> source_child_idxs_;
    std::vector<size_t> source_child_column_ids_;
};

class SchemasContext {
 public:
    SchemasContext() : root_(nullptr) {}
    explicit SchemasContext(const PhysicalOpNode* root) : root_(root) {}
    ~SchemasContext();

    base::Status ResolveColumnIndexByName(const std::string& relation_name,
                                          const std::string& column_name,
                                          size_t* schema_idx,
                                          size_t* col_idx) const;

    base::Status ResolveColumnIndexByID(size_t column_id, size_t* schema_idx,
                                        size_t* col_idx) const;

    base::Status ResolveColumnNameByID(size_t column_id,
                                       std::string* name) const;

    base::Status ResolveColumnRefIndex(const node::ColumnRefNode* column_ref,
                                       size_t* schema_idx,
                                       size_t* col_idx) const;

    base::Status ResolveColumnID(const std::string& relation_name,
                                 const std::string& column_name,
                                 size_t* column_id) const;

    base::Status ResolveColumnID(const std::string& relation_name,
                                 const std::string& column_name,
                                 size_t* column_id, int* child_path_idx,
                                 size_t* child_column_id,
                                 size_t* source_column_id,
                                 const PhysicalOpNode** source_node) const;
    base::Status ResolveExprDependentColumns(
        const node::ExprNode* expr, std::set<size_t>* column_ids) const;
    base::Status ResolveExprDependentColumns(
        const node::ExprNode* expr,
        std::vector<const node::ExprNode*>* columns) const;

    const std::string& GetName() const;

    const PhysicalOpNode* GetRoot() const;

    const codec::RowFormat* GetRowFormat(size_t idx) const;

    const SchemaSource* GetSchemaSource(size_t idx) const;

    const codec::Schema* GetSchema(size_t idx) const;

    size_t GetSchemaSourceSize() const;

    void SetName(const std::string& name);

    SchemaSource* AddSource();

    void Merge(size_t child_idx, const SchemasContext* child);

    void MergeWithNewID(size_t child_idx, const SchemasContext* child,
                        PhysicalPlanContext* plan_ctx);

    void Clear();
    void Build();

    bool Empty() const { return schema_sources_.empty(); }

    size_t GetColumnNum() const;

    const codec::Schema* GetOutputSchema() const;

    void BuildTrivial(const std::vector<const codec::Schema*>& schemas);
    void BuildTrivial(const std::vector<const type::TableDef*>& tables);

 private:
    bool IsColumnAmbiguous(const std::string& column_name) const;

    bool CheckBuild() const;

    // root node to search column id, can be null
    const PhysicalOpNode* root_ = nullptr;
    std::string root_relation_name_ = "";

    // column id -> (schema idx, column idx) mapping
    std::map<size_t, std::pair<size_t, size_t>> column_id_map_;

    // column name -> [(schema idx, column idx)] mapping
    std::map<std::string, std::vector<std::pair<size_t, size_t>>>
        column_name_map_;

    // child source mapping
    // child idx -> (child column id -> column idx)
    std::map<size_t, std::map<size_t, size_t>> child_source_map_;

    // schema source parts
    std::vector<SchemaSource*> schema_sources_;

    // detailed schema format info
    std::vector<codec::RowFormat> row_formats_;

    // owned schema object
    codec::Schema owned_concat_output_schema_;
};
}  // namespace vm
}  // namespace hybridse

#endif  // SRC_INCLUDE_VM_SCHEMAS_CONTEXT_H_
```


-------------------------------

Updated on 29 March 2021 at 18:05:16 PDT
