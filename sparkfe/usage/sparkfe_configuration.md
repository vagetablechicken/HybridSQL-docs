# SparkFE Configuration

## Introduction

SparkFE is compatible with standard [Spark configurations](https://spark.apache.org/docs/latest/configuration.html). In addition, it supports new configurations which may improve performance for the native execution engine.

## Extra Configuration

| Configuration | Introduction | Default | Note |
| ------------- | ------------ | ------- | ---- |
| sparkfe.window.parallelization | Enable multiple window computing concurrently or not | false | It improves cluster usage but adds extra compute nodes |
| sparkfe.addIndexColumn.method | The method of adding index column | monotonicallyIncreasingId | Available options: zipWithUniqueId, zipWithIndex, monotonicallyIncreasingId |
| sparkfe.concatjoin.jointype | The method for concat join | inner | Available options: inner, left, last |
| sparkfe.enable.native.last.join | Enable NativeLastJoin or not | true | Has better performance than left join |
| sparkfe.enable.unsaferow.optimization | Enable UnsafeRow optimization or not | false | It can reduce the overhead of encoding but some complex types are not supported yet |
| sparkfe.physical.plan.graphviz.path | The path to export the image of physical plans | "" | Do not export image by default |
