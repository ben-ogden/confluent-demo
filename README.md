# confluent-demo
A docker-based quick start for a Confluent demo

https://user-images.githubusercontent.com/7433434/121204315-ceee7f00-c844-11eb-99f5-a2eb0cfd5012.mov

`./docker-compose up -d` 

Starts Confluent Platform 6.1: Zookeeper, Confluent Server (Broker), Schema Registry, Connect, ksqlDB, Control Center and the REST Proxy. Includes optional containers for ksqlDB CLI and kafkacat.

Access Control Center at http://localhost:9021

Important: For macOS and Windows, Docker runs in a virtual machine, and you must allocate at least 8 GB of RAM for the Docker VM to run the Kafka stack. The default is 2 GB.


