
# Apachie kafka

kafka cluster = kafka server(broker) + zookeeper

## Run kafka
```bash
bin/zookeeper-server-start.sh config/zookeeper.properties  # start Zookeeper in port 2181
bin/kafka-server-start.sh config/server.properties         # start Kafka server(broker) in port 9092
bin/kafka-topice.sh --create --bootstrap-server localhost:9092 replication-factor 1 partitions 3 --topic name_of_topice  # create a new topic with three folder in /tmp/kafka-logs
bin/kafka-topice.sh                                            # not run just show arguments
bin/kafka-topice.sh --create --bootstrap-server localhost:9092 --topic name_of_topice  # create a new topic with default arguements
bin/kafka-topice.sh --list --bootstrap-server localhost:9092      # list all available topics
bin/kafka-topice.sh --list --zookeeper localhost:2181           # list all available topics
bin/kafka-topice.sh --describe --bootstrap-server localhost:2181 --topic name_of_topice          # describe a topic
bin/kafka-topice.sh --describe --zookeeper localhost:2181 --topic name_of_topice  # describe configuration of topic, 1.pratitionCount: number of folders per topic, 2.ReplicationFactor: the number of servers where data will store 3. details for every partition[ number of folders +  id of broker by default is zero]
# ReplicationFactor: if we have three servers every message will ne stores in every of three servers, so if one server can not be available the others can
bin/kafka-console-producer.sh --broker-list localhost:9092 --topic name_of_topice  # connect to broker for writting messages
bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic name_of_topice  # connect to broker for reading just new messages
bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic name_of_topice --from-beginning  # connect to broker for reading messages from beginning (all messages) [if you run another consumer, the new consumer can read message too]
bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic name_of_topice --group GROUP --from-beginning # connect to broker with consumer group
bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --list  # list consumer groups 
bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --describe --group GROUP # describe consumer group
bin/kafka-server-stop.sh                                      # stop Kafka server
rm -rf /tmp/zookeeper & rm-rf /tmp/kafka-logs & rm -rf yourpath/kafka/logs   # delete logs in kafka
```
## Facts
1. We can run multiple producers and consumers at the same time with same arguments at termial. but producers and consumers do not know about each other
2. if you stop one consumer, it will not stop other consumers and producers and vise versa.[they do just a  snigle job]
3. kafka does not store messages forever and after specific time/size will delete messages called *log retention period*[ default: 7days, 10MB ]
4. every consumer must be part of the consumer group with random id. ex: console-soncumer-1534 in logs
5. every topic has a unique name and every message inside of a topic has a unique number called offset. These numbers is immutable. And every new messages append to the end offset list. first message in each topic has offset 0 and consumers start reading messages starting form specific offset.When consumer connects to kafka cluster you are able to specify a specific offset number you want to start reading message from.[ --from-beginning ==> number zero]
6. Producers decides which partition to choose to write message inside that.
7. consumers can connect to one or multiple topices but usually they connect to only one topice
8. consumers can are able to consume messages from multiple partitions
9. if multiple consumers connect the one topice they belong to one consumer group,In such case every single message will be consumed only by one of the consumers in the consume group.

### folder contents
```bash
######## Config/
config/server.properties                                    # Kafka server config
config/zookeeper.properties                                 # Zookeeper config

######## Bin/

######## Logs/
# when you start kafka server, it will create a log folder in /kafka/logs across bin/ and config/
```

## Logs
```bash
# when you start kafka server, it will create a log folder in /kafka/logs across bin/ and config/
server.log                                                  # Kafka server log [samae as your terminal]


### /tmp
/tmp/zookeeper                                             # Zookeeper logs has diff path
/tmp/kafka-logs                                             # logs for producers and consumer [new topic creates a new folder]
0000000000000000000000.log                                # logs for messages of prodeucers
```

## concetps
kafka is a *distributed* *publish-subscribe* *messaging system*
Broker is responsible for saving messages of producers

        Producer ===> Broker ===> Consumer

We can have multiple consumer and multiple producer with one Broker but if this broker fails nobody can read/write messages, so we need to have multiple brokers(cluster of Brokers)

                    Cluster of Brokers   ===> Zookeeper
Producer        [      Broker         ]       Consumer
Producer ===>   [      Broker         ] ====> Consumer
Producer        [      Broker         ]       Consumer
producers can wtire in different Brokers and consumers can read from different Brokers
if Brokers should be publicly accessible set *advertised listeners* in Broker config
How these Brokers can sync with each other? By zookeeper
zookeeper: 
1. Maintain list of active brokers
2. Maintain configuration of topics and partitions
3. elects controller

When you create any topic in kafka cluster, it is created basicly in zookeeper. and zookeeper will create a new folder for that topic. and zookeeper distribute its configuration to all brokers in the cluster ==> so zookeeper is needed for kafka

we can also have a cluster of zookeepers that called *ensemble*
in every ensumble we should set so-called *quorum*
Quorum is the minimum number of servers that should be up and running. If there are less servers than quorum, zookeeper is considered down and all coresponding  brokers that were connected to the cluster will be also down 
so the number of servers in ensemble should be odd like 3 or 5 or 7 (and quorum for them 2 or 3 or 4 ==> (n+1)+1) 9server and 5quorum)

We can have multiple partitions in one topic. And this partitions can be spread between multiple brokers.
If we set a replication factor on the topic level you can create replicas of every message in every partition for that topic.
Replication: If we copy a partition (messages of a topice) from one broker to another broker (or from one prtition to another),
it is called *replication*. So if that broker fail we can use another. The origin partition called *Leader* or **Leader prtition* or *Broker of leader partition* and destination partitions called *follower*. So Leader writes its content(replicates) inside followers. 
Consumers read just from leader and not from followes. Buf if Leader fail, one of the follower become leader. Followers are just relax and wait for
new messages from Leader.
It recommended to have at least two Replica.
One of the brokers that is responsible for managing the state of patitions and replicas called *controlelr*. Controller electes
automatically be zookeeper. and if the controller fail then new controller elected by zookeeper.
controller create different partitions, assign them to diffenre brokers, reassign in sace of faluire broker, and if there was a replication 
configuration on the topic level controller selecet leader for specific partition and select forwards. If leader fail controller decides next leader.
If one broker fail, controller will reassaing the partition of fail broker to a remain broker. controller elect leader partition.




