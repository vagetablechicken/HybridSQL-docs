# Quick Start

## Build 

```shell
git clone https://github.com/4paradigm/HybridSE.git
cd HybridSE
docker run -v `pwd`:/HybridSE -it ghcr.io/4paradigm/centos6_gcc7_hybridsql:latest
cd /HybridSE
sh tools/build_hybridse.sh
```

### 

# Getting Started 

## How to Build

```shell
git clone https://github.com/4paradigm/HybridSE.git
cd HybridSE
docker run -v `pwd`:/HybridSE -it ghcr.io/4paradigm/centos6_gcc7_hybridsql:latest
cd /HybridSE
sh tools/build_hybridse.sh
```

##  How to use a Demo

### Simple Engine Demo

```shell
cd /HybridSE
mkdir build
cd build
cmake ..
make -j4 hybridse_proto && make -j4 hybride_parser && make -j4 simple_engine_demo
./src/simple_engine_demo
```

### ToyDB Demo

#### Build ToyDB

```shell
cd /HybridSE
mkdir build 
cmake .. -DEXAMPLES_ENABLE=ON 
make -j4 hybridse_proto && make -j4 hybride_parser && make toydb -j4
```

#### Start ToyDB

```
cd /HybridSE/examples/toydb/onebox
sh start_all.sh
sh start_cli.sh
```

Toydb支持基本的NewSQL数据库的操作，具体操作细节可参考[ToyDB使用手册](./toydb_tutorial/toydb_usage.md)



## Java编程接口
HybridSE也提供Java编程接口，基于Java/Scala的项目也可以使用来实现SQL语法支持，详情参考HybridSE Java SDK。


## 示例： 一个简单NewSQL数据库
开发者使用HybridSE可以快速实现一个支持SQL的高性能数据库。examples/toydb就是一个简易的单机版面向实时决策的NewSQL数据库。

[ToyDB快速使用手册](./toydb_tutorial/toydb_usage.md)