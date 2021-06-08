# confluent-demo
A docker-based quick start for a Confluent demo

https://user-images.githubusercontent.com/7433434/121204315-ceee7f00-c844-11eb-99f5-a2eb0cfd5012.mov


## Setup

Starts Confluent Platform 6.1: Zookeeper, Confluent Server (Broker), Schema Registry, Connect, ksqlDB, Control Center and the REST Proxy. Includes optional containers for ksqlDB CLI and kafkacat and PostgreSQL.

`./docker compose up -d` 

Important: For macOS and Windows, Docker runs in a virtual machine, and you must allocate at least 8 GB of RAM for the Docker VM to run the Kafka stack. The default is 2 GB.


## Control Center

Access Control Center at http://localhost:9021


## Connect

View available connectors from Control Center, or use the REST interface -

`curl -s localhost:8083/connector-plugins|jq '.[].class'`

## ksqlDB

To access the ksqlDB CLI, run

`docker compose exec ksqldb-cli ksql http://ksqldb-server:8088`


## PostgreSQL

To connect to PostgreSQL -

`docker-compose exec postgres bash -c 'psql -U $POSTGRES_USER $POSTGRES_DB'`


## Troubleshooting

To see status of containers in the stack, use

`docker ps`

To view the logs for a container with 

`docker compose logs <container-name>`

For example, to view the logs for connect, try 

`docker compose logs connect`


## Connector Documentation

### Sample Data

* Datagen Source Connector: https://github.com/confluentinc/kafka-connect-datagen
* Voluble Source Connector: https://github.com/MichaelDrogalis/voluble

### File-based

* SpoolDir: https://docs.confluent.io/kafka-connect-spooldir/current/index.html
* FilePulse: https://github.com/streamthoughts/kafka-connect-file-pulse


