## **Online store**

Online store is microservices application. It consists of backend services:

1. Order service - manages orders
2. Customer service - manages customer data (name, address, etc.)
3. Configuration service - manages services configuration information
4. Spring cloud eureka service - service registry
5. Zuul service - services gateway
6. Alternative routes service - has a database record for the customer service that can be used for redirection to different versions of the service

Order service, Customer service and Alternative routes service have their own REST APIs and their own private datastores.
Each service has its own source code repository.

## **Building**

To compile source code and build Docker images for all services:
```
mvn clean package docker:build
```

## **Running**

To start all services in Docker containers with docker-compose:
```
docker-compose –f docker/common/docker-compose.yml up
```

## **Running the tests**

To run tests for all services via Maven:
```
mvn clean test
```

## **Technology stack**

* Java
* Spring Boot
* Spring Cloud
* Spring Data
* Postgres SQL

* jUnit
* Mockito

* Maven
* Docker