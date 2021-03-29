---
title: hybridse::vm::SchemaSource

---

# hybridse::vm::SchemaSource




`#include <schemas_context.h>`

## Public Functions

|                | Name           |
| -------------- | -------------- |
| const hybridse::codec::Schema * | **[GetSchema](/Classes/classhybridse_1_1vm_1_1_schema_source.md#function-getschema)**() const |
| size_t | **[GetColumnID](/Classes/classhybridse_1_1vm_1_1_schema_source.md#function-getcolumnid)**(size_t idx) const |
| const std::string & | **[GetColumnName](/Classes/classhybridse_1_1vm_1_1_schema_source.md#function-getcolumnname)**(size_t idx) const |
| const hybridse::type::Type | **[GetColumnType](/Classes/classhybridse_1_1vm_1_1_schema_source.md#function-getcolumntype)**(size_t idx) const |
| const std::string & | **[GetSourceName](/Classes/classhybridse_1_1vm_1_1_schema_source.md#function-getsourcename)**() const |
| void | **[SetSchema](/Classes/classhybridse_1_1vm_1_1_schema_source.md#function-setschema)**(const codec::Schema * schema) |
| void | **[SetSourceName](/Classes/classhybridse_1_1vm_1_1_schema_source.md#function-setsourcename)**(const std::string & name) |
| void | **[SetColumnID](/Classes/classhybridse_1_1vm_1_1_schema_source.md#function-setcolumnid)**(size_t idx, size_t column_id) |
| void | **[SetSource](/Classes/classhybridse_1_1vm_1_1_schema_source.md#function-setsource)**(size_t idx, size_t child_idx, size_t child_column_id) |
| void | **[SetNonSource](/Classes/classhybridse_1_1vm_1_1_schema_source.md#function-setnonsource)**(size_t idx) |
| int | **[GetSourceColumnID](/Classes/classhybridse_1_1vm_1_1_schema_source.md#function-getsourcecolumnid)**(size_t idx) const |
| int | **[GetSourceChildIdx](/Classes/classhybridse_1_1vm_1_1_schema_source.md#function-getsourcechildidx)**(size_t idx) const |
| bool | **[IsSourceColumn](/Classes/classhybridse_1_1vm_1_1_schema_source.md#function-issourcecolumn)**(size_t idx) const |
| bool | **[IsStrictSourceColumn](/Classes/classhybridse_1_1vm_1_1_schema_source.md#function-isstrictsourcecolumn)**(size_t idx) const |
| size_t | **[size](/Classes/classhybridse_1_1vm_1_1_schema_source.md#function-size)**() const |
| void | **[Clear](/Classes/classhybridse_1_1vm_1_1_schema_source.md#function-clear)**() |
| std::string | **[ToString](/Classes/classhybridse_1_1vm_1_1_schema_source.md#function-tostring)**() const |

## Public Functions Documentation

### function GetSchema

```cpp
inline const hybridse::codec::Schema * GetSchema() const
```


### function GetColumnID

```cpp
size_t GetColumnID(
    size_t idx
) const
```


### function GetColumnName

```cpp
const std::string & GetColumnName(
    size_t idx
) const
```


### function GetColumnType

```cpp
const hybridse::type::Type GetColumnType(
    size_t idx
) const
```


### function GetSourceName

```cpp
const std::string & GetSourceName() const
```


### function SetSchema

```cpp
void SetSchema(
    const codec::Schema * schema
)
```


### function SetSourceName

```cpp
void SetSourceName(
    const std::string & name
)
```


### function SetColumnID

```cpp
void SetColumnID(
    size_t idx,
    size_t column_id
)
```


### function SetSource

```cpp
void SetSource(
    size_t idx,
    size_t child_idx,
    size_t child_column_id
)
```


### function SetNonSource

```cpp
void SetNonSource(
    size_t idx
)
```


### function GetSourceColumnID

```cpp
int GetSourceColumnID(
    size_t idx
) const
```


### function GetSourceChildIdx

```cpp
int GetSourceChildIdx(
    size_t idx
) const
```


### function IsSourceColumn

```cpp
bool IsSourceColumn(
    size_t idx
) const
```


### function IsStrictSourceColumn

```cpp
bool IsStrictSourceColumn(
    size_t idx
) const
```


### function size

```cpp
size_t size() const
```


### function Clear

```cpp
void Clear()
```


### function ToString

```cpp
std::string ToString() const
```


-------------------------------

Updated on 28 March 2021 at 19:23:48 PDT