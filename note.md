# Hadoop

`http://demo:50070`

# HBase

`http://demo:16010`

# Storm 

## Start nimbus(first node only)
```shell
$ nohup storm nimbus >> nimbus.log 2>&1 &
```

## Start supervisor(Each node)
```shell
$ nohup storm supervisor >> supervisor.log 2>&1 &
```

## Start storm UI(first node only)
```shell
$ nohup storm ui >> ui.log 2>&1 &
```

## Start Logviewer(Each node)
```shell
$ nohup storm logviewer > logviewer.log &
```

## Demo

http://192.168.33.10:8080

## Kafka

```
$ bin/zookeeper-server-start.sh -daemon config/zookeeper.properties
$ bin/kafka-server-start.sh -daemon config/server.properties
```

```
$ bin/kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic TopicName
```

```
$ bin/kafka-topics.sh --list --zookeeper localhost:2181
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
$ mvn exec:java -Dexec.mainClass=kyun.hadoop.HDFSClient
```

<console.aws.amazon.com>
neobns.jwlee@gmail.com
