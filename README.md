# Twaddle

## Project Build commands
- Download Kafka (includes zookeeper)
- Build Kafka after extracting the tar file
```
./gradlew jar
```
- In /bin run Zookeeper
```
./zookeeper-server-start.sh ../config/zookeeper.properties
```
- In /bin run Kafka
```
./kafka-server-start.sh ../config/server.properties
```
- In /bin create a new kafka topic
```
./kafka-topics.sh --create --topic kafka-chat --replication-factor 1 --partitions 2 --zookeeper localhost:2181
```
- To quickly test - post a message after running below command
```
./kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic kafka-chat
```

## npm packages
```
npm i sockjs-client @material-ui/core react-stomp axios
```
