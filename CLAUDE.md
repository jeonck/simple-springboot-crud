# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a simple Spring Boot CRUD application project. The repository is currently empty and ready for Spring Boot application development.

## Development Commands

When the project is set up with Maven:
```bash
# Build the application
mvn clean compile

# Run tests
mvn test

# Run the application
mvn spring-boot:run

# Package the application
mvn clean package

# Run a single test class
mvn test -Dtest=ClassName

# Run a single test method
mvn test -Dtest=ClassName#methodName
```

When the project is set up with Gradle:
```bash
# Build the application
./gradlew build

# Run tests
./gradlew test

# Run the application
./gradlew bootRun

# Run a single test class
./gradlew test --tests ClassName

# Run a single test method
./gradlew test --tests ClassName.methodName
```

## Expected Architecture

For a Spring Boot CRUD application, the typical structure will be:

- **Controller Layer**: REST endpoints handling HTTP requests
- **Service Layer**: Business logic implementation
- **Repository Layer**: Data access using Spring Data JPA
- **Entity/Model Layer**: JPA entities representing database tables
- **Configuration**: Application properties and configuration classes

## Key Dependencies Expected

- Spring Boot Starter Web
- Spring Boot Starter Data JPA
- Database driver (H2, MySQL, PostgreSQL, etc.)
- Spring Boot Starter Test
- Validation dependencies for request validation

## Database Configuration

Application will likely use `application.properties` or `application.yml` for database configuration. Common patterns:
- Development: H2 in-memory database
- Production: External database (MySQL, PostgreSQL)

## Testing Strategy

- Unit tests for service layer logic
- Integration tests for repository layer
- Web layer tests for controllers using `@WebMvcTest`
- Full integration tests using `@SpringBootTest`