# Log Monitoring Architecture

## 모니터링 아키텍처 및 요소기술 
* Lambda Architecture
* Monitoring Architecture
* Tech Stack

## 하둡 아키텍처 및 HBase를 이용한 대용량 테이블 설계

### Hadoop

```
$ start-dfs.sh
$ start-yarn.sh
$ hadoop fs -df -h
```

`http://demo:50070`

#### HDFS

#### Map/Reduce


### HBase

```
$ start-hbase.sh
$ hbase shell
```

`http://demo:16010`

#### HBase 사용법

### Phoenix

```
$ sqlline.py localhost
```

## Storm 을 이용한 실시간 데이터 분석

### Start nimbus(first node only)
```shell
$ nohup storm nimbus >> nimbus.log 2>&1 &
```

### Start supervisor(Each node)
```shell
$ nohup storm supervisor >> supervisor.log 2>&1 &
```

### Start storm UI(first node only)
```shell
$ nohup storm ui >> ui.log 2>&1 &
```

### Start Logviewer(Each node)
```shell
$ nohup storm logviewer > logviewer.log &
```

### Demo

http://192.168.33.10:8080

## Kafka 및 Redis 활용

```
$ bin/zookeeper-server-start.sh -daemon config/zookeeper.properties
$ bin/kafka-server-start.sh -daemon config/server.properties
$ jps
7355 QuorumPeerMain
7803 Kafka
```

```
$ bin/kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic TopicName
Created topic "TopicName".
```

```
$ bin/kafka-topics.sh --list --zookeeper localhost:2181
TopicName
```

```
$ bin/kafka-topics.sh --describe --zookeeper localhost:2181 --topic TopicName 
```

```
$ bin/kafka-console-producer.sh --broker-list localhost:9092 --topic TestTopic
$ bin/kafka-console-consumer.sh --zookeeper localhost:2181 --topic TestTopic --from-beginning
```

## 기타

```
about:blank
data:text/html, <html contenteditable>
```
