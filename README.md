# Kafka-Docker-Setup


 - Clone this repository

 - Move inside the cloned directory and execute the following command (Make sure docker is running)

```
This will make sure that you load everything from your docker-compose file and start docker container
docker compose up -d
```

 - Now once the container is up, use the following command to enter the kafka shell running inside the container

```
 docker exec -it -w /opt/kafka/bin broker sh
```

- To Add a topic in Kafka,

```
./kafka-topics.sh --create --topic sample-topic --bootstrap-server broker:29092
```

- To list all topics in kafka,

```
./kafka-topics.sh --bootstrap-server broker:29092 --list
```

- To start consumer on a topic,

```
./kafka-console-consumer.sh --topic sample-topic --from-beginning --bootstrap-server broker:29092
```


- To produce the data in the topic,

```
./kafka-console-producer.sh --topic sample-topic --bootstrap-server broker:29092
```
