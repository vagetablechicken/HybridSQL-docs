---
title: hybridse::vm::EngineOptions

---

# hybridse::vm::EngineOptions




`#include <engine.h>`

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[EngineOptions](/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-engineoptions)**() |
| void | **[set_keep_ir](/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-set_keep_ir)**(bool flag) |
| bool | **[is_keep_ir](/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-is_keep_ir)**() const |
| void | **[set_compile_only](/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-set_compile_only)**(bool flag) |
| bool | **[is_compile_only](/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-is_compile_only)**() const |
| bool | **[is_plan_only](/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-is_plan_only)**() const |
| void | **[set_plan_only](/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-set_plan_only)**(bool flag) |
| bool | **[is_performance_sensitive](/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-is_performance_sensitive)**() const |
| uint32_t | **[max_sql_cache_size](/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-max_sql_cache_size)**() const |
| void | **[set_performance_sensitive](/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-set_performance_sensitive)**(bool flag) |
| bool | **[is_cluster_optimzied](/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-is_cluster_optimzied)**() const |
| [EngineOptions](/Classes/classhybridse_1_1vm_1_1_engine_options.md) * | **[set_cluster_optimized](/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-set_cluster_optimized)**(bool flag) |
| bool | **[is_batch_request_optimized](/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-is_batch_request_optimized)**() const |
| [EngineOptions](/Classes/classhybridse_1_1vm_1_1_engine_options.md) * | **[set_batch_request_optimized](/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-set_batch_request_optimized)**(bool flag) |
| void | **[set_max_sql_cache_size](/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-set_max_sql_cache_size)**(uint32_t size) |
| bool | **[is_enable_expr_optimize](/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-is_enable_expr_optimize)**() const |
| [EngineOptions](/Classes/classhybridse_1_1vm_1_1_engine_options.md) * | **[set_enable_expr_optimize](/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-set_enable_expr_optimize)**(bool flag) |
| [EngineOptions](/Classes/classhybridse_1_1vm_1_1_engine_options.md) * | **[set_enable_batch_window_parallelization](/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-set_enable_batch_window_parallelization)**(bool flag) |
| bool | **[is_enable_batch_window_parallelization](/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-is_enable_batch_window_parallelization)**() const |
| [EngineOptions](/Classes/classhybridse_1_1vm_1_1_engine_options.md) * | **[set_enable_spark_unsaferow_format](/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-set_enable_spark_unsaferow_format)**(bool flag) |
| bool | **[is_enable_spark_unsaferow_format](/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-is_enable_spark_unsaferow_format)**() const |
| [hybridse::vm::JITOptions](/Classes/classhybridse_1_1vm_1_1_j_i_t_options.md) & | **[jit_options](/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-jit_options)**() |
| [EngineOptions](/Classes/classhybridse_1_1vm_1_1_engine_options.md) | **[NewEngineOptionWithClusterEnable](/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-newengineoptionwithclusterenable)**(bool flag) |

## Public Functions Documentation

### function EngineOptions

```cpp
EngineOptions()
```


### function set_keep_ir

```cpp
inline void set_keep_ir(
    bool flag
)
```


### function is_keep_ir

```cpp
inline bool is_keep_ir() const
```


### function set_compile_only

```cpp
inline void set_compile_only(
    bool flag
)
```


### function is_compile_only

```cpp
inline bool is_compile_only() const
```


### function is_plan_only

```cpp
inline bool is_plan_only() const
```


### function set_plan_only

```cpp
inline void set_plan_only(
    bool flag
)
```


### function is_performance_sensitive

```cpp
inline bool is_performance_sensitive() const
```


### function max_sql_cache_size

```cpp
inline uint32_t max_sql_cache_size() const
```


### function set_performance_sensitive

```cpp
inline void set_performance_sensitive(
    bool flag
)
```


### function is_cluster_optimzied

```cpp
inline bool is_cluster_optimzied() const
```


### function set_cluster_optimized

```cpp
inline EngineOptions * set_cluster_optimized(
    bool flag
)
```


### function is_batch_request_optimized

```cpp
inline bool is_batch_request_optimized() const
```


### function set_batch_request_optimized

```cpp
inline EngineOptions * set_batch_request_optimized(
    bool flag
)
```


### function set_max_sql_cache_size

```cpp
inline void set_max_sql_cache_size(
    uint32_t size
)
```


### function is_enable_expr_optimize

```cpp
inline bool is_enable_expr_optimize() const
```


### function set_enable_expr_optimize

```cpp
inline EngineOptions * set_enable_expr_optimize(
    bool flag
)
```


### function set_enable_batch_window_parallelization

```cpp
inline EngineOptions * set_enable_batch_window_parallelization(
    bool flag
)
```


### function is_enable_batch_window_parallelization

```cpp
inline bool is_enable_batch_window_parallelization() const
```


### function set_enable_spark_unsaferow_format

```cpp
EngineOptions * set_enable_spark_unsaferow_format(
    bool flag
)
```


### function is_enable_spark_unsaferow_format

```cpp
inline bool is_enable_spark_unsaferow_format() const
```


### function jit_options

```cpp
inline hybridse::vm::JITOptions & jit_options()
```


### function NewEngineOptionWithClusterEnable

```cpp
static inline EngineOptions NewEngineOptionWithClusterEnable(
    bool flag
)
```


-------------------------------

Updated on 28 March 2021 at 19:23:48 PDT