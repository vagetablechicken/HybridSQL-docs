# SparkFE更多用法

## 简介

SparkFE是Spark兼容的发行版，因此SparkFE的用法与标准Spark一致，用户使用Scala、Java、Python和R编写的程序不需要修改源码，就可以在Local、Standalone、Mesos、Yarn和Kubernetes集群上运行。

注意，目前SparkFE只优化SparkSQL接口，使用其他API的应用暂不会被加速。

## 使用多种编程语言

### 使用Scala

参考Spark源码中的`SparkSQLExample.scala`文件。

```
// $example on:create_df$
val df = spark.read.json("examples/src/main/resources/people.json")

// Register the DataFrame as a SQL temporary view
df.createOrReplaceTempView("people")

val sqlDF = spark.sql("SELECT * FROM people")
sqlDF.show()
```

### 使用Java

参考Spark源码中的`JavaSparkSQLExample.java`文件。

```
// $example on:create_df$
Dataset<Row> df = spark.read().json("examples/src/main/resources/people.json");

// Register the DataFrame as a SQL temporary view
df.createOrReplaceTempView("people");

Dataset<Row> sqlDF = spark.sql("SELECT * FROM people");
sqlDF.show();
```

### 使用Python

参考Spark源码中的`sql_network_wordcount.py`文件。

```
# Creates a temporary view using the DataFrame
wordsDataFrame.createOrReplaceTempView("words")

# Do word count on table using SQL and print it
wordCountsDataFrame = spark.sql("select word, count(*) as total from words group by word")
wordCountsDataFrame.show()
```

### 使用R语言

参考[SparkR官方文档](https://spark.apache.org/docs/latest/sparkr.html)的代码示例。

```
# Load a JSON file
people <- read.df("./examples/src/main/resources/people.json", "json")

# Register this SparkDataFrame as a temporary view.
createOrReplaceTempView(people, "people")

# SQL statements can be run by using the sql method
teenagers <- sql("SELECT name FROM people WHERE age >= 13 AND age <= 19")
head(teenagers)
```

## 提交Spark任务

### 使用Local模式

提交任务到本地运行非常简单，使用`local`配置即可。

```
${SPARK_HOME}/bin/spark-submit \
    --master=local \
    ./sparkfe_demo.py
```

### 使用Standalone模式

提交任务到Standalone集群可以参考[Spark Standalone Mode](https://spark.apache.org/docs/latest/spark-standalone.html)官方文档。

```
val conf = new SparkConf()
  .setMaster("spark://IP:PORT")
  .setAppName("My app")
  .set("spark.cores.max", "10")
val sc = new SparkContext(conf)
```

### 使用Mesos集群

提交任务到Mesos集群可以参考[Running Spark on Mesos](https://spark.apache.org/docs/latest/running-on-mesos.html)官方文档。

```
val conf = new SparkConf()
  .setMaster("mesos://HOST:5050")
  .setAppName("My app")
  .set("spark.executor.uri", "<path to spark.tar.gz uploaded above>")
val sc = new SparkContext(conf)
```

### 使用Yarn集群

提交任务到Yarn集群可以参考[Running Spark on YARN](https://spark.apache.org/docs/latest/running-on-yarn.html)官方文档。

```
${SPARK_HOME}/bin/spark-submit --class org.apache.spark.examples.SparkPi \
    --master yarn \
    --deploy-mode cluster \
    --driver-memory 4g \
    --executor-memory 2g \
    --executor-cores 1 \
    --queue thequeue \
    examples/jars/spark-examples*.jar \
    10
```

### 使用Kubernetes集群

提交任务到Kubernetes集群可以参考[Running Spark on Kubernetes](https://spark.apache.org/docs/latest/running-on-kubernetes.html)官方文档。

```
${SPARK_HOME}/bin/spark-submit \
    --master k8s://https://<k8s-apiserver-host>:<k8s-apiserver-port> \
    --deploy-mode cluster \
    --name spark-pi \
    --class org.apache.spark.examples.SparkPi \
    --conf spark.executor.instances=5 \
    --conf spark.kubernetes.container.image=<spark-image> \
    local:///path/to/examples.jar
```
