---
title: com._4paradigm.hybridse.sdk.RequestEngine
summary: SQL Engine in request mode. 

---
# com._4paradigm.hybridse.sdk.RequestEngine



SQL Engine in request mode. 
## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[RequestEngine](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_request_engine.md#function-requestengine)**(String sql, TypeOuterClass.Database database)| <br>Construct [RequestEngine](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_request_engine.md) with given sql and database.  |
|**[getPlan](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_request_engine.md#function-getplan)**()| PhysicalOpNode <br>Get physical plan.  |
|**[close](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_request_engine.md#function-close)**()| synchronized void <br>Close the request engine.  |

## Public Functions

#### function RequestEngine

```cpp
inline RequestEngine(
    String sql,
    TypeOuterClass.Database database
)
```

Construct [RequestEngine](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_request_engine.md) with given sql and database. 

**Parameters**: 

  * **sql** 
  * **database** 


**Exceptions**: 

  * **[UnsupportedHybridSeException](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_unsupported_hybrid_se_exception.md)** 


#### function getPlan

```cpp
inline PhysicalOpNode getPlan()
```

Get physical plan. 

#### function close

```cpp
inline synchronized void close()
```

Close the request engine. 

**Exceptions**: 

  * **Exception** 


