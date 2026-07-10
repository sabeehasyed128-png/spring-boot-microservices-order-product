# spring-boot-microservices-order-product
Order and Product Microservices built using Spring Boot, Spring Data JPA, REST APIs, H2 Database, and RestTemplate communication.
# Spring Boot Order & Product Microservices

## Overview

This project demonstrates a simple Microservices Architecture using Spring Boot.

The application consists of:

- Product Service
- Order Service

The Order Service communicates with the Product Service using RestTemplate and calculates the total order amount.

---

## Technologies Used

- Java 17
- Spring Boot
- Spring Data JPA
- H2 Database
- Maven
- Lombok
- REST APIs
- RestTemplate

---

## Project Architecture

Product Service
|
| REST API
|
Order Service

---

## Product Service

### Features

- Add Product
- View Product
- Store Product Details
- H2 Database Integration

### Product Entity

| Field | Type |
|---------|---------|
| id | Long |
| name | String |
| price | Double |

---

## Order Service

### Features

- Create Orders
- Fetch Product Details
- Calculate Total Amount
- Store Order Details

### Order Entity

| Field | Type |
|---------|---------|
| id | Long |
| productId | Long |
| quantity | Integer |
| total | Double |

---

## API Endpoints

### Product Service

#### Get All Products

GET

/api/products

#### Get Product By Id

GET

/api/products/{id}

#### Add Product

POST

/api/products

Sample Request

```json
{
  "name": "Laptop",
  "price": 50000
}
```

---

### Order Service

#### Get All Orders

GET

/api/orders

#### Get Order By Id

GET

/api/orders/{id}

#### Create Order

POST

/api/orders

Sample Request

```json
{
  "productId": 1,
  "quantity": 3
}
```

Sample Response

```json
{
  "id": 1,
  "productId": 1,
  "productName": "Laptop",
  "price": 50000,
  "quantity": 3,
  "total": 150000
}
```

---

## Database

### Product Database

H2 Console

http://localhost:2007/h2-console

### Order Database

H2 Console

http://localhost:2008/h2-console

---

## How to Run

### Clone Repository

```bash
git clone https://github.com/sabeehasyed128-png/springboot-microservices-order-product.git
```

### Run Product Service

```bash
mvn spring-boot:run
```

### Run Order Service

```bash
mvn spring-boot:run
```

---

## Future Enhancements

- MySQL Integration
- OpenFeign Client
- Spring Cloud Gateway
- Eureka Service Discovery
- Docker Deployment
- Swagger Documentation

---

## Author

**Sabeeha Parveen**

B.Tech Artificial Intelligence & Data Science

Aspiring Java Full Stack Developer