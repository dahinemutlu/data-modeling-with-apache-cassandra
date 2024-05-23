# Data Modeling with Cassandra
A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analysis team is particularly interested in understanding what songs users are listening to. The data reside in a directory of CSV files (event_data).

The purpose of the project is to create an Apache Cassandra database which can create queries on song play data to answer the questions given to by the analytics team. This project aims to create an ETL pipeline that transfers data from a set of CSV files within a directory to create a streamlined CSV file to model and insert data into Apache Cassandra tables.

## Installing Cassandra using Docker image

Follow the instructions to install and start Apache Cassandra database using Docker image.

1. Install and run [Docker Desktop](https://www.docker.com/products/docker-desktop/).

2. Pull the docker image. For the latest image, use:

```bash
docker pull cassandra:latest
```


3. Start Cassandra with a docker run command:

```bash
docker run --name cass_cluster -p 9042:9042 cassandra:latest
```

- `--name` option will be the name of the Cassandra cluster created.
- `-p` option is to expose your Cassandra Docker container port to localhost (Cassandra will be accessible on localhost:9042)

4. To test, start the CQL shell, cqlsh to interact with the Cassandra node created:

```bash
docker exec -it cass_cluster cqlsh
```