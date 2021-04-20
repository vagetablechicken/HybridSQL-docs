---
title: com._4paradigm.hybridse.utils.SkewUtils

---
# com._4paradigm.hybridse.utils.SkewUtils



## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[genPercentileSql](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1utils_1_1_skew_utils.md#function-genpercentilesql)**(String table1, int quantile, List< String > keys, String ts, String cnt)| String  |
|**[genPercentileTagSql](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1utils_1_1_skew_utils.md#function-genpercentiletagsql)**(String table1, String table2, int quantile, List< String > schemas, Map< String, String > keysMap, String ts, String tag1, String tag2, String tag3, long tag4)| String  |
|**[caseWhenTag](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1utils_1_1_skew_utils.md#function-casewhentag)**(String table1, String table2, String ts, int quantile, String output, String con1, long cnt)| String <br>?shu @paraable1  |
|**[explodeDataSql](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1utils_1_1_skew_utils.md#function-explodedatasql)**(String table, int quantile, List< String > schemas, String tag1, String tag2, long watershed, long windowSize)| String  |

## Public Functions

#### function genPercentileSql

```cpp
static inline String genPercentileSql(
    String table1,
    int quantile,
    List< String > keys,
    String ts,
    String cnt
)
```


#### function genPercentileTagSql

```cpp
static inline String genPercentileTagSql(
    String table1,
    String table2,
    int quantile,
    List< String > schemas,
    Map< String, String > keysMap,
    String ts,
    String tag1,
    String tag2,
    String tag3,
    long tag4
)
```


**Parameters**: 

  * **table1** 
  * **table2** 
  * **quantile** 
  * **schemas** 
  * **keysMap** 
  * **ts** 
  * **tag1** skewTag 标签位 
  * **tag2** skewPosition 
  * **tag3** skewCntName 
  * **tag4** skewCnt = 100 


**Return**: 

#### function caseWhenTag

```cpp
static inline String caseWhenTag(
    String table1,
    String table2,
    String ts,
    int quantile,
    String output,
    String con1,
    long cnt
)
```

?shu @paraable1 

**Parameters**: 

  * **ts** 
  * **quantile** 
  * **output** 


**Return**: 

#### function explodeDataSql

```cpp
static inline String explodeDataSql(
    String table,
    int quantile,
    List< String > schemas,
    String tag1,
    String tag2,
    long watershed,
    long windowSize
)
```


