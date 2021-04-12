# 底层实现

## 简介

SparkFE底层基于LLVM和自研的SQL引擎进行优化，有以下的性能优化。

* [NativeWindow优化](./native_window_compute.md)
* [原生LastJoin优化](./native_last_join_optimization.md)
* [UnsafeRow编码优化](./unsaferow_codec_optimization.md)
* [多窗口并行计算优化](./multiple_window_concurrent_compute_optimization.md)
