---
title: hybridse::vm::SchemaSource

---
# hybridse::vm::SchemaSource



`#include <schemas_context.h>`

## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[GetSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schema_source.md#function-getschema)**() const| const [hybridse::codec::Schema](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1codec.md#typedef-schema) *  |
|**[GetColumnID](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schema_source.md#function-getcolumnid)**(size_t idx) const| size_t  |
|**[GetColumnName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schema_source.md#function-getcolumnname)**(size_t idx) const| const std::string &  |
|**[GetColumnType](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schema_source.md#function-getcolumntype)**(size_t idx) const| const hybridse::type::Type  |
|**[GetSourceName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schema_source.md#function-getsourcename)**() const| const std::string &  |
|**[SetSchema](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schema_source.md#function-setschema)**(const [codec::Schema](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1codec.md#typedef-schema) * schema)| void  |
|**[SetSourceName](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schema_source.md#function-setsourcename)**(const std::string & name)| void  |
|**[SetColumnID](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schema_source.md#function-setcolumnid)**(size_t idx, size_t column_id)| void  |
|**[SetSource](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schema_source.md#function-setsource)**(size_t idx, size_t child_idx, size_t child_column_id)| void  |
|**[SetNonSource](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schema_source.md#function-setnonsource)**(size_t idx)| void  |
|**[GetSourceColumnID](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schema_source.md#function-getsourcecolumnid)**(size_t idx) const| int  |
|**[GetSourceChildIdx](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schema_source.md#function-getsourcechildidx)**(size_t idx) const| int  |
|**[IsSourceColumn](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schema_source.md#function-issourcecolumn)**(size_t idx) const| bool  |
|**[IsStrictSourceColumn](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schema_source.md#function-isstrictsourcecolumn)**(size_t idx) const| bool  |
|**[size](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schema_source.md#function-size)**() const| size_t  |
|**[Clear](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schema_source.md#function-clear)**()| void  |
|**[ToString](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schema_source.md#function-tostring)**() const| std::string  |

## Public Functions

#### GetSchema

```cpp
inline const hybridse::codec::Schema * GetSchema() const
```


#### GetColumnID

```cpp
size_t GetColumnID(
    size_t idx
) const
```


#### GetColumnName

```cpp
const std::string & GetColumnName(
    size_t idx
) const
```


#### GetColumnType

```cpp
const hybridse::type::Type GetColumnType(
    size_t idx
) const
```


#### GetSourceName

```cpp
const std::string & GetSourceName() const
```


#### SetSchema

```cpp
void SetSchema(
    const codec::Schema * schema
)
```


#### SetSourceName

```cpp
void SetSourceName(
    const std::string & name
)
```


#### SetColumnID

```cpp
void SetColumnID(
    size_t idx,
    size_t column_id
)
```


#### SetSource

```cpp
void SetSource(
    size_t idx,
    size_t child_idx,
    size_t child_column_id
)
```


#### SetNonSource

```cpp
void SetNonSource(
    size_t idx
)
```


#### GetSourceColumnID

```cpp
int GetSourceColumnID(
    size_t idx
) const
```


#### GetSourceChildIdx

```cpp
int GetSourceChildIdx(
    size_t idx
) const
```


#### IsSourceColumn

```cpp
bool IsSourceColumn(
    size_t idx
) const
```


#### IsStrictSourceColumn

```cpp
bool IsStrictSourceColumn(
    size_t idx
) const
```


#### size

```cpp
size_t size() const
```


#### Clear

```cpp
void Clear()
```


#### ToString

```cpp
std::string ToString() const
```


-------------------------------

Updated on 29 March 2021 at 17:34:52 PDT