
# Product Management REST API

A RESTful Product Management API built using Java 17,
Spring Boot, Spring Data JPA, MySQL, and Swagger UI.

## Features

- Create products
- Retrieve all products
- Retrieve a product by ID
- Update product details
- Delete products
- Validate product inputs
- Handle errors with meaningful HTTP responses
- Test APIs using Swagger UI

## Technology Stack

- Java 17
- Spring Boot 3.5.6
- Spring Web
- Spring Data JPA
- MySQL
- Hibernate
- Maven


## Prerequisites

- JDK 17 or later
- MySQL Server
- Maven (optional if using Maven Wrapper)

## Database Setup

Create the database in MySQL:

    CREATE DATABASE product_management;

Configure your MySQL credentials in
src/main/resources/application.properties.

You can use the DB_USERNAME and DB_PASSWORD
environment variables to supply credentials.

## Run the Application

Using Maven:

    mvn clean package
    mvn spring-boot:run

Using the Maven Wrapper on Windows:

    mvnw.cmd spring-boot:run

Using the Maven Wrapper on Linux:

    ./mvnw spring-boot:run

## Swagger UI

After starting the application, visit:

http://localhost:8080/swagger-ui/index.html

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | /api/products | Create product |
| GET | /api/products | Get all products |
| GET | /api/products/{id} | Get product by ID |
| PUT | /api/products/{id} | Update product |
| DELETE | /api/products/{id} | Delete product |

## Example Request

POST /api/products

    {
      "name": "Keyboard",
      "price": 1499.00,
      "quantity": 10
    }

## Database Schema

Table: products

- id: BIGINT, primary key, auto-increment
- name: VARCHAR(100), not null
- price: DECIMAL(12,2), not null
- quantity: INT, not null

Hibernate creates or updates the table automatically
using the configured JPA schema setting.

## Error Handling

- 400 Bad Request: Invalid input
- 404 Not Found: Product does not exist
- 201 Created: Product successfully created
- 204 No Content: Product successfully deleted

## License

This project is intended for learning and portfolio use.
