# Build For Different Operating Systems

## Introduction

SparkFE is the native execution engine which need to be built in different operating systems.

## Compile Commands

For different operating systems, the commands of compliation are listed as follows.

| Operating System | Compile Command | Notice |
| ---------------- | --------------- | ------ |
| Linux   | mvn clean package| Support CentOS 6, Ubuntu and other Linux distros |
| MacOS   | mvn clean package -Pmacos | Support macOS Big Sur and later versions |
| All in one | mvn clean package -Pallinone | Support Linux and MacOS at the same time |

## Build SparkFE Distribution

The source code of SparkFE distribution is in the `spark` submodule of SparkFE. It relies on the release of `sparkfe` module and use `allinone` version by default.

If you want to build for Linux or MacOS, just modify `sql/core/pom.xml` and change the dependency.

```
<dependency>
    <groupId>com._4paradigm.hybridsql</groupId>
    <artifactId>sparkfe</artifactId>
    <version>0.1.0-SNAPSHOT-allinone</version>
</dependency>
```
