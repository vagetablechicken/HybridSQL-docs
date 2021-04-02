# 快速开始

## Build

### Get source code and pull docker

```shell
git clone git@github.com:4paradigm/HybridSE.git
cd HybridSE
docker run -v `pwd`:/HybridSE -it ghcr.io/4paradigm/centos6_gcc7_hybridsql:latest
cd /Hybridse
# init enviroment before build
source tools/init_env.profile.sh
```

建议开发者使用我们提供的镜像编译和安装库。若需要使用自己的开发环境，请确保相关依赖库正确安装。编译环境和依赖库可参考 [HybridSQL-docker](https://github.com/4paradigm/HybridSQL-docker/blob/main/README.md)

### Configure and build

```shell
cd /HybridSE
mkdir -p build && cd build
cmake ..
# just compile the core library
make -j4
```

### Install

```shell
cd /HybridSE
mkdir -p build && cd build
cmake ..  -DCMAKE_INSTALL_PREFIX="CONFIG_YOUR_HYRBIDSE_DIRECTORY"
make -j4 install
```

编译配置项说明:

- `-DCMAKE_BUILD_TYPE=type`:  可选的编译类型包括 Debug, Release, RelWithDebInfo (defualt is `RelWithDebInfo`), 编译类型
- `-DCMAKE_INSTALL_PREFIX=directory`: Specify for *directory* the full path name of where you want the HybridSE libraries to be installed (default `/usr/local`)
- `-DTESTING_ENABLE=On`: 开启测试的编译 (default is `OFF`)
- `-DEXAMPLES_ENABLE=On`: 开启`examples`模块的编译(default is `OFF`)
- `-DBENCHMARK_ENABLE=On`: 开启`benchmark`模块的编译 (default is `OFF`)
- `-DJAVASDK_ENABLE=On`: 开启JAVA SDK的编译 (default is `ON`)
- `-DPYSDK_ENABLE=On` : 开启Python SDK的编译(default is `ON`)

## Run tests

```shell
cd /Hybridse
mkdir -p build & cd buid
cmake .. -DTESTING_ENABLE=ON
export SQL_CASE_BASE_DIR=/HybridSE 
make -j4 && make -j4 test
```

## Run simple engine demo

```shell
cd /HybridSE
mkdir build
cd build
cmake ..
make -j4 hybridse_proto && make -j4 hybridse_parser && make -j4 simple_engine_demo
./src/simple_engine_demo
```

## Run ToyDB

### Build ToyDB

```shell
cd /HybridSE
mkdir build 
cmake .. -DEXAMPLES_ENABLE=ON 
make -j4 hybridse_proto && make -j4 hybride_parser && make toydb -j4
```

### Start ToyDB

```
cd /HybridSE/examples/toydb/onebox
sh start_all.sh
sh start_cli.sh
```

ToyDB是基于HybridSE开发的简易内存数据库. 它支持基本的数据库操作和SQL查询语句。详细使用参见 [ToyDB使用手册](./toydb_usage/toydb_quickstart.md)

