---
title: com._4paradigm.hybridse.sdk.HybridSeException
summary: The general exception class throw when something goes wrong during compiling SQL queries. 

---
# com._4paradigm.hybridse.sdk.HybridSeException



The general exception class throw when something goes wrong during compiling SQL queries. 
## Summary

```cpp
class com._4paradigm.hybridse.sdk.HybridSeException;
```
The general exception class throw when something goes wrong during compiling SQL queries. 

This includes, but is not limited to, SQL syntax error, Non-support Plan and so on. 


|  Public functions|            |
| -------------- | -------------- |
|**[HybridSeException](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_hybrid_se_exception.md#function-hybridseexception)**(String message)|  |
|**[HybridSeException](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_hybrid_se_exception.md#function-hybridseexception)**(String message, Throwable cause)|  |
|**[getCause](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_hybrid_se_exception.md#function-getcause)**()| synchronized Throwable  |
|**[getMessage](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_hybrid_se_exception.md#function-getmessage)**()| String  |

## Public Functions

#### function HybridSeException

```cpp
inline HybridSeException(
    String message
)
```


#### function HybridSeException

```cpp
inline HybridSeException(
    String message,
    Throwable cause
)
```


#### function getCause

```cpp
inline synchronized Throwable getCause()
```


#### function getMessage

```cpp
inline String getMessage()
```


