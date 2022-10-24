Kafka stream example Wordcount

This application shows how a simple Kafka configuration of an input and output topic counts the words
entered at the input topic.

Establish the Kafka environment by starting the ZooKeeper and the Kafka broker. Create then the input and output topic and start the Java WordCountDemo.

By courtesy of Apache Kafka

Summary:

- install Kafka, https://www.apache.org/dyn/closer.cgi?path=/kafka/3.3.1/kafka_2.13-3.3.1.tgz
- Start the ZooKeeper service, bin/zookeeper-server-start.sh config/zookeeper.properties
- Start the Kafka broker service, bin/kafka-server-start.sh config/server.properties
- create the input topic named streams-plaintext-input, bin/kafka-topics.sh --create \
    --bootstrap-server localhost:9092 \
    --replication-factor 1 \
    --partitions 1 \
    --topic streams-plaintext-input
Created topic "streams-plaintext-input".
- create the input topic named streams-wordcount-output, bin/kafka-topics.sh --create \
    --bootstrap-server localhost:9092 \
    --replication-factor 1 \
    --partitions 1 \
    --topic streams-wordcount-output \
    --config cleanup.policy=compact
Created topic "streams-wordcount-output".
- Start Java WordCountDemo

