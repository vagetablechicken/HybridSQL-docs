# SparkFE Docker Image

## Use Docker Image

SparkFE has provided [official docker image](https://hub.docker.com/r/4pdosc/sparkfe) and you can use with this command.

```bash
docker run -it 4pdosc/sparkfe bash
```

The docker image has included the following softwares.

| Software | Version |
| -------- | ------- |
| Java | OpenJDK 1.8.0 |
| Maven | 3.6.3 |
| Git | 2.20.1 |
| Python | 3.7.3 |
| Python3-pip | 18.1 |
| PySpark | 3.0.0 |
| Vim | 8.1 |

The docker image has included the following directories.

| Directory | Introduction |
| --------- | ------------ |
| /usr/local/openjdk-8 | $JAVA_HOME |
| /usr/share/maven | $MAVEN_HOME |
| /spark-3.0.0-bin-sparkfe | Pre-built SparkFE distribution, $SPARK_HOME |
| /spark-3.0.0-bin-hadoop2.7 | Pre-built Spark distribution |

## Build Docker Image

The scripts of building docker image are maintained in Github as well. Please refer to https://github.com/4paradigm/SparkFE/tree/main/docker .

You can build SparkFE docker image in local server.

```
git clone https://github.com/4paradigm/SparkFE.git

cd ./SparkFE/docker/

docker build -t 4pdosc/sparkfe .
```
