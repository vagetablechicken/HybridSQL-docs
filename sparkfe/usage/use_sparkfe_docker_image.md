# 使用SparkFE镜像

## 使用官方镜像

SparkFE提供了[官方Docker容器镜像](https://hub.docker.com/r/4pdosc/sparkfe)，使用以下命令即可运行。

```bash
docker run -it 4pdosc/sparkfe bash
```

镜像内包含以下基础软件。

| 基础软件| 版本 |
| -------| --- |
| Java | OpenJDK 1.8.0 |
| Maven | 3.6.3 |
| Git | 2.20.1 |
| Python | 3.7.3 |
| Python3-pip | 18.1 |
| PySpark | 3.0.0 |
| Vim | 8.1 |

镜像内包含以下基础目录。

| 基础目录| 介绍 |
| -------| --- |
| /usr/local/openjdk-8 | $JAVA_HOME |
| /usr/share/maven | $MAVEN_HOME |
| /spark-3.0.0-bin-sparkfe | 预编译SparkFE版本, $SPARK_HOME |
| /spark-3.0.0-bin-hadoop2.7 | 预编译标准Spark版本 |

## 构建镜像

镜像构建脚本同样使用Github托管，代码地址为 https://github.com/4paradigm/SparkFE/tree/main/docker 。

使用以下命令可以从本地构建SparkFE容器镜像。

```
git clone https://github.com/4paradigm/SparkFE.git

cd ./SparkFE/docker/

docker build -t 4pdosc/sparkfe .
```
