---
title: com._4paradigm.hybridse.sdk.JitManager
summary: JIT manager provides a set of API to access jit, configure JitOptions and init llvm module. 

---
# com._4paradigm.hybridse.sdk.JitManager



JIT manager provides a set of API to access jit, configure JitOptions and init llvm module. 
## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[getJit](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_jit_manager.md#function-getjit)**(String tag)| synchronized HybridSeJitWrapper <br>Return JIT specified by tag.  |
|**[initJitModule](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_jit_manager.md#function-initjitmodule)**(String tag, ByteBuffer moduleBuffer)| synchronized void <br>Init llvm module specified by tag.  |
|**[removeModule](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_jit_manager.md#function-removemodule)**(String tag)| synchronized void <br>Remove native module specified by tag.  |
|**[clear](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_jit_manager.md#function-clear)**()| synchronized void <br>Clear native modules and jits.  |

## Public Functions

#### function getJit

```cpp
static inline synchronized HybridSeJitWrapper getJit(
    String tag
)
```

Return JIT specified by tag. 

#### function initJitModule

```cpp
static inline synchronized void initJitModule(
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

  * **tag** module tag 


#### function clear

```cpp
static inline synchronized void clear()
```

Clear native modules and jits. 

