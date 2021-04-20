---
title: com._4paradigm.hybridse.sdk.JitManager
summary: JIT manager provides a set of API to access jit, configure JitOptions and init llvm module. 

---
# com._4paradigm.hybridse.sdk.JitManager



JIT manager provides a set of API to access jit, configure JitOptions and init llvm module. 
## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[getJIT](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_jit_manager.md#function-getjit)**(String tag)| synchronized HybridSeJitWrapper <br>Return JIT specified by tag.  |
|**[initJITModule](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_jit_manager.md#function-initjitmodule)**(String tag, ByteBuffer moduleBuffer)| synchronized void <br>Init llvm module specified by tag.  |
|**[removeModule](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_jit_manager.md#function-removemodule)**(String tag)| synchronized void <br>Remove native module specified by tag.  |
|**[clear](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_jit_manager.md#function-clear)**()| synchronized void <br>Clear native modules and jits.  |

## Public Functions

#### function getJIT

```cpp
static inline synchronized HybridSeJitWrapper getJIT(
    String tag
)
```

Return JIT specified by tag. 

#### function initJITModule

```cpp
static inline synchronized void initJITModule(
    String tag,
    ByteBuffer moduleBuffer
)
```

Init llvm module specified by tag. 

**Parameters**: 

  * **tag** tag specified a jit 
  * **moduleBuffer** ByteBuffer used to initialize native module 


Init native module with module byte buffer. 

#### function removeModule

```cpp
static inline synchronized void removeModule(
    String tag
)
```

Remove native module specified by tag. 

**Parameters**: 

  * **tag** 


#### function clear

```cpp
static inline synchronized void clear()
```

Clear native modules and jits. 

