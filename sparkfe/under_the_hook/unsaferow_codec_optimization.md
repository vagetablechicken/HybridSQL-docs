# UnsafeRow编码优化

## 介绍

Spark UnsafeRow是Catalyst和Tungsten模块引入的内存优化方案，基于JVM提供的Unsafe接口实现，可以减少JVM对象并降低GC带来的性能影响。

## UnsafeRow内存格式

Spark UnsafeRow定义了单行的数据内存分布格式，整行的数据都在一段连续内存中，具体的格式如下。

* 64bit（8byte）对齐，内存空间不紧凑但有利于提高访存性能
* 小端存储，这样低位类型存到高位内存（如存int到64位）不需要额外编码
* 所有列不管什么类型都按64bit存储，变长内容顺延存储

![](../images/spark_unsaferow_memory_layout.jpeg)

## SparkFE编码兼容

Spark内部所有行数据存储默认都使用UnsafeRow格式，SparkFE提供了以下两种方式支持Spark都行编码。

* 编解码模式，对行的每一列进行重新的编解码，总内存占用更小，但存在编解码开销。
* UnsafeRow兼容模式，内部行格式兼容UnsafeRow内存布局，没有编解码开销。

参考[SparkFE配置](../usage/sparkfe_configuration.md)文档，可以通过以下配置来开启UnsafeRow优化。


| 配置项 | 说明 | 默认值 | 备注 |
| ----- | --- | ----- | ---- |
| sparkfe.enable.unsaferow.optimization | 是否开启UnsafeRow内存优化 | false | 开启后降低编解码开销，目前部分复杂类型不支持 |
