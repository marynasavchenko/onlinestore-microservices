## **Online store**

Online store is a microservices application. It contains of:

1. A customer service - manages customer data
2. A configuration service - manages a services configuration information
3. A Postgres SQL database

## **Building**

1. To compile source code and build Docker images for all services:
```
mvn clean package docker:build
```

## **Running**

1. To start all services in Docker containers with docker-compose:
```
docker-compose –f docker/common/docker-compose.yml up
```

## **Running the tests**

1.To run tests for all services via Maven:
```
mvn clean test
```

## **Technology stack**

* Java 8
* Spring Boot 2
* Spring Cloud
* Spring Data
* Postgres SQL

* jUnit 4
* Mockito

* Maven
* Docker