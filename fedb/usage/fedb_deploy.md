# 部署FEDB
## 从docker部署

## 在物理机部署
### 部署zookeeper
建议部署3.4.10或者3.4.14版本  
如果已有可用zookeeper集群可略过此步骤  
#### 下载zookeeper安装包
```
$ wget https://archive.apache.org/dist/zookeeper/zookeeper-3.4.14/zookeeper-3.4.14.tar.gz
$ tar -zxvf zookeeper-3.4.14.tar.gz
$ cd zookeeper-3.4.14
$ cp conf/zoo_sample.cfg conf/zoo.cfg
``` 
#### 修改配置文件
打开文件conf/zoo.cfg修改dataDir和clientPort
```
dataDir=./data
clientPort=6181
```
#### 启动zookeeper
```
$ sh bin/zkServer.sh start
```
部署zookeeper集群[参考这里](https://zookeeper.apache.org/doc/r3.4.14/zookeeperStarted.html)
### 部署nameserver
#### 1 下载FEDB部署包
````
$ wget http://pkg.4paradigm.com/fedb/fedb-2.0.0.0.tar.gz
$ tar -zxvf fedb-2.0.0.0.tar.gz
$ mv fedb-2.0.0.0 fedb-ns-2.0.0.0
$ cd fedb-ns-2.0.0.0
````
#### 2 修改配置文件conf/nameserver.flags
* 修改endpoint
* 修改zk_cluster为已经启动的zk集群地址. ip为zk所在机器的ip, port为zk配置文件中clientPort配置的端口号. 如果zk是集群模式用逗号分割, 格式为ip1:port1,ip2:port2,ip3:port3
* 如果和其他FEDB共用zk需要修改zk_root_path
```
--endpoint=172.27.128.31:6527
--role=nameserver
--zk_cluster=172.27.128.33:7181,172.27.128.32:7181,172.27.128.31:7181
--zk_root_path=/fedb_cluster
--enable_distsql=true
```
**注: endpoint不能用0.0.0.0和127.0.0.1**
#### 3 启动服务
```
sh bin/start_ns.sh start
```
### 部署tablet
#### 1 下载FEDB部署包
```
$ wget http://pkg.4paradigm.com/fedb/fedb-2.0.0.0.tar.gz
$ tar -zxvf fedb-2.0.0.0.tar.gz
$ mv fedb-2.0.0.0 fedb-tablet-2.0.0.0
$ cd fedb-tablet-2.0.0.0
```
#### 2 修改配置文件conf/tablet.flags
* 修改endpoint
* 修改zk_cluster为已经启动的zk集群地址
* 如果和其他FEDB共用zk需要修改zk_root_path
```
--endpoint=172.27.128.33:9527
--role=tablet

# if tablet run as cluster mode zk_cluster and zk_root_path should be set
--zk_cluster=172.27.128.33:7181,172.27.128.32:7181,172.27.128.31:7181
--zk_root_path=/fedb_cluster
--enable_distsql=true
```
**注意：**
* endpoint不能用0.0.0.0和127.0.0.1 
* 如果此处使用的域名, 所有使用rtidb的client所在的机器都得配上对应的host. 不然会访问不到
* zk_cluster和zk_root_path配置和nameserver的保持一致
#### 3 启动服务
```
$ sh bin/start.sh start
```
**注: 服务启动后会在bin目录下产生tablet.pid文件, 里边保存启动时的进程号。如果该文件内的pid正在运行则会启动失败**

重复以上步骤部署多个nameserver和tablet