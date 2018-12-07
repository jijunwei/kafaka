# kafaka
MACdeMacBook-Air:bin MAC$ ./kafka-server-start.sh -daemon ../config/server.properties 

MACdeMacBook-Air:bin MAC$ ./kafka-topics.sh --zookeeper localhost:2181 --create --topic t_test --partitions 5 --replication-factor 1
WARNING: Due to limitations in metric names, topics with a period ('.') or underscore ('_') could collide. To avoid issues it is best to use either, but not both.
Created topic "t_test".

MACdeMacBook-Air:bin MAC$ ./kafka-console-producer.sh --broker-list localhost:9092 --topic t_test
>

./kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic t_test --from-beginning

MACdeMacBook-Air:bin MAC$ ./kafka-topics.sh --zookeeper localhost:2181 --describe --topic t_test
Topic:t_test	PartitionCount:5	ReplicationFactor:1	Configs:
	Topic: t_test	Partition: 0	Leader: 0	Replicas: 0	Isr: 0
	Topic: t_test	Partition: 1	Leader: 0	Replicas: 0	Isr: 0
	Topic: t_test	Partition: 2	Leader: 0	Replicas: 0	Isr: 0
	Topic: t_test	Partition: 3	Leader: 0	Replicas: 0	Isr: 0
	Topic: t_test	Partition: 4	Leader: 0	Replicas: 0	Isr: 0
MACdeMacBook-Air:bin MAC$ 
