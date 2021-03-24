# DataHandler

`include <vm/catalog.h>`

## Summary

`DataHandler`继承自` ListV<Row>`定义了HybridSE的标准行编码数据处理接口，定义了一系列数据集的访问接口

| Constructors and Destructors |
| :--------------------------- |
| [DataHandler](#DataHandler)  |

| Public functions                          | Return type          |
| :---------------------------------------- | -------------------- |
| [GetSchema](#GetSchema)                   | `const Schema*`      |
| [GetName](#GetName)                       | `const std::string&` |
| [GetDatabase](#GetDatabase)               | `const std::string&` |
| [GetHanlderType](#GetHanlderType)         | `const HandlerType`  |
| [GetHandlerTypeName](#GetHandlerTypeName) | `const std::string`  |
| GetIterator                               |                      |

## Public functions

#### GetHanlderType

```c++
DataHandler() {}
```

DataHandler的构造函数。

#### GetHanlderType

```c++
virtual HandlerType GetHanlderType()
```

返回数据集的类型

```c++
enum HandlerType { kRowHandler, kTableHandler, kPartitionHandler };
```

#### GetHandlerTypeName

```c++
// get handler type name
virtual const std::string GetHandlerTypeName()
```

返回数据集的类型名字

#### GetIterator

```c++
std::unique_ptr<RowIterator> GetIterator()
```



#### GetCount

```c++
const uint64_t GetCount()
```

