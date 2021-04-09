# More Usage For SparkFE

## Introduction

SparkFE distribution is compatible with standard Spark so the usage is the same as the standard one. Users do not need to modify the source in Scala, Java, Python or R programming languages. And the jobs can be submitted to Local, Standalone, Mesos, Yarn or Kubernetes as well.

Notice that currently SparkFE only optimize the SparkSQL interface and using other APIs will not be accerlated.

## Supported Programming Languages

### Use Scala

Refer to file `SparkSQLExample.scala` in Spark source code.

```
// $example on:create_df$
val df = spark.read.json("examples/src/main/resources/people.json")

// Register the DataFrame as a SQL temporary view
df.createOrReplaceTempView("people")

val sqlDF = spark.sql("SELECT * FROM people")
sqlDF.show()
```

### Use Java

Refer to file `JavaSparkSQLExample.java` in Spark source code.

```
// $example on:create_df$
Dataset<Row> df = spark.read().json("examples/src/main/resources/people.json");

// Register the DataFrame as a SQL temporary view
df.createOrReplaceTempView("people");

Dataset<Row> sqlDF = spark.sql("SELECT * FROM people");
sqlDF.show();
```

### Use Python

Refer to file `sql_network_wordcount.py` in Spark souce code.

```
# Creates a temporary view using the DataFrame
wordsDataFrame.createOrReplaceTempView("words")

# Do word count on table using SQL and print it
wordCountsDataFrame = spark.sql("select word, count(*) as total from words group by word")
wordCountsDataFrame.show()
```

### Use R

Refe rto the example code in official [SparkR documentation](https://spark.apache.org/docs/latest/sparkr.html).

```
# Load a JSON file
people <- read.df("./examples/src/main/resources/people.json", "json")

# Register this SparkDataFrame as a temporary view.
createOrReplaceTempView(people, "people")

# SQL statements can be run by using the sql method
teenagers <- sql("SELECT name FROM people WHERE age >= 13 AND age <= 19")
head(teenagers)
```

## Supported Clusters

### Use Local Mode

It is easy to deploy to local by using `local` configuration.

```
${SPARK_HOME}/bin/spark-submit \
    --master=local \
    ./sparkfe_demo.py
```

### Use Standalone Mode

Refer to official documentation of [Spark Standalone Mode](https://spark.apache.org/docs/latest/spark-standalone.html).

```
val conf = new SparkConf()
  .setMaster("spark://IP:PORT")
  .setAppName("My app")
  .set("spark.cores.max", "10")
val sc = new SparkContext(conf)
```

### Use Mesos Cluster

Refer to official documentation of [Running Spark on Mesos](https://spark.apache.org/docs/latest/running-on-mesos.html).

```
val conf = new SparkConf()
  .setMaster("mesos://HOST:5050")
  .setAppName("My app")
  .set("spark.executor.uri", "<path to spark.tar.gz uploaded above>")
val sc = new SparkContext(conf)
```

### Use Yarn Cluster

Refer to official documentation of [Running Spark on YARN](https://spark.apache.org/docs/latest/running-on-yarn.html).

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

### Use Kubernetes Cluster

Refer to official documentation of [Running Spark on Kubernetes](https://spark.apache.org/docs/latest/running-on-kubernetes.html).

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
