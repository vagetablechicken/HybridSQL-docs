# SparkFE Distribution

## Introduction

SparkFE distribution is the LLVM-based and high-performance native Spark distribution. It provides Scala, Java, Python and R programming interfaces jsut like standard Spark and the usage is all the same.

## Download SparkFE Distribution

The Github [Releases Page](https://github.com/4paradigm/SparkFE/releases) provides the donwload link for SparkFE distribution and users can download directly.

Notice that the pre-built SparkFE disbution is the all-in-one version which means it supports Linux and MacOS. If you have any other requirements, you can download the source code and re-compile for your need.


## Use Example Jars

After downloading and decompression, you can setup `SPARK_HOME` environment variable and execute the demo in Example Jars.

```
export SPARK_HOME=`pwd`/spark-3.0.0-bin-sparkfe/

$SPARK_HOME/bin/spark-submit \
  --master local \
  --class org.apache.spark.examples.sql.SparkSQLExample \
  $SPARK_HOME/examples/jars/spark-examples*.jar
```

Notice that SparkSQLExample is the built-in demo in standard Spark source code. Part of these examples can be accelerated by SparkFE but some of the DataFrame examples can not.

## Use PySpark

After downloading SparkFE distribution, you can use the standard PySpark to implement your applications. Here is the example code.

```
from pyspark.sql import SparkSession
from pyspark.sql import Row
from pyspark.sql.types import *
 
spark = SparkSession.builder.appName("demo").getOrCreate()
print(spark.version)

schema = StructType([
    StructField("name", StringType(), nullable=True),
    StructField("age", IntegerType(), nullable=True),
])

rows = [
    Row("Andy", 20),
    Row("Berta", 30),
    Row("Joe", 40)
]

spark.createDataFrame(spark.sparkContext.parallelize(rows), schema).createOrReplaceTempView("t1")
spark.sql("SELECT name, age + 1 FROM t1").show()

```

Just save above code as file `sparkfe_demo.py` then submit the job with the following command.

```
${SPARK_HOME}/bin/spark-submit \
    --master=local \
    ./sparkfe_demo.py
```

Observe the log of Spark jobs and it will display the optimized SQL logical plans and do JIT compiling for different computing architecture.

```
PROJECT(type=TableProject)
    DATA_PROVIDER(table=t1)
```
