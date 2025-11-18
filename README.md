# Vaadin Demo

A Java Web application demo project based on [Vaadin](https://vaadin.com/) and [Spring Boot](https://spring.io/projects/spring-boot). Demonstrates how to build modern enterprise-level Web applications using Vaadin.

## Tech Stack

- **Java**: 21
- **Spring Boot**: 3.5.7
- **Vaadin**: 24.9.3
- **Spring Data JPA**: Data access layer
- **H2 Database**: In-memory database (development environment)
- **Maven**: Build tool

## Project Structure

```
vaadin-demo/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── org/mvnsearch/...       # Java source code
│   │   └── resources/
│   │       └── application.properties
│   └── test/             # Test code
├── pom.xml               # Maven dependency configuration
└── README.md
```

## Features

- Vaadin component library
- Spring Boot integration
- Spring Data JPA
- H2 database support
- Reactive UI
- Server-side rendering
- Actuator monitoring endpoints

## Quick Start

### Prerequisites

- Java 21 or higher
- Maven 3.6+

### Installation and Running

```bash
# Build project
mvn clean package

# Run application
mvn spring-boot:run
# Or
java -jar target/vaadin-demo-1.0-SNAPSHOT.jar
```

The application will start at `http://localhost:8080`.

## Project Features

### Vaadin Framework

Vaadin is a server-driven Web framework:
- **Server-side Rendering**: UI generated on the server
- **Component Library**: Rich enterprise-level components
- **Type Safety**: Type-safe UI development in Java
- **Automatic Communication**: Automatic client-server communication handling

### Spring Boot Integration

- **Auto Configuration**: Vaadin Spring Boot Starter
- **Dependency Injection**: Spring DI container
- **Data Access**: Spring Data JPA
- **Monitoring**: Spring Boot Actuator

### View Development

Vaadin views are regular Java classes:

```java
@Route("")
public class MainView extends VerticalLayout {
    public MainView() {
        add(new H1("Welcome to Vaadin"));
        add(new Button("Click me", e -> {
            Notification.show("Button clicked!");
        }));
    }
}
```

## References

- [Vaadin Official Website](https://vaadin.com/)
- [Vaadin Documentation](https://vaadin.com/docs)
- [Vaadin Spring Boot Integration](https://vaadin.com/docs/latest/integrations/spring/overview)
- [Vaadin Components Documentation](https://vaadin.com/docs/latest/components)
