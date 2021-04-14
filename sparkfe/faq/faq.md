# FAQ

## 如何部署SparkFE？

SparkFE和Spark一样，是一个分布式应用编程类库，不需要单独部署，可以在本地、容器内或者Yarn、Kubernetes集群上运行。在开发调试阶段，使用本地和容器环境一般可以满足需求，大数据处理则需要Yarn这样的分布式环境。

## SparkFE是否和Spark upstream同步？

是的，SparkFE distribution是基于Spark源码修改，可以支持Spark 3.0及后续版本，侵入源码的修改少与一百行，除了SparkSQL有优化实现外其他功能保持与Spark一致，未来也将跟随Spark版本同步发展。

## SparkFE性能提升是否需要硬件支持？

目前SparkFE生成的平台相关二进制码都是基于平台CPU优化的，不需要额外的硬件支持，相当于无成本的性能提升并且降低项目TCO。
