---
title: com._4paradigm.hybridse.sdk.SQLEngine
summary: Implementation of HybridSE SQL simple engine that compiled queries with given sql and database. 

---
# com._4paradigm.hybridse.sdk.SQLEngine



Implementation of HybridSE SQL simple engine that compiled queries with given sql and database. 
## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[SQLEngine](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_s_q_l_engine.md#function-sqlengine)**(String sql, TypeOuterClass.Database database)| <br>Construct SQL engine for specific sql and database.  |
|**[SQLEngine](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_s_q_l_engine.md#function-sqlengine)**(String sql, TypeOuterClass.Database database, EngineOptions engineOptions)| <br>Construct SQL engine for specific sql, database and EngineOptions.  |
|**[initilize](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_s_q_l_engine.md#function-initilize)**(String sql, TypeOuterClass.Database database, EngineOptions engineOptions)| void  |
|**[getPlan](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_s_q_l_engine.md#function-getplan)**()| PhysicalOpNode <br>Return physical plan.  |
|**[getIRBuffer](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_s_q_l_engine.md#function-getirbuffer)**()| ByteBuffer <br>Return compile IR result as ByteBuffer.  |
|**[close](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_s_q_l_engine.md#function-close)**()| synchronized void  |
|**[createDefaultEngineOptions](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_s_q_l_engine.md#function-createdefaultengineoptions)**()| EngineOptions <br>Create default engine option.  |

## Public Functions

#### function SQLEngine

```cpp
inline SQLEngine(
    String sql,
    TypeOuterClass.Database database
)
```

Construct SQL engine for specific sql and database. 

**Exceptions**: 

  * **[UnsupportedHybridSeException](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_unsupported_hybrid_se_exception.md)** throws exception when fail to compile queries 


#### function SQLEngine

```cpp
inline SQLEngine(
    String sql,
    TypeOuterClass.Database database,
    EngineOptions engineOptions
)
```

Construct SQL engine for specific sql, database and EngineOptions. 

**Exceptions**: 

  * **[UnsupportedHybridSeException](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_unsupported_hybrid_se_exception.md)** throws exception when fail to compile queries 


#### function initilize

```cpp
inline void initilize(
    String sql,
    TypeOuterClass.Database database,
    EngineOptions engineOptions
)
```


#### function getPlan

```cpp
inline PhysicalOpNode getPlan()
```

Return physical plan. 

#### function getIRBuffer

```cpp
inline ByteBuffer getIRBuffer()
```

Return compile IR result as ByteBuffer. 

**Return**: 

#### function close

```cpp
inline synchronized void close()
```


#### function createDefaultEngineOptions

```cpp
static inline EngineOptions createDefaultEngineOptions()
```

Create default engine option. 



* Enable store ir results into SQL context
* Only compile SQL
* Disable performance sensitive mode. 

