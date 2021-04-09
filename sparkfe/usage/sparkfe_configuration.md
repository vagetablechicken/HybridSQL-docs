# SparkFE配置

## 简介

SparkFE兼容标准的[Spark配置](https://spark.apache.org/docs/latest/configuration.html)，除此之外，还支持新增的配置项，可以更好地利用原生执行引擎的性能优化。

## 新增配置

| 配置项 | 说明 | 默认值 | 备注 |
| ----- | --- | ----- | ---- |
| sparkfe.window.parallelization | 是否启动窗口并行计算优化 | false | 窗口并行计算可提高集群利用率但增加计算节点 |
| sparkfe.addIndexColumn.method | 添加索引列方法 | monotonicallyIncreasingId | 可选方法为zipWithUniqueId, zipWithIndex, monotonicallyIncreasingId |
| sparkfe.concatjoin.jointype | 拼接拼表方法 | inner | 可选方法为inner, left, last |
| sparkfe.enable.native.last.join | 是否开启NativeLastJoin优化 | true | 相比基于LeftJoin实现性能更高 |
| sparkfe.enable.unsaferow.optimization | 是否开启UnsafeRow内存优化 | false | 开启后降低编解码开销，目前部分复杂类型不支持 |
| sparkfe.physical.plan.graphviz.path | 导出物理计划图片路径 | "" | 默认不导出图片文件 |
