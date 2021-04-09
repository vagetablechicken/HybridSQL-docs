# 从源码构建项目

## 简介

SparkFE是开源项目，用户可以下载源码并编译项目，本文档介绍从源码构建项目的所有细节。

## 环境准备

SparkFE基于Scala/Java开发，用户需要准备和安装以下依赖。

| 基础软件| 版本 |
| -------| --- |
| Java | OpenJDK 1.8.0+ |
| Maven | 3.6.0+ |
| Python | 3.7.0+ |
| Git | 2.20.0+ |

也可以使用官方Docker镜像进行开发。

```
docker run -it 4pdosc/sparkfe bash
```

## 下载源码

SparkFE包含Spark作为子模块，如果要编译`sparkfe模块`和`SparkFE发行版`，需要用以下命令下载源码。

```
git clone --recurse-submodules git@github.com:4paradigm/SparkFE.git
```

## 编译sparkfe模块

`sparkfe模块`是实现原生执行引擎的核心，包含了对SparkSQL接口的封装以及最终物理计划生成等功能实现。

编译方式与其他Maven项目一致，使用下面的编译命令即可。

```
cd ./SparkFE/sparkfe/

mvn clean package
```

## 编译SparkFE发行版

`SparkFE发行版`是兼容标准Spark的预编译包，用户使用SparkFE发行版用法与标准Spark一致，无论是Scala、Java、Python还是R实现的应用代码都不需要修改。

编译打包方法和标准Spark一致，使用Spark子模块执行下面命令即可。

```
cd ../spark/

./dev/make-distribution.sh --name sparkfe --pip --tgz -Phadoop-2.7 -Pyarn
```

## 注意事项

SparkFE实现的原生执行引擎，底层根据不同体系架构生成的二进制码也不同，实现不依赖于JVM类跨平台虚拟机，因此不同操作系统的编译依赖也是不一样的。上述命令默认只在Linux或者Docker容器内环境运行，使用不同操作系统编译参考后面的[使用不同操作系统构建](./build_for_different_os.md)文档。
