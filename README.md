# Convivio Apache Kafka Microservice

This microservice uses [Apache Kafka](https://kafka.apache.org/) to provide real-time data pipelines and distributed streaming.

## Install
### 1. Create a one-node docker-machine for the Kafka container

Create a Docker machine for the Kafka container:

```
$ docker-machine create --driver=virtualbox --virtualbox-memory "6000" ap-kafka
```
Get the docker machine environment.
```
$ docker-machine env ap-kafka
```

Modify the `KAFKA_ADVERTISED_HOST_NAME` environment variable in your `.env` file to use the IP of the new Docker machine for Kafka.

Configure your shell:
```
$ eval $(docker-machine env ap-kafka)
```

Then, build the Docker instance:

```
$ make up
```
