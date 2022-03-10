### Install docker-compose
```shell
# Download
curl -SL https://github.com/docker/compose/releases/download/v2.2.3/docker-compose-linux-x86_64 -o docker-compose

# Install
mv docker-compose /usr/bin/

# Set permission
chmod +x /usr/bin/docker-compose
```

### Run component
```shell
# Hadoop
cd cicd/hadoop
docker-compose up

# Hadoop, Spark, Kafka, Solr, Cassandra
cd cicd/package
docker-compose up

# Hadoop, and Hbase
cd cicd/hadoop
docker-compose up

# Hadoop, and Hive
cd cicd/hive
docker-compose up

# Cassandra
cd cicd/cassandra
docker-compose up
```
Notes: If the container is not running or fail, using `docker start container_name` to start container.
Example: docker start cicd-kafka-1
