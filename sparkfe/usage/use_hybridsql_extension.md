# 使用HybridSQL拓展

## 简介

HybridSQL是针对AI等场景优化的SQL语法，SparkFE支持HybridSQL并且可以在拼表、滑动窗口计算等SQL功能上比SparkSQL有巨大的性能提升。

更多HybridSQL语法细节可参考[HybridSE SQL语法手册](../../hybridse/language_guide/)。

## 特殊拼表LastJoin

SparkFE支持LastJoin，用法与其他Join类型类似。

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

## 特殊窗口定义RowsRange

SparkFE支持RowsRange的窗口边界定义，用法与其他窗口边界类型类似。

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
