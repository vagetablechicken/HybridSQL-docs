---
title: hybridse::vm::ExplainOutput
summary: An options class for controlling runtime interpreter behavior. 

---
# hybridse::vm::ExplainOutput



`#include <engine.h>`

An options class for controlling runtime interpreter behavior. 
## Summary


| **Public attributes**|    |
| -------------- | -------------- |
| **[input_schema](/hybridse/usage/api/c++/Classes/structhybridse_1_1vm_1_1_explain_output.md#variable-input_schema)**| vm::Schema <br>The schema of request row for request-mode query.  |
| **[request_name](/hybridse/usage/api/c++/Classes/structhybridse_1_1vm_1_1_explain_output.md#variable-request_name)**| std::string <br>The name of request for request-mode query.  |
| **[logical_plan](/hybridse/usage/api/c++/Classes/structhybridse_1_1vm_1_1_explain_output.md#variable-logical_plan)**| std::string <br>Logical plan string.  |
| **[physical_plan](/hybridse/usage/api/c++/Classes/structhybridse_1_1vm_1_1_explain_output.md#variable-physical_plan)**| std::string <br>Physical plan string.  |
| **[ir](/hybridse/usage/api/c++/Classes/structhybridse_1_1vm_1_1_explain_output.md#variable-ir)**| std::string <br>Codegen IR String.  |
| **[output_schema](/hybridse/usage/api/c++/Classes/structhybridse_1_1vm_1_1_explain_output.md#variable-output_schema)**| vm::Schema <br>The schema of query result.  |
| **[router](/hybridse/usage/api/c++/Classes/structhybridse_1_1vm_1_1_explain_output.md#variable-router)**| [vm::Router](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_router.md) <br>The [Router]() for request-mode query.  |

## Public Attributes

### variable input_schema

```cpp
vm::Schema input_schema;
```

The schema of request row for request-mode query. 

### variable request_name

```cpp
std::string request_name;
```

The name of request for request-mode query. 

### variable logical_plan

```cpp
std::string logical_plan;
```

Logical plan string. 

### variable physical_plan

```cpp
std::string physical_plan;
```

Physical plan string. 

### variable ir

```cpp
std::string ir;
```

Codegen IR String. 

### variable output_schema

```cpp
vm::Schema output_schema;
```

The schema of query result. 

### variable router

```cpp
vm::Router router;
```

The [Router]() for request-mode query. 

-------------------------------

Updated on  6 April 2021 at 19:38:01 PDT