---
title: hybridse::vm::EngineOptions

---
# hybridse::vm::EngineOptions



`#include <engine.h>`

## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[EngineOptions](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-engineoptions)**()|  |
|**[set_keep_ir](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-set_keep_ir)**(bool flag)| void  |
|**[is_keep_ir](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-is_keep_ir)**() const| bool  |
|**[set_compile_only](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-set_compile_only)**(bool flag)| void  |
|**[is_compile_only](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-is_compile_only)**() const| bool  |
|**[is_plan_only](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-is_plan_only)**() const| bool  |
|**[set_plan_only](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-set_plan_only)**(bool flag)| void  |
|**[is_performance_sensitive](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-is_performance_sensitive)**() const| bool  |
|**[max_sql_cache_size](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-max_sql_cache_size)**() const| uint32_t  |
|**[set_performance_sensitive](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-set_performance_sensitive)**(bool flag)| void  |
|**[is_cluster_optimzied](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-is_cluster_optimzied)**() const| bool  |
|**[set_cluster_optimized](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-set_cluster_optimized)**(bool flag)| [EngineOptions](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md) *  |
|**[is_batch_request_optimized](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-is_batch_request_optimized)**() const| bool  |
|**[set_batch_request_optimized](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-set_batch_request_optimized)**(bool flag)| [EngineOptions](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md) *  |
|**[set_max_sql_cache_size](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-set_max_sql_cache_size)**(uint32_t size)| void  |
|**[is_enable_expr_optimize](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-is_enable_expr_optimize)**() const| bool  |
|**[set_enable_expr_optimize](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-set_enable_expr_optimize)**(bool flag)| [EngineOptions](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md) *  |
|**[set_enable_batch_window_parallelization](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-set_enable_batch_window_parallelization)**(bool flag)| [EngineOptions](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md) *  |
|**[is_enable_batch_window_parallelization](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-is_enable_batch_window_parallelization)**() const| bool  |
|**[set_enable_spark_unsaferow_format](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-set_enable_spark_unsaferow_format)**(bool flag)| [EngineOptions](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md) *  |
|**[is_enable_spark_unsaferow_format](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-is_enable_spark_unsaferow_format)**() const| bool  |
|**[jit_options](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-jit_options)**()| [hybridse::vm::JITOptions](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_j_i_t_options.md) &  |
|**[NewEngineOptionWithClusterEnable](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-newengineoptionwithclusterenable)**(bool flag)| [EngineOptions](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md)  |

## Public Functions

#### EngineOptions { function EngineOptions }

```cpp
EngineOptions()
```


#### set_keep_ir { function set_keep_ir }

```cpp
inline void set_keep_ir(
    bool flag
)
```


#### is_keep_ir { function is_keep_ir }

```cpp
inline bool is_keep_ir() const
```


#### set_compile_only { function set_compile_only }

```cpp
inline void set_compile_only(
    bool flag
)
```


#### is_compile_only { function is_compile_only }

```cpp
inline bool is_compile_only() const
```


#### is_plan_only { function is_plan_only }

```cpp
inline bool is_plan_only() const
```


#### set_plan_only { function set_plan_only }

```cpp
inline void set_plan_only(
    bool flag
)
```


#### is_performance_sensitive { function is_performance_sensitive }

```cpp
inline bool is_performance_sensitive() const
```


#### max_sql_cache_size { function max_sql_cache_size }

```cpp
inline uint32_t max_sql_cache_size() const
```


#### set_performance_sensitive { function set_performance_sensitive }

```cpp
inline void set_performance_sensitive(
    bool flag
)
```


#### is_cluster_optimzied { function is_cluster_optimzied }

```cpp
inline bool is_cluster_optimzied() const
```


#### set_cluster_optimized { function set_cluster_optimized }

```cpp
inline EngineOptions * set_cluster_optimized(
    bool flag
)
```


#### is_batch_request_optimized { function is_batch_request_optimized }

```cpp
inline bool is_batch_request_optimized() const
```


#### set_batch_request_optimized { function set_batch_request_optimized }

```cpp
inline EngineOptions * set_batch_request_optimized(
    bool flag
)
```


#### set_max_sql_cache_size { function set_max_sql_cache_size }

```cpp
inline void set_max_sql_cache_size(
    uint32_t size
)
```


#### is_enable_expr_optimize { function is_enable_expr_optimize }

```cpp
inline bool is_enable_expr_optimize() const
```


#### set_enable_expr_optimize { function set_enable_expr_optimize }

```cpp
inline EngineOptions * set_enable_expr_optimize(
    bool flag
)
```


#### set_enable_batch_window_parallelization { function set_enable_batch_window_parallelization }

```cpp
inline EngineOptions * set_enable_batch_window_parallelization(
    bool flag
)
```


#### is_enable_batch_window_parallelization { function is_enable_batch_window_parallelization }

```cpp
inline bool is_enable_batch_window_parallelization() const
```


#### set_enable_spark_unsaferow_format { function set_enable_spark_unsaferow_format }

```cpp
EngineOptions * set_enable_spark_unsaferow_format(
    bool flag
)
```


#### is_enable_spark_unsaferow_format { function is_enable_spark_unsaferow_format }

```cpp
inline bool is_enable_spark_unsaferow_format() const
```


#### jit_options { function jit_options }

```cpp
inline hybridse::vm::JITOptions & jit_options()
```


#### NewEngineOptionWithClusterEnable { function NewEngineOptionWithClusterEnable }

```cpp
static inline EngineOptions NewEngineOptionWithClusterEnable(
    bool flag
)
```


-------------------------------

Updated on 29 March 2021 at 17:58:50 PDT