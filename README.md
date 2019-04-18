Kafka in Docker
===

This repository provides everything you need to run Kafka in Docker. Forked from [spotify/kafka](https://github.com/spotify/docker-kafka) and updated to Kafka 2.2.0


Why?
---
The main hurdle of running Kafka in Docker is that it depends on Zookeeper.
Compared to other Kafka docker images, this one runs both Zookeeper and Kafka
in the same container. This means:

* No dependency on an external Zookeeper host, or linking to another container
* Zookeeper and Kafka are configured to work together out of the box

Run
---

```bash
docker run -p 2181:2181 -p 9092:9092 mswatosh/kafka
```

Defaults
---
Ports

* Zookeeper: 2181
* Kafka: 9092
* advertised.listeners=PLAINTEXT://localhost:9092 (allows for local use)

Build from Source
---

    docker build -t mswatosh/kafka kafka/