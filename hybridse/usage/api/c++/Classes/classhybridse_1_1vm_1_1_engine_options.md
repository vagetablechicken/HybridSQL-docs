---
title: hybridse::vm::EngineOptions
summary: An options class for controlling engine behaviour. 

---
# hybridse::vm::EngineOptions



`#include <engine.h>`

An options class for controlling engine behaviour. 
## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[EngineOptions](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-engineoptions)**()|  |
|**[set_keep_ir](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-set_keep_ir)**(bool flag)| void <br>Set if support to store ir results into SqlContext.  |
|**[is_keep_ir](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-is_keep_ir)**() const| bool <br>Return if support to store ir results into SqlContext.  |
|**[set_compile_only](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-set_compile_only)**(bool flag)| void  |
|**[is_compile_only](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-is_compile_only)**() const| bool <br>Return if only support to compile physical plan.  |
|**[set_plan_only](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-set_plan_only)**(bool flag)| void  |
|**[is_plan_only](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-is_plan_only)**() const| bool  |
|**[max_sql_cache_size](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-max_sql_cache_size)**() const| uint32_t <br>Return the maximum number of entries we can hold for compiling cache.  |
|**[set_max_sql_cache_size](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-set_max_sql_cache_size)**(uint32_t size)| void <br>Set the maxinum number of cache entries.  |
|**[set_performance_sensitive](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-set_performance_sensitive)**(bool flag)| void  |
|**[is_performance_sensitive](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-is_performance_sensitive)**() const| bool <br>Return if the engine is performance sensitive.  |
|**[set_cluster_optimized](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-set_cluster_optimized)**(bool flag)| [EngineOptions](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md) * <br>Set if the engine support cluster optimization.  |
|**[is_cluster_optimzied](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-is_cluster_optimzied)**() const| bool <br>Return if the engine support cluster optimization.  |
|**[set_batch_request_optimized](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-set_batch_request_optimized)**(bool flag)| [EngineOptions](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md) * <br>Set if the engine supoort batch request optimization.  |
|**[is_batch_request_optimized](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-is_batch_request_optimized)**() const| bool <br>Return if the engine support batch request optimization.  |
|**[set_enable_expr_optimize](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-set_enable_expr_optimize)**(bool flag)| [EngineOptions](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md) * <br>Set if the engine can support expression optimization.  |
|**[is_enable_expr_optimize](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-is_enable_expr_optimize)**() const| bool <br>Return if the engine support expression optimization.  |
|**[set_enable_batch_window_parallelization](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-set_enable_batch_window_parallelization)**(bool flag)| [EngineOptions](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md) * <br>Set if the engine can support batch window parallelization.  |
|**[is_enable_batch_window_parallelization](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-is_enable_batch_window_parallelization)**() const| bool <br>Return if the engine support batch window parallelization.  |
|**[set_enable_spark_unsaferow_format](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-set_enable_spark_unsaferow_format)**(bool flag)| [EngineOptions](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md) * <br>Set if the engine can support spark unsafe row format.  |
|**[is_enable_spark_unsaferow_format](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-is_enable_spark_unsaferow_format)**() const| bool <br>Return if the engine can support can support spark unsafe row format.  |
|**[jit_options](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md#function-jit_options)**()| [hybridse::vm::JitOptions](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_jit_options.md) & <br>Return [JitOptions]().  |

## Public Functions

#### function EngineOptions

```cpp
EngineOptions()
```


#### function set_keep_ir

```cpp
inline void set_keep_ir(
    bool flag
)
```

Set if support to store ir results into SqlContext. 

#### function is_keep_ir

```cpp
inline bool is_keep_ir() const
```

Return if support to store ir results into SqlContext. 

#### function set_compile_only

```cpp
inline void set_compile_only(
    bool flag
)
```


Set if only support to compile SQL.

If set `true`, the engine won't generate runner plan as well. 

#### function is_compile_only

```cpp
inline bool is_compile_only() const
```

Return if only support to compile physical plan. 

#### function set_plan_only

```cpp
inline void set_plan_only(
    bool flag
)
```


Set if the engine only generate physical plan.

If set `true`, the engine won't build llvm jit. 

#### function is_plan_only

```cpp
inline bool is_plan_only() const
```


#### function max_sql_cache_size

```cpp
inline uint32_t max_sql_cache_size() const
```

Return the maximum number of entries we can hold for compiling cache. 

#### function set_max_sql_cache_size

```cpp
inline void set_max_sql_cache_size(
    uint32_t size
)
```

Set the maxinum number of cache entries. 

#### function set_performance_sensitive

```cpp
inline void set_performance_sensitive(
    bool flag
)
```


Set if the engine is performance sensitive.

Normally, the engine can support more abilities under performance un-sensitive mode. 

#### function is_performance_sensitive

```cpp
inline bool is_performance_sensitive() const
```

Return if the engine is performance sensitive. 

#### function set_cluster_optimized

```cpp
inline EngineOptions * set_cluster_optimized(
    bool flag
)
```

Set if the engine support cluster optimization. 

#### function is_cluster_optimzied

```cpp
inline bool is_cluster_optimzied() const
```

Return if the engine support cluster optimization. 

#### function set_batch_request_optimized

```cpp
inline EngineOptions * set_batch_request_optimized(
    bool flag
)
```

Set if the engine supoort batch request optimization. 

#### function is_batch_request_optimized

```cpp
inline bool is_batch_request_optimized() const
```

Return if the engine support batch request optimization. 

#### function set_enable_expr_optimize

```cpp
inline EngineOptions * set_enable_expr_optimize(
    bool flag
)
```

Set if the engine can support expression optimization. 

#### function is_enable_expr_optimize

```cpp
inline bool is_enable_expr_optimize() const
```

Return if the engine support expression optimization. 

#### function set_enable_batch_window_parallelization

```cpp
inline EngineOptions * set_enable_batch_window_parallelization(
    bool flag
)
```

Set if the engine can support batch window parallelization. 

#### function is_enable_batch_window_parallelization

```cpp
inline bool is_enable_batch_window_parallelization() const
```

Return if the engine support batch window parallelization. 

#### function set_enable_spark_unsaferow_format

```cpp
inline EngineOptions * set_enable_spark_unsaferow_format(
    bool flag
)
```

Set if the engine can support spark unsafe row format. 

#### function is_enable_spark_unsaferow_format

```cpp
inline bool is_enable_spark_unsaferow_format() const
```

Return if the engine can support can support spark unsafe row format. 

#### function jit_options

```cpp
inline hybridse::vm::JitOptions & jit_options()
```

Return [JitOptions](). 

-------------------------------

Updated on  6 April 2021 at 19:38:01 PDT