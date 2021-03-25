# EngineMode

## Summary

`EngineMode`定义了若干Engine模式

```c++
enum EngineMode { kBatchMode, kRequestMode, kBatchRequestMode };
```

| Enum Type           | Description                                                  |
| :------------------ | ------------------------------------------------------------ |
| `kBatchMode`        | 批式数据处理模式，是传统的SQL执行模式。                      |
| `kRequestMode`      | 请求式数据处理模式，是`OLDA`下的处理处理模式。一次SQL查询需要传入一条请求数据，在窗口聚合计算时，将以该请求数据作为`CURRENT_ROW`来划定窗口范围计算。 |
| `kBatchRequestMode` | 批量请求式数据处理模式，`请求式数据处理模式`的变体，唯一的区别是，一次SQL查询可以传入一条或者多条请求数据。 |

# 