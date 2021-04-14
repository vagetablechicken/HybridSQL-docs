# Multiple Window Concurrently Computing

## Introduction

It is common to compute with multiple windows when using Spark for feature extraction. The standard Spark only support compute windows serially which has limitation to utilize the cluster resources.

We will introduce the improvement from SparkFE with the following SQL example.

```
SELECT 
  min(age) OVER w1 as w1_min_age, 
  min(age) OVER w2 as w2_min_age 
FROM t1 
WINDOW 
  w1 as (PARTITION BY name ORDER by age ROWS BETWEEN 10 PRECEDING AND CURRENT ROW), 
  w2 as (PARTITION BY age ORDER by age ROWS BETWEEN 10 PRECEDING AND CURRENT ROW)"
```

## Spark Implementation For Multiple Windows

According to the above SQL application, standard Spark will generate the logical plan and physical plan like this.

![](../images/spark_multiple_window_logical_plan.png)

The windows are computed serially and the next window computation will start after the former one has been finished. Since the window computation requires repartition, if the partitions have skew data then the whole task need to wait for the slowest partition to compute which is the the waste of the cluster resources.


## SparkFE Implementation For Multiple Windows

Refer to [SparkFE Configuration](../usage/sparkfe_configuration.md), SparkFE has the configuration to enable optimization of multiple window concurrently computing.

| Configuration | Introduction | Default | Note |
| ------------- | ------------ | ------- | ---- |
| sparkfe.window.parallelization | Enable multiple window computing concurrently or not | false | It improves cluster usage but adds extra compute nodes |

After enabling the configuration, SparkFE will generate the logical plan for the above SQL application.

![](../images/sparkfe_multiple_window_concurrent_logical_plan.png)

Optimization of multiple window concurrently computing requires to implement the ConcatJoin which will merge features from multiple windows. It can use the [Native LastJoin Optimization](./native_last_join_optimization.md) for better performance. Compare with the serial implementation, even though it requires more data processing, this optimization can get significant performance improvement in most use cases especially for scenarios with data skew or sufficient computing resouces.
