# Quick Start

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

We strongly recommand developers building hybridse with HybridSQL-docker. Otherwise, the developer have to install related thirdparty lib. See the [HybridSQL-docker](https://github.com/4paradigm/HybridSQL-docker/blob/main/README.md)

### Configure and build

```shell
cd /Hybridse
mkdir -p build && cd build
cmake ..
# just compile the core library
make -j4
```

### Install

```shell
cd /Hybridse
mkdir -p build && cd build
cmake ..  -DCMAKE_INSTALL_PREFIX="CONFIG_YOUR_HYRBIDSE_DIRECTORY"
make -j4 install
```

Some Common options:

- `-DCMAKE_BUILD_TYPE=type`:  Optional valid *type* are Debug, Release, RelWithDebInfo (defualt is `RelWithDebInfo`)
- `-DCMAKE_INSTALL_PREFIX=directory`: Specify for *directory* the full path name of where you want the HybridSE libraries to be installed (default `/usr/local`)
- `-DTESTING_ENABLE=On`: Compile with test enabled (default is `OFF`)
- `-DEXAMPLES_ENABLE=On`: Compile with examples disabled (default is `OFF`)
- `-DBENCHMARK_ENABLE=On`: Compile with benchmark enabled (default is `OFF`)
- `-DJAVASDK_ENABLE=On`: Compile with java sdk enabled (default is `ON`)
- `-DPYSDK_ENABLE=On` : Compile with python sdk enabled (default is `ON`)

## Run unit test

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

## Run ToyDB Demo

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

Toydb is a toy In-Memory Database developed upon HybridSE. It supported basic database operations and NewSQL query statements. 

We also offer an [ToyDB quick start](./toydb_usage/toydb_quickstart.md) for quickly learning the basics of using Toydb.

