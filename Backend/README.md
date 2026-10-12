# Smart Billing and Retailing System — Backend

## Overview

The Smart Billing and Retailing System is a backend application developed using Spring Boot and MySQL. It provides REST APIs for managing products, customers, billing operations, inventory, and sales history.

The application follows a layered architecture to separate business logic, database operations, and HTTP request handling.

## Technologies Used

- Java 21
- Spring Boot
- Spring Data JPA
- Hibernate ORM
- MySQL
- Maven
- REST APIs

## Features

### 1. Product Management
- Add new products.
- Retrieve product information.
- Update product details and prices.
- Delete products.
- Track available stock quantities.

### 2. Customer Management
- Register new customers.
- Retrieve customer information.
- Update customer details.
- Delete customer records.

### 3. Billing Management
- Create customer bills.
- Calculate bill totals.
- Validate product availability and requested quantities.
- Update inventory after successful sales.
- Store billing records in the database.

### 4. Sales History
- Retrieve previous sales records.
- View billing information.
- Retrieve individual sales records by ID.

## Backend Architecture

The backend follows a layered architecture.

```text
Backend
   |
   v
Controller Layer
   |
   v
Service Layer
   |
   v
Repository Layer
   |
   v
Entity Layer
   |
   v
MySQL Database
```

### Entity Layer
Defines the database entities used by the application, including Product, Customer, and Bill.

### Repository Layer
Uses Spring Data JPA to perform database operations such as saving, retrieving, updating, and deleting records.

### Service Layer
Contains business logic for product management, customer management, billing, and sales operations.

### Controller Layer
Handles HTTP requests and exposes REST API endpoints to the frontend.

## API Endpoints

### Product APIs

| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/products` | Retrieve all products |
| POST | `/api/products` | Add a product |
| PUT | `/api/products/{id}` | Update a product |
| DELETE | `/api/products/{id}` | Delete a product |

### Customer APIs

| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/customers` | Retrieve all customers |
| POST | `/api/customers` | Add a customer |
| PUT | `/api/customers/{id}` | Update a customer |
| DELETE | `/api/customers/{id}` | Delete a customer |

### Billing APIs

| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/billing` | Retrieve all bills |
| POST | `/api/billing` | Create a bill |

### Sales APIs

| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/sales` | Retrieve sales history |
| GET | `/api/sales/{id}` | Retrieve a sale by ID |

## Database

The application uses MySQL to store product, customer, and billing information.

**Database name:** `retailbilling`

Spring Data JPA and Hibernate manage persistence between Java entities and database tables.

Configure the database connection in `application.properties`.

Example configuration:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/retailbilling
spring.datasource.username=${DB_USERNAME}
spring.datasource.password=${DB_PASSWORD}

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

Set the `DB_USERNAME` and `DB_PASSWORD` environment variables to your local MySQL credentials before running the application.

Do not upload database passwords or other secrets to GitHub.

## Prerequisites

- Java 21
- MySQL Server
- Maven or the included Maven Wrapper

## Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/rupasric07-design/SmartBillingAndRetailing.git
```

### 2. Navigate to the Backend Project

```bash
cd SmartBillingAndRetailing/backend/retailbilling
```

### 3. Create the Database

Open MySQL and execute:

```sql
CREATE DATABASE retailbilling;
```

### 4. Configure Database Credentials

Configure your database URL, username, and password in `src/main/resources/application.properties`, or provide the required environment variables.

### 5. Run the Application on Windows

```cmd
mvnw.cmd spring-boot:run
```

Alternatively, if Maven is installed:

```bash
mvn spring-boot:run
```

### 6. Verify the Backend

The application should start on port `8080`, unless a different port is configured.

Base address:

```text
http://localhost:8080
```

For example, to retrieve products, use:

```text
http://localhost:8080/api/products
```

The endpoint will return data only when the backend is running and the database and API configuration are correct.

## Frontend Integration

The backend provides REST APIs that can be consumed by the React frontend.

Frontend development address:

```text
http://localhost:5173
```

Backend development address:

```text
http://localhost:8080
```

Ensure that CORS is configured correctly if the frontend and backend run on different origins.

## Future Enhancements

- Authentication and role-based access control.
- Low-stock alerts.
- Advanced sales reports.
- Invoice generation and PDF export.
- Improved error handling and validation.
- Automated unit and integration tests.

## Author

Developed as an educational project for retail inventory and billing management.

## License

This project is intended for educational and demonstration purposes.
