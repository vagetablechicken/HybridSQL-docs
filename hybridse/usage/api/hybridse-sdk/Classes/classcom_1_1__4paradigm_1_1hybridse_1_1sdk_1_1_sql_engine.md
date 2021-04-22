---
title: com._4paradigm.hybridse.sdk.SqlEngine
summary: Implementation of HybridSE SQL simple engine that compiled queries with given sql and database. 

---
# com._4paradigm.hybridse.sdk.SqlEngine



Implementation of HybridSE SQL simple engine that compiled queries with given sql and database. 
## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[SqlEngine](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_sql_engine.md#function-sqlengine)**(String sql, TypeOuterClass.Database database)| <br>Construct SQL engine for specific sql and database.  |
|**[SqlEngine](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_sql_engine.md#function-sqlengine)**(String sql, TypeOuterClass.Database database, EngineOptions engineOptions)| <br>Construct SQL engine for specific sql, database and EngineOptions.  |
|**[initilize](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_sql_engine.md#function-initilize)**(String sql, TypeOuterClass.Database database, EngineOptions engineOptions)| void <br>Initialize engine with given sql, database and specified engine options.  |
|**[getPlan](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_sql_engine.md#function-getplan)**()| PhysicalOpNode <br>Return physical plan.  |
|**[getIrBuffer](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_sql_engine.md#function-getirbuffer)**()| ByteBuffer <br>Return compile IR result as ByteBuffer.  |
|**[close](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_sql_engine.md#function-close)**()| synchronized void  |
|**[createDefaultEngineOptions](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_sql_engine.md#function-createdefaultengineoptions)**()| EngineOptions <br>Create default engine option.  |

## Public Functions

#### function SqlEngine

```cpp
inline SqlEngine(
    String sql,
    TypeOuterClass.Database database
)
```

Construct SQL engine for specific sql and database. 

**Exceptions**: 

  * **[UnsupportedHybridSeException](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_unsupported_hybrid_se_exception.md)** throws exception when fail to compile queries 


#### function SqlEngine

```cpp
inline SqlEngine(
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

Initialize engine with given sql, database and specified engine options. 

**Parameters**: 

  * **sql** query sql string 
  * **database** query on the database 
  * **engineOptions** query engine options 


**Exceptions**: 

  * **[UnsupportedHybridSeException](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_unsupported_hybrid_se_exception.md)** throw when query unsupported or has syntax error 


#### function getPlan

```cpp
inline PhysicalOpNode getPlan()
```

Return physical plan. 

#### function getIrBuffer

```cpp
inline ByteBuffer getIrBuffer()
```

Return compile IR result as ByteBuffer. 

#### function close

```cpp
inline synchronized void close()
```


#### function createDefaultEngineOptions

```cpp
static inline EngineOptions createDefaultEngineOptions()
```

Create default engine option. 

**Return**: Return default engine option 

- Enable store ir results into SQL context

* Only compile SQL
* Disable performance sensitive mode.

