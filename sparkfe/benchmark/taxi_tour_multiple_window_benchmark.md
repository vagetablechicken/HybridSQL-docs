# TaxiTour多窗口测试

## 介绍

这个测试场景使用公开的TaxiTour数据，数据已经预处理成Parquet文件格式，测试脚本地址为 https://github.com/4paradigm/SparkFE/tree/main/benchmark/taxi_tour_multiple_window 。

## 测试SQL

测试的SQL脚本包含两个Window，窗口大小默认为10000，如果窗口越大那么整体运行时间变长，但SparkFE的性能提升越明显。

```
select 
    trip_duration,
    passenger_count,
    sum(pickup_latitude) over w as vendor_sum_pl,
    max(pickup_latitude) over w as vendor_max_pl,
    min(pickup_latitude) over w as vendor_min_pl,
    avg(pickup_latitude) over w as vendor_avg_pl,
    sum(pickup_latitude) over w2 as pc_sum_pl,
    max(pickup_latitude) over w2 as pc_max_pl,
    min(pickup_latitude) over w2 as pc_min_pl,
    avg(pickup_latitude) over w2 as pc_avg_pl,
    sum(dropoff_latitude) over w as vendor_sum_pl2,
    max(dropoff_latitude) over w as vendor_max_pl2,
    min(dropoff_latitude) over w as vendor_min_pl2,
    avg(dropoff_latitude) over w as vendor_avg_pl2,
    sum(dropoff_latitude) over w2 as pc_sum_pl2,
    max(dropoff_latitude) over w2 as pc_max_pl2,
    min(dropoff_latitude) over w2 as pc_min_pl2,
    avg(dropoff_latitude) over w2 as pc_avg_pl2,
    sum(trip_duration) over w as vendor_sum_pl3,
    max(trip_duration) over w as vendor_max_pl3,
    min(trip_duration) over w as vendor_min_pl3,
    avg(trip_duration) over w as vendor_avg_pl3,
    sum(trip_duration) over w2 as pc_sum_pl3,
    max(trip_duration) over w2 as pc_max_pl3,
    min(trip_duration) over w2 as pc_min_pl3,
    avg(trip_duration) over w2 as pc_avg_pl3
from t1
window w as (partition by vendor_id order by pickup_datetime ROWS BETWEEN 10000 PRECEDING AND CURRENT ROW),
       w2 as (partition by passenger_count order by pickup_datetime ROWS BETWEEN 10000 PRECEDING AND CURRENT ROW)
```

## 测试脚本

测试使用简单PySpark即可运行，也可以使用Scala等语言实现，小数据量下本地可运行，示例程序如下。

```
from pyspark.sql import SparkSession
import os

def main():
    spark = SparkSession.builder.appName("app").getOrCreate()

    current_path = os.getcwd()
    parquet_file_path = "file://{}/taxi_tour_parquet/".format(current_path)

    train = spark.read.parquet(parquet_file_path)
    train.createOrReplaceTempView("t1")

    with open("multiple_window.sql", "r") as f:
        sparksqlText = f.read()
        spark_df = spark.sql(sparksqlText)

        output_path = "file:///tmp/spark_output/"
        spark_df.write.mode('overwrite').parquet(output_path)

    spark.stop()

if __name__ == "__main__":
    main()
```

```
$SPARK_HOME/bin/spark-submit \
     --master local[*] \
     ./multiple_window.py
```
