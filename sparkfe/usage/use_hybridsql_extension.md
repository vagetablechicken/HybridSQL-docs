# Use HybridSQL Extensions

## Introduction

HybridSQL has SQL syntax extensions for AI scenarios. SparkFE supports HybridSQL and has significant performance improvement in joining tables, sliding window computing and other SQL functionalities.

For more detail of HybridSQL syntax, please refer to[HybridSE Language Guide](../../hybridse/language_guide/)。

## LastJoin: Custom Join Type

SparkFE supports LastJoin which is similar with other join type.

```
val spark = SparkSession
    .builder
    .appName("SparkFEApp")
    .getOrCreate()
val sc = spark.sparkContext

val data = Seq(
    Row("A", 10l, 112233, "06-03-2009"),
    Row("B", 20l, 223311, "06-03-2009"),
    Row("C", 30l, 331122, "06-03-2009"))

val schema = StructType(List(
    StructField("name", StringType),
    StructField("age", LongType),
    StructField("phone", IntegerType),
    StructField("mydate", StringType)))

val df = spark.createDataFrame(sc.makeRDD(data), schema)

df.createOrReplaceTempView("t1")
df.createOrReplaceTempView("t2")

val sqlText = "SELECT t1.name, t2.age FROM t1 LAST JOIN t2 ON t1.age == t2.age"

val outputDf = spark.sql(sqlText)    
```

## RowsRange: Custom Window Frame

SparkFE support RowsRange as window frame bound which is like others.

```
val spark = SparkSession
    .builder
    .appName("SparkFEApp")
    .getOrCreate()
val sc = spark.sparkContext

val data = Seq(
    Row("A", 10l, 112233, "06-03-2009"),
    Row("B", 20l, 223311, "06-03-2009"),
    Row("C", 30l, 331122, "06-03-2009"))

val schema = StructType(List(
    StructField("name", StringType),
    StructField("age", LongType),
    StructField("phone", IntegerType),
    StructField("mydate", StringType)))

val df = spark.createDataFrame(sc.makeRDD(data), schema)

df.createOrReplaceTempView("t1")

val sqlText = "SELECT min(age) OVER w1 as w1_min_age FROM t1 WINDOW w1 as (PARTITION BY name ORDER by age ROWS_RANGE BETWEEN 10s PRECEDING AND CURRENT ROW)"

val outputDf = sess.sql(sqlText)    
```
