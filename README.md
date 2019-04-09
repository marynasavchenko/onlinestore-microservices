## **Online store**

Online store is microservices-based e-commerce application that takes orders from customers.

It consists of several backend microservices:

1. Order service - manages orders
2. Customer service - manages customer data (name, address, etc.)
3. Configuration service - manages services configuration data
4. Spring cloud eureka service - special service registry that is used for locating services
5. Zuul gateway service - provides dynamic routing, monitoring, resiliency, security for entire application
6. Alternative routes service - has a database of route records for the customer service that can be used for redirection to different versions of the service

Order service, Customer service and Alternative routes service have their own REST APIs and their own private datastores.
Each service has its own source code repository.

## **Technology stack**

* Java 8
* Spring Boot 2
* Spring Cloud 2
* Spring Data 2
* Postgres SQL

* jUnit 4
* Mockito

* Maven
* Docker

* Netflix Zuul
* Netflix Eureka

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