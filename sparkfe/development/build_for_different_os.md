# 使用不同操作系统构建

## 介绍

SparkFE是一个原生的计算执行引擎，需要根据不同的操作系统进行单独构建。

## 构建命令

针对不同的操作系统，构建命令如下。

| 操作系统 | 编译命令 | 备注 |
| ------- | ------ | ---- |
| Linux   | mvn clean package| 支持CentOS 6、Ubuntu等Linux发行版 |
| MacOS   | mvn clean package -Pmacos | 支持macOS Big Sur以及后续版本 |
| All in one | mvn clean package -Pallinone | 同时支持Linux、MacOS操作系统 |

## 构建SparkFE发行版

SparkFE发行版的源码在项目中的spark子模块中，依赖正式发布的sparkfe的模块，默认使用allinone版本构建。

如果需要针对Linux或者MacOS进行编译优化，需要修改`sql/core/pom.xml`文件的以下依赖。

```
<dependency>
    <groupId>com._4paradigm.hybridsql</groupId>
    <artifactId>sparkfe</artifactId>
    <version>0.1.0-SNAPSHOT-allinone</version>
</dependency>
```
