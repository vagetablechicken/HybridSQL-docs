# FAQ

## How to deploy SparkFE?

SparkFE is like Spark which is a programming library for distributed computing applications. It does not require deploying in advance and you can run in local container, Yarn, or Kuberentes cluster. During the development phase, local server or container may need your requirements and Yarn is needed for computing big data scenarios.


## Will SparkFE be synchronous with Spark upstream?

Yes and it will support Spark 3.0 and the later versions. SparkFE distribution is based on Spark source code and the number of modificaiton line is less than one hundred. All the functionalities except SparkSQL of SparkFE are the same as standard Spark.

## Does SparkFE require hardware for improvement?

目前SparkFE生成的平台相关二进制码都是基于平台CPU优化的，