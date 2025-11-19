# Spring Boot application demo

This is a demo application with Vaadin and Spring Boot.

## Tech Stack

- Java 21
- Apache Maven 3.9.11
- Spring Boot 3 with Spring MVC
- Vaadin 24.9
- Junit 5.13
- AssertJ: Fluent assertions, please use it instead of JUnit assertions.

## Project structure

- base package: `org.mvnsearch`
- Vaadin base component package: `org.mvnsearch.base`
- Vaadin application package: `org.mvnsearch.demo`

## Database

- H2 in-memory database for development
- JPA entities use `@GeneratedValue(strategy = GenerationType.SEQUENCE)`
- Entity equality based on ID (see Task.equals/hashCode pattern)
- ORM: Spring Data JPA

## Build and run

The project uses Maven as the build tool and [just](https://github.com/casey/just) as the task runner.

- Build: `mvn -DskipTests package`
- Run: `mvn -DskipTests spring-boot:run`
- Release: `mvn -Pproduction -DskipTests clean package`

## Java Guide line

- Use jspecify to annotate nullable and non-nullable types: `org.jspecify.annotations.NonNull` and
  `org.jspecify.annotations.Nullable`
- Use slf4j for logging

## Configuration

The project uses `src/main/resources/application.properties` as the configuration file.

