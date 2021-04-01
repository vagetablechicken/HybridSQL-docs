---
title: hybridse::vm::SchemasContext

---
# hybridse::vm::SchemasContext



`#include <schemas_context.h>`

## Summary

```cpp
class hybridse::vm::SchemasContext;
```

Utility context to resolve column spec into detailed column information. This class should be explicitly initialized with schema source list info or some physical node with schema intiailized. If initialized by physical node, current context will take a relation name used when column search is assiociated with a relation name. and the node graph can be traversed to resolve column inherited from input nodes. 



|  Public functions|            |
| -------------- | -------------- |
|**[SchemasContext](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schemas_context.md#function-schemascontext)**()|  |
|**[SchemasContext](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schemas_context.md#function-schemascontext)**(const PhysicalOpNode * root)|  |
|**[~SchemasContext](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schemas_context.md#function-~schemascontext)**()|  |
|**[ResolveColumnIndexByName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schemas_context.md#function-resolvecolumnindexbyname)**(const std::string & relation_name, const std::string & column_name, size_t * schema_idx, size_t * col_idx) const| base::Status  |
|**[ResolveColumnIndexByID](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schemas_context.md#function-resolvecolumnindexbyid)**(size_t column_id, size_t * schema_idx, size_t * col_idx) const| base::Status  |
|**[ResolveColumnNameByID](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schemas_context.md#function-resolvecolumnnamebyid)**(size_t column_id, std::string * name) const| base::Status  |
|**[ResolveColumnRefIndex](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schemas_context.md#function-resolvecolumnrefindex)**(const node::ColumnRefNode * column_ref, size_t * schema_idx, size_t * col_idx) const| base::Status  |
|**[ResolveColumnID](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schemas_context.md#function-resolvecolumnid)**(const std::string & relation_name, const std::string & column_name, size_t * column_id) const| base::Status  |
|**[ResolveColumnID](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schemas_context.md#function-resolvecolumnid)**(const std::string & relation_name, const std::string & column_name, size_t * column_id, int * child_path_idx, size_t * child_column_id, size_t * source_column_id, const PhysicalOpNode ** source_node) const| base::Status  |
|**[ResolveExprDependentColumns](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schemas_context.md#function-resolveexprdependentcolumns)**(const node::ExprNode * expr, std::set< size_t > * column_ids) const| base::Status  |
|**[ResolveExprDependentColumns](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schemas_context.md#function-resolveexprdependentcolumns)**(const node::ExprNode * expr, std::vector< const node::ExprNode * > * columns) const| base::Status  |
|**[GetName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schemas_context.md#function-getname)**() const| const std::string &  |
|**[GetRoot](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schemas_context.md#function-getroot)**() const| const PhysicalOpNode *  |
|**[GetRowFormat](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schemas_context.md#function-getrowformat)**(size_t idx) const| const [codec::RowFormat](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_format.md) *  |
|**[GetSchemaSource](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schemas_context.md#function-getschemasource)**(size_t idx) const| const [SchemaSource](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schema_source.md) *  |
|**[GetSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schemas_context.md#function-getschema)**(size_t idx) const| const [codec::Schema](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1codec.md#typedef-schema) *  |
|**[GetSchemaSourceSize](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schemas_context.md#function-getschemasourcesize)**() const| size_t  |
|**[SetName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schemas_context.md#function-setname)**(const std::string & name)| void  |
|**[AddSource](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schemas_context.md#function-addsource)**()| [SchemaSource](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schema_source.md) *  |
|**[Merge](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schemas_context.md#function-merge)**(size_t child_idx, const [SchemasContext](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schemas_context.md) * child)| void  |
|**[MergeWithNewID](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schemas_context.md#function-mergewithnewid)**(size_t child_idx, const [SchemasContext](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schemas_context.md) * child, PhysicalPlanContext * plan_ctx)| void  |
|**[Clear](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schemas_context.md#function-clear)**()| void  |
|**[Build](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schemas_context.md#function-build)**()| void  |
|**[Empty](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schemas_context.md#function-empty)**() const| bool  |
|**[GetColumnNum](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schemas_context.md#function-getcolumnnum)**() const| size_t  |
|**[GetOutputSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schemas_context.md#function-getoutputschema)**() const| const [codec::Schema](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1codec.md#typedef-schema) *  |
|**[BuildTrivial](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schemas_context.md#function-buildtrivial)**(const std::vector< const [codec::Schema](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1codec.md#typedef-schema) * > & schemas)| void  |
|**[BuildTrivial](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schemas_context.md#function-buildtrivial)**(const std::vector< const type::TableDef * > & tables)| void  |

## Public Functions

#### function SchemasContext

```cpp
inline SchemasContext()
```


#### function SchemasContext

```cpp
inline explicit SchemasContext(
    const PhysicalOpNode * root
)
```


#### function ~SchemasContext

```cpp
~SchemasContext()
```


#### function ResolveColumnIndexByName

```cpp
base::Status ResolveColumnIndexByName(
    const std::string & relation_name,
    const std::string & column_name,
    size_t * schema_idx,
    size_t * col_idx
) const
```


Given relation name and column name, return schema slice index and column index within current context. 


#### function ResolveColumnIndexByID

```cpp
base::Status ResolveColumnIndexByID(
    size_t column_id,
    size_t * schema_idx,
    size_t * col_idx
) const
```


Given unique column id, return schema slice index and column index within schema slice within current context. 


#### function ResolveColumnNameByID

```cpp
base::Status ResolveColumnNameByID(
    size_t column_id,
    std::string * name
) const
```


Given unique column id, return column name. 


#### function ResolveColumnRefIndex

```cpp
base::Status ResolveColumnRefIndex(
    const node::ColumnRefNode * column_ref,
    size_t * schema_idx,
    size_t * col_idx
) const
```


Resolve index for column reference expression 


#### function ResolveColumnID

```cpp
base::Status ResolveColumnID(
    const std::string & relation_name,
    const std::string & column_name,
    size_t * column_id
) const
```


Given relation name and column name, return column unique id under current context. 


#### function ResolveColumnID

```cpp
base::Status ResolveColumnID(
    const std::string & relation_name,
    const std::string & column_name,
    size_t * column_id,
    int * child_path_idx,
    size_t * child_column_id,
    size_t * source_column_id,
    const PhysicalOpNode ** source_node
) const
```


Resolve source column by relation name and column name recursively. If it can be resolved in current node, `child_path_id` is -1, else `child_path_id` is the index of the child which the column is resolved from. 


#### function ResolveExprDependentColumns

```cpp
base::Status ResolveExprDependentColumns(
    const node::ExprNode * expr,
    std::set< size_t > * column_ids
) const
```


Resolve all columns input expression will depend on. Return column id list. 


#### function ResolveExprDependentColumns

```cpp
base::Status ResolveExprDependentColumns(
    const node::ExprNode * expr,
    std::vector< const node::ExprNode * > * columns
) const
```


#### function GetName

```cpp
const std::string & GetName() const
```


Get the relation name for this schema context, default "" 


#### function GetRoot

```cpp
const PhysicalOpNode * GetRoot() const
```


#### function GetRowFormat

```cpp
const codec::RowFormat * GetRowFormat(
    size_t idx
) const
```


Get detailed format for `idx`th schema source. 


#### function GetSchemaSource

```cpp
const SchemaSource * GetSchemaSource(
    size_t idx
) const
```


Get `idx`th schema source. 


#### function GetSchema

```cpp
const codec::Schema * GetSchema(
    size_t idx
) const
```


Get raw schema for `idx`th schema source. 


#### function GetSchemaSourceSize

```cpp
size_t GetSchemaSourceSize() const
```


Get num of total schema sources. 


#### function SetName

```cpp
void SetName(
    const std::string & name
)
```


Set the relation name for this schema context. 


#### function AddSource

```cpp
SchemaSource * AddSource()
```


Add new schema source and return the mutable instance of added source. 


#### function Merge

```cpp
void Merge(
    size_t child_idx,
    const SchemasContext * child
)
```


Add schema sources from child and inherit column identifiers. 


#### function MergeWithNewID

```cpp
void MergeWithNewID(
    size_t child_idx,
    const SchemasContext * child,
    PhysicalPlanContext * plan_ctx
)
```


Add schema sources from child with new column identifiers. The source informations are set to traceback which child column the new column is from. 


#### function Clear

```cpp
void Clear()
```


#### function Build

```cpp
void Build()
```


#### function Empty

```cpp
inline bool Empty() const
```


#### function GetColumnNum

```cpp
size_t GetColumnNum() const
```


Get total column num of all schema sources. 


#### function GetOutputSchema

```cpp
const codec::Schema * GetOutputSchema() const
```


#### function BuildTrivial

```cpp
void BuildTrivial(
    const std::vector< const codec::Schema * > & schemas
)
```


Helper method to init schemas context with trival schema sources this can be commonly used when no plan node is provided. 


#### function BuildTrivial

```cpp
void BuildTrivial(
    const std::vector< const type::TableDef * > & tables
)
```


-------------------------------

Updated on  1 April 2021 at 16:11:23 PDT