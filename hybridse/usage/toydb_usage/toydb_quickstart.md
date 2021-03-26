# ToyDB Quick Start

## Build

```shell
cd /HybridSE
mkdir build 
cmake .. -DEXAMPLES_ENABLE=ON 
make -j4 hybridse_proto && make -j4 hybride_parser && make toydb -j4
```

## Start ToyDB

```shell
cd /HybridSE/examples/toydb/onebox
sh start_all.sh
sh start_cli.sh
```

### Start dbms

```shell script
BUILD_DIR=$PROJECT_ROOT/build/examples/toydb
"$BUILD_DIR/src/toydb" --role=dbms  --toydb_port=9211 > dbms.log 2>&1 &
sleep 5
```

### Start a tablet

```shell script
BUILD_DIR=$PROJECT_ROOT/build/examples/toydb
"$BUILD_DIR/src/toydb" --role=tablet --toydb_endpoint=127.0.0.1:9212 --toydb_port=9212 --dbms_endpoint=127.0.0.1:9211 > tablet.log 2>&1 &
sleep 5
```
### Start a client

```shell
BUILD_DIR=$PROJECT_ROOT/build/examples/toydb
"${BUILD_DIR}/src/toydb" --role=client --tablet_endpoint=127.0.0.1:9212 --toydb_endpoint=127.0.0.1:9211
```


## ToyDB examples

### Databse Operation
#### Create database

```mysql
CREATE DATABASE db_name
```

#### Go into database

```MYSQL
USE db_name;
```

#### Show databse list 

```mysql
 SHOW DATABASES;
```

### Table  Operation

#### Create table

```mysql
-- create table t1
create table IF NOT EXISTS t1(
    column1 int NOT NULL,
    column2 int NOT NULL,
    column3 float NOT NULL,
    column4 bigint NOT NULL,
    column5 int NOT NULL,
    column6 string,
    index(key=column1, ts=column4)
);
```

#### Show table schema

```SQL
DESC t1;
+---------+---------+------+
| Field   | Type    | Null |
+---------+---------+------+
| column1 | kInt64  | NO   |
| col2    | kString | NO   |
| col3    | kFloat  | NO   |
+---------+---------+------+
```

#### Show table list 

```mysql
SHOW TABLES;
```

#### Insert data

```SQL
-- prepare t1 data 
insert into t1 values(1, 2, 3.3, 1000, 5, "hello");
insert into t1 values(1, 3, 4.4, 2000, 6, "world");
insert into t1 values(11, 4, 5.5, 3000, 7, "string1");
insert into t1 values(11, 5, 6.6, 4000, 8, "string2");
insert into t1 values(11, 6, 7.7, 5000, 9, "string3");
insert into t1 values(1, 2, 3.3, 1000, 5, "hello");
insert into t1 values(1, 3, 4.4, 2000, 6, "world");
insert into t1 values(11, 4, 5.5, 3000, 7, "string1");
insert into t1 values(11, 5, 6.6, 4000, 8, "string2");
insert into t1 values(11, 6, 7.7, 5000, 9, "string3");
```

### SQL Query

#### Simple query statement
```sql
-- simple query 
SELECT column1, column2, column1 + (2*column5) as f1 FROM t1 limit 10;
```

#### Window query statement

```sql
-- window query t1
select
sum(column1) OVER w1 as w1_col1_sum, 
sum(column2) OVER w1 as w1_col2_sum, 
sum(column3) OVER w1 as w1_col3_sum, 
sum(column4) OVER w1 as w1_col4_sum, 
sum(column5) OVER w1 as w1_col5_sum 
FROM t1 WINDOW w1 AS (PARTITION BY column1 ORDER BY column4 ROWS BETWEEN 3000 PRECEDING AND CURRENT ROW) limit 100;

```
