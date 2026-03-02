# 🛒 OrderStack – E-Commerce Product Management System

## 📘 Executive Summary
**OrderStack** is a production-oriented backend system designed to power modern e-commerce platforms. Built using **Spring Boot 3** and **PostgreSQL**, it provides a comprehensive and scalable REST API for managing product data, digital assets, and search functionality.

The application follows enterprise-grade architectural principles with a strong emphasis on:
* Clean layered architecture
* Performance and scalability
* Maintainability and modular design
* Secure API development standards

Although this repository primarily focuses on the Product Management module, the architecture is designed to integrate seamlessly with Spring Security (JWT, RBAC) and Spring AOP for authentication, authorization, logging, and cross-cutting concerns.

---

## 📑 Table of Contents
- [Project Objective](#project-objective)
- [Features](#features)
  - [User Module](#user-module)
  - [Functional Features](#functional-features)
- [Technologies Used](#technologies-used)
- [Dependencies Used](#dependencies-used)
- [System Architecture](#system-architecture)
- [Security & Cross-Cutting Concerns](#security--cross-cutting-concerns)
- [API Specification](#api-specification)
- [Installation](#installation)
  - [Backend Installation with IntelliJ IDEA](#backend-installation-with-intellij-idea)
  - [Frontend Installation With VS Code](#frontend-installation-with-vs-code)
- [Folder Structure (Backend)](#folder-structure-backend)

---

## 🎯 Project Objective
To design and implement a high-performance **Product Management backend system** that serves as the core foundation of a scalable and secure e-commerce platform.

The system enables:
* Efficient product lifecycle management
* Structured relational data persistence
* Optimized keyword-based search
* RESTful API exposure aligned with industry standards
* Seamless frontend integration

---

## 🔧 Features

### User Module
* Manage product creation, updates, and deletion
* Retrieve and display product details
* Fetch associated product images

### Functional Features
* Full product lifecycle management (CRUD operations)
* Keyword-based search functionality
* Image upload and retrieval support
* Cross-Origin frontend integration (CORS enabled)
* Structured REST API design

---

## 💡 Technologies Used

| Component               | Technology                     |
| ----------------------- | ------------------------------ |
| **Backend** | Spring Boot 3.3.3              |
| **ORM** | Spring Data JPA, Hibernate ORM |
| **Database** | PostgreSQL                     |
| **Security (Extensible)**| Spring Security, JWT, RBAC     |
| **Cross-Cutting Layer** | Spring AOP                     |
| **Frontend (optional)** | React.js                       |
| **Build Tool** | Apache Maven                   |
| **Runtime** | Java 21                        |
| **Tools** | Project Lombok, Postman        |

---

## 📦 Dependencies Used
The following dependencies are included in the project as per the `pom.xml`:

| Dependency Group             | Artifact                       | Scope     |
| ---------------------------- | ------------------------------ | --------- |
| `org.springframework.boot`   | `spring-boot-starter-web`      | compile   |
| `org.springframework.boot`   | `spring-boot-starter-data-jpa` | compile   |
| `org.springframework.boot`   | `spring-boot-starter-test`     | test      |
| `org.postgresql`             | `postgresql`                   | runtime   |
| `org.projectlombok`          | `lombok`                       | optional  |

---

## 🧱 System Architecture
The system follows a multi-layered monolithic architecture adhering to enterprise Java best practices:

1. **Presentation Layer** – REST controllers managing HTTP requests and responses.
2. **Service Layer** – Business logic components encapsulating core operations.
3. **Data Access Layer** – Spring Data JPA repositories handling database interactions.
4. **Entity Layer** – Java domain models mapped to relational database tables.

This layered separation ensures scalability, clean code organization, and long-term maintainability.

---

## 🔐 Security & Cross-Cutting Concerns
The architecture is designed to support enterprise-grade enhancements including:

* Stateless authentication using JWT
* Role-Based Access Control (RBAC)
* Endpoint protection via Spring Security
* Centralized logging and monitoring using Spring AOP
* Global exception handling strategy

These capabilities are modular and can be integrated seamlessly into the existing structure.

---

## 🔗 API Specification

| Endpoint                          | Method | Description                 | Status Codes |
| --------------------------------- | ------ | --------------------------- | ------------ |
| `/api/products`                   | GET    | Retrieve all products       | 200          |
| `/api/product/{id}`               | GET    | Get product by ID           | 200, 404     |
| `/api/product/{productId}/image`  | GET    | Retrieve product image      | 200, 404     |
| `/api/product`                    | POST   | Add a new product           | 201, 500     |
| `/api/product/{id}`               | PUT    | Update existing product     | 200, 500     |
| `/api/product/{id}`               | DELETE | Delete product              | 200, 404     |
| `/api/product/search?keyword=xyz` | GET    | Search product by keyword   | 200          |

---

## 🛠 Installation

### Backend Installation with IntelliJ IDEA
1. Open IntelliJ IDEA and select **Open Project**.
2. Navigate to the `SpringEcom` directory.
3. Ensure **Java 21** is installed and configured.
4. Click **Run > Run 'SpringEcomApplication'**.

### Frontend Installation With VS Code
1. Navigate to the frontend folder (React.js project).
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.

---

## 📂 Folder Structure (Backend)

```plaintext
com.telusko.springecom
├── controller                # REST controllers (ProductController)
├── service                   # Service layer interfaces and implementations
├── repository                # Spring Data JPA repositories
├── model                     # Entity classes (Product)
└── SpringEcomApplication     # Main application class
