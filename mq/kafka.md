

## 基本概念

一个kafka架构有多个Producer，多个Broker，若干个consumer group，一个Zookeeper集群（集群配置 选取leader）组成。

### Broker 

消息中间件处理节点（服务器），一个节点就是一个broker，一个Kafka集群由一个或多个broker组成

### Topic

Kafka对消息进行归类，发送到集群的每一条消息都要指定一个topic

### Partition

物理上的概念，每个topic包含一个或多个partition，一个partition对应一个文件夹，这个文件夹下存储partition的数据和索引文件，每个partition内部是有序的

### ConsumerGroup

每个consumer属于一个特定的consumer group，可为每个consumer指定group name，若不指定，则属于默认的group，一条消息可以发送到不同的consumer group，但一个consumer group中只能有一个consumer能消费这条消息


## kafka特性


* 高吞吐量、低延迟：kafka每秒可以处理几十万条消息，它的延迟最低只有几毫秒，每个topic可以分多个partition, consumer group 对partition进行consume操作。
* 可扩展性：kafka集群支持热扩展
* 持久性、可靠性：消息被持久化到本地磁盘，并且支持数据备份防止数据丢失
* 容错性：允许集群中节点失败（若副本数量为n,则允许n-1个节点失败）
* 高并发：支持数千个客户端同时读写