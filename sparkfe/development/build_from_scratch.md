# Build From Scratch

## Introduction

SparkFE is the open-source project which means that developers can download and build the project by theirselves. This documentation introduces all the details of building SparkFE from srcatch.

## Preparation

SparkFE is implemented in Scala and Java. Developers need to install the following dependencies.

| Software | Version |
| -------- | ------- |
| Java | OpenJDK 1.8.0+ |
| Maven | 3.6.0+ |
| Python | 3.7.0+ |
| Git | 2.20.0+ |

You can use the official docker image to develop as well.

```
docker run -it 4pdosc/sparkfe bash
```

## Download Source Code

SparkFE includes Spark as a submodule. If you want to compile `sparkfe module` and `SparkFE distribution`, you can use the following command to download the complete source code.

```
git clone --recurse-submodules git@github.com:4paradigm/SparkFE.git
```

## Compile Sparkfe Module

`sparkfe module` is the core of the native execution engine which includes the functionalities of wraping SparkSQL interfaces and generating the final physical plans.

The way to compile sparkfe module is the same as other maven projects. Here are the commands for compilation.

```
cd ./SparkFE/sparkfe/

mvn clean package
```

## Compile SparkFE Distribution

`SparkFE distribution` is the Spark-compatible pre-built package. Uses can use SparkFE distribution just like standard Spark and do not need to modify the applications in Scala, Java, Python or R.

The way to package SparkFE distribution is the same as Spark. Here the the compile commands which can be run in the Spark submodule.

```
cd ../spark/

./dev/make-distribution.sh --name sparkfe --pip --tgz -Phadoop-2.7 -Pyarn
```

## Notice

The native execution engine of SparkFE will generate different binary code for different computing architectures. The native code is not like JVM which supports cross platforms which means different operating systems may rely on different underlying dependencies. The following commands can not be used within Linux operating system or docker containers. For building in other operating systems, please refer to [Build For Different Operating Systems](./build_for_different_os.md).
