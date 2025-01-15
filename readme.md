# Spring Security Web Application

This project demonstrates how to secure a Spring MVC web application using Spring Security. It implements basic authentication and authorization features with a login form backed by an in-memory user store.

## Features

- Secured web application with Spring Security
- Login form authentication
- Public home page and secured greeting page
- User session management with logout functionality
- In-memory user store with configurable credentials

## Prerequisites

- Java 17 or later
- Gradle 7.5+ or Maven 3.5+
- Your favorite IDE (Spring Tool Suite, IntelliJ IDEA, or VSCode)

## Getting Started

### Clone the Repository

```bash
git clone https://github.com/alexketh/securing-web
cd securing-web
```

### Build and Run

With Gradle:
```bash
./gradlew bootRun
```
Or build the JAR file and run:
```bash
./gradlew build
java -jar build/libs/gs-securing-web-0.1.0.jar
```

With Maven:
```bash
./mvnw spring-boot:run
```
Or build the JAR file and run:
```bash
./mvnw clean package
java -jar target/gs-securing-web-0.1.0.jar
```

### Access the Application

Navigate to `http://localhost:8080` in your web browser.

## Project Structure

- `src/main/java/com/example/securing_web/`
  - `SecuringWebApplication.java`: Main application class
  - `MvcConfig.java`: MVC configuration
  - `WebSecurityConfig.java`: Security configuration

- `src/main/resources/templates/`
  - `home.html`: Public home page
  - `hello.html`: Secured greeting page
  - `login.html`: Custom login page

## Security Configuration

The application security is configured in `WebSecurityConfig.java`:
- Public access to `/` and `/home`
- Secured access to all other endpoints
- Custom login page at `/login`
- Default user credentials (username: "user", password: "password")

## Built With

- Spring Boot
- Spring Security
- Spring MVC
- Thymeleaf
- Gradle/Maven

## License

This project is released under the ASLv2 license.

## Acknowledgments

Based on the [Spring Security Web Application](https://spring.io/guides/gs/securing-web/) guide from Spring.io.
