## Introduction

SparkFE is the LLVM-based and high-performance Spark native execution engine which is designed for AI Feature Enginnering.

![Architecture](../images/sparkfe_architecture.png)

## Background

Why SparkFE?

* Optimizing performance for Spark has been reach the bottleneck. Using C++ and LLVM to implement the native execution engine can leverage the modern CPU and GPU to achieve several times performance improvement.
* Spark focus on general-purpose offline computing but be short of feature engineering for machine learning and generating online features. SparkFE can make up for the above defects and make AI landing easier.
* Comparing with other native execution engine, like Intel OAP and Nvidia spark-rapids, SparkFE rewrite SQL optimization passes and use LLVM for JIT which is much more efficient and flexible.

Who is SparkFE for?

* Spark users. SparkFE is compatible with most of SparkSQL syntax. Spark users can use SparkFE for acceleration without any code changed.
* Spark developer. If you are familiar with Spark source code or LLVM JIT, you can contribute to SparkFE for better performance and functionality.
* Users who use Spark for ML/AI. SparkFE provides AI-oriented syntax extensions and high-performance feature engineering which can solve online-offline consistency problem for AI landing.

Why SparkFE is fast?

* SparkFE is written in C++ and based on LLVM. It will optimize and generate native binary code for each hardware architecture. It rewrites the underlying SQL compiler and expression optimization passes. There are some physical plans have no CodeGen supported in Spark however SparkFE has implemented in efficient way. SparkFE has creatively implemented the features of multiple window concurrently computing and skew computing optimization for window data. It also has better memory management which avoid the overhead of JVM garbage collection.


What are the features of SparkFE?

* **High Performance**

    Based on LLVM optimization, we can get more than six times performance improvement in some AI scenarios. It reduces the computing time for the same applications and get lower TCO.
    
* **No Migration Cost**

    Using SparkFE does not require modifying or re-compiling your SparkSQL applications. Just set the SPARK_HOME then you will reap the performance benefit of native execution engine.
    
* **Optimized For Machine Learning**

    SparkFE provided the customized join type and UDF/UDAF for machine learning scenarios which can meet the requirements for feature engineering in production environment.

* **Online-Offline consistency**

    Using [FEDB](https://github.com/4paradigm/fedb) and SparkFE, the machine learning applications with SQL for feature engineering can be deployed without any development. The native execution engine guarantees the online-offline consistency and greatly reduces the cost of AI landing. 

* **Upstream First** 
  
    SparkFE will be compatible with Spark 3.0 and the later versions. All the functions will be synchronized with upstream and it is able to fallback to vanilla Spark in some special scenarios.
