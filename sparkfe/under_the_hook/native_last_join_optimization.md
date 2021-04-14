# 原生LastJoin优化

## 介绍

LastJoin是SparkFE新增的一种适用于机器学习场景的拼表类型，详细介绍可参考[HybridSE语法介绍](../../hybridse/language_guide/reference.md)。

## LastJoin实现

根据LastJoin语意，要求拼表后行数与左表行数一致，目前SQL标准的inner join和outer join都不能够满足。如果使用Spark来实现LastJoin语意，实现步骤如下。

1. 左表添加一个索引列，保证每一行有唯一ID
2. 左右表使用left outer join
3. 拼表后根据索引列进行reduce

基本的实现代码如下。

```
val indexColumnName = "indexCol"
val orderbyColmn = "orderbyCol"

val t1WithIndex = t1.withColumn(indexColumnName, monotonically_increasing_id())
val t3 = t1WithIndex.join(t2, t1WithIndex("id") === t2("u_id"), "left_outer")

val customOrder = new Ordering[Row]() {
    override def compare(x: Row, y: Row): Int =
    Ordering[Long].compare(x.getAs[Long](orderbyColmn), y.getAs[Long](orderbyColmn))
}

val t4 = t3.groupByKey(row => row.getAs[Long](indexColumnName)).mapGroups {
    case (k, iter) => {
    val maxRow = iter.max(customOrder)
    (maxRow.getAs[Int](0), maxRow.getAs[String](1), maxRow.getAs[String](2), maxRow.getAs[Int](3), maxRow.getAs[Long](4), maxRow.getAs[Int](6), maxRow.getAs[String](7), maxRow.getAs[Long](8))
    }
}
```

从性能上看，LastJoin实现显然不如LeftJoin，但从计算的数据量来看却比后者小很多，主要原因是Spark没有原生LastJoin实现或者拓展，用户必须拼表后再reduce才能得到预期结果。

## 原生LastJoin实现

考虑到LastJoin在机器学习场景还是比较常用了，SparkFE提供了原生的LastJoin实现，无论是网络通信量还是数据计算量都有明显减少。原生LastJoin实现与Spark中其他join type实现类似，需要添加对新类型的支持，并且在BrocastHashJoin、SortMergeJoin和ShuffleHashJoin具体实现中支持这种新类型。

具体实现源码可以在SparkFE的spark子模块中找到。

## 性能对比

对于无排序条件的LastJoin场景，基于Spark的实现和原生LastJoin实现性能对比如下。

![](../image/../images/native_lastjoin_benchmark.png)
