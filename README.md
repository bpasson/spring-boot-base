Spring Boot Base ![License MIT](https://img.shields.io/badge/license-MIT-blue.svg)
=============

A base container simplifying the running of Spring Boot applications. [Dockerize](https://github.com/jwilder/dockerize) is used for starting the Java process.

Dockerize command line options can be specified using the the environment variable DOCKERIZE_OPTS.

### Example Usage

``` Dockerfile
FROM bpasson/spring-boot-base:8-jre

COPY ./app.jar /app/app.jar

CMD ["-jar","/app/app.jar"]
```
