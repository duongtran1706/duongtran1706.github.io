# Yêu cầu
- [Yêu cầu](#yêu-cầu)
  - [Hệ điều hành:](#hệ-điều-hành)
  - [Yêu cầu liên quan](#yêu-cầu-liên-quan)
    - [Nodejs](#nodejs)
    - [Go lang](#go-lang)
    - [Protoc](#protoc)
    - [Docker - docker compose](#docker---docker-compose)
    - [Kafka](#kafka)
    - [ActiveMq](#activemq)
    - [Jaeger](#jaeger)
    - [Elasticsearch](#elasticsearch)
    - [Fluentd](#fluentd)
  - [Concepts](#concepts)
  - [Tech stack](#tech-stack)
  - [IP Access (môi trường UAT)](#ip-access-môi-trường-uat)
  - [Domain](#domain)
## Hệ điều hành: 
- Thuộc hệ điều hành [Debian](https://distrowatch.com/), Apple

## Yêu cầu liên quan
  ### Nodejs
   - Learning [nodejs](https://nodejs.org/en/docs/)
  ### Go lang 
   - Learning [Go lang](https://go.dev/doc/install)
  ### Protoc 
  - Learning [protoc]( http://google.github.io/proto-lens/installing-protoc.html)

  - Install related protoc packages (https://github.com/grpc-ecosystem/grpc-gateway)
    
  ### Docker - docker compose
   - Installing [docker](https://docs.docker.com/desktop/install/ubuntu/)
   - Learning docker [get started](https://docs.docker.com/get-started/) 
   - (Optional) Update docker-compose.yml if you want to start 
   - Kafka and database in the same docker network with your application.
   - Build docker images: docker-compose build
   - Start the app by using Docker: docker-compose up -d
  ### Kafka 
   - Learning [Kafka](https://kafka.apache.org/documentation/#introduction)
  ### ActiveMq
   - Learning [activemq](https://activemq.apache.org/getting-started)
  ### Jaeger
  - Learning [jaeger](https://www.jaegertracing.io/docs/1.38/)
  ### Elasticsearch
  - Learning [Elasticsearch](  https://www.elastic.co/guide/index.html)
  ### Fluentd 
  - Learning [Fluentd](https://www.fluentd.org/architecture)
  
  ## Concepts
- Clean Architecture
- SOLID Principles

## Tech stack
- NodeJS (Javascript, Typescript)
- Docker
- MySQL (sequelize)
- MongoDB (mongoose)
- ActiveMQ (@stomp/stompjs)
- KAFKA producer (node-rdkafka)
- KAFKA consumer (@finviet-promotion/rd-kafka-node)
- Jaeger Tracing (@opentelemetry)
- gRPC (@grpc/grpc-js)
- Redis (redis)
- Prometheus (prom-client)
- Env: Linux
<!-- - 
##  IP Access (môi trường UAT)
- 10.12.23.40:31333 (KAFKA uat)
- 10.12.50.7:3308 (ecomv2 DB uat)
- 10.12.19.8:27017 (MongoDB Master-data uat)
- 10.12.23.40:32018 (MongoDB Promotion uat)
- 10.12.23.42:30433 (Jaeger Trace uat)
- 10.12.23.40:32012 (Consul uat)
- 10.11.23.60:30433 (Jaeger Trace Product)
- 10.11.23.60:32018 (Portal data sync Product)

## Domain

https://promotion-uat.finviet.com.vn/
Account: 0332901435
Password: Hello

https://ecom-uat.finviet.com.vn/
Account: admin@gmail.com
Password: admin@fv123

https://cms-uat-ecom.finviet.com.vn
Account: 0912428128
Password: 123456

https://promotion-data-sync-uat.finviet.com.vn/

10.11.23.60:32018 (portal data sync)
 -->
