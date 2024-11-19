# Exception Logging Library

This library for Spring Boot applications captures and logs any exceptions thrown within the application. It stores these logs in a database and provides an API to retrieve the logs in a structured JSON format. Each log entry includes detailed information such as the type of exception, the error message, the stack trace, and the source class and method where the exception occurred and etc.

## Features
- Logs exception details such as type, message, stack trace, and source.
- Stores logs in a MongoDB database.
- Exposes an API to retrieve logs in JSON format.
- Easily integrates with existing Spring Boot applications.

## Requirements
- Java 17 or later
- Spring Boot 2.x or later
- MongoDB (for storing error logs)
- Spring Data MongoDB

## Installation

# ExceptionLogger Integration Guide

## Steps for Integration

### 1. Download the JAR File

1. Download the `ExceptionHandler-0.0.1-SNAPSHOT.jar` file.
2. Place it in the `libs` folder under your project's root directory. If the `libs` folder doesn't exist, create one.

### 2. Add the JAR File to `pom.xml`

To include the local JAR file, update your `pom.xml` file as follows:

1. Open `pom.xml`.
2. Add the following dependency inside the `<dependencies>` section:

```xml
<dependencies>    
    <dependency>
        <groupId>com.ExceptionLogger</groupId>
        <artifactId>ExceptionHandler</artifactId>
        <version>0.0.1-SNAPSHOT</version>
    </dependency>
</dependencies>

```
### 3. Add MongoDB connection URL in your Spring Boot application:
 1. Open `application.properties`.
 2. Add the MongoDB connection details: 
   ```xml
spring.data.mongodb.uri=mongodb://localhost:27017/exception_logger
```
