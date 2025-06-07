# 🛒 E-Commerce Microservices Platform

A scalable and event-driven microservices-based e-commerce application built with Spring Boot. The project is modularized into Product, Order, and Inventory services, with seamless inter-service communication and robust infrastructure features.

## 🔧 Tech Stack

- **Language & Frameworks**: Java, Spring Boot, Spring Security, Hibernate
- **Messaging & Event-Driven Architecture**: Kafka, RabbitMQ
- **Authentication & Authorization**: Keycloak (Role-Based Access Control)
- **Service Discovery**: Eureka
- **Logging & Monitoring**: Elasticsearch, Kibana
- **Containerization**: Docker
- **Database**: SQL

---

## 📦 Microservices Overview

### 1. **Product Service**
- Manages product catalog (add, update, view products).
- Exposes RESTful APIs for CRUD operations.
- Communicates with Order Service to validate product details.

### 2. **Order Service**
- Handles order placement, status tracking, and order history.
- Listens to Kafka/RabbitMQ events to update inventory post-order.
- Publishes events for successful order placements.

### 3. **Inventory Service**
- Maintains product stock information.
- Subscribes to order events to decrement stock.
- Publishes out-of-stock alerts via messaging queues.

---

## 🔐 Security

- **Keycloak** for OAuth2-based authentication and authorization.
- Role-based access implemented for admin and user privileges.
- Secured APIs using JWT tokens.

---

## 🔄 Real-Time Communication

- **Apache Kafka** and **RabbitMQ** handle asynchronous communication.
- Ensures decoupled, fault-tolerant messaging between services.
- Enables smooth order processing and inventory updates.

---

## 🔍 Observability

- **Elasticsearch + Kibana** used for centralized logging and monitoring.
- Logs are collected in real time for all services to trace issues effectively.

---

## 🐳 Deployment

- Each microservice and its dependencies are containerized using **Docker**.
- Docker Compose can be used to bring up the full infrastructure.

```bash
docker-compose up --build
📁 Project Structure
bash
Copy
Edit
ecommerce-platform/
├── product-service/
├── order-service/
├── inventory-service/
├── config-server/ (Optional)
├── discovery-server/ (Eureka)
├── api-gateway/ (Optional)
├── docker-compose.yml
└── README.md
🚀 Getting Started
Prerequisites:
Java 17+

Maven

Docker & Docker Compose

Kafka & RabbitMQ running locally or via Docker

Steps:
Clone the repository:

bash
Copy
Edit
git clone https://github.com/yourusername/ecommerce-platform.git
cd ecommerce-platform
Build services:

bash
Copy
Edit
mvn clean install
Run with Docker Compose:

bash
Copy
Edit
docker-compose up --build
Access Keycloak at http://localhost:8080/auth
Access services via Eureka or API Gateway

✍️ Author
Kishlay Raj
Java Backend Developer | Passionate about scalable microservices
📫 LinkedIn | ✉️ kishlayraj@example.com

📄 License
This project is licensed under the MIT License - see the LICENSE file for details.

yaml
Copy
Edit

---
---

Let me know if you want a Docker Compose file, API endpoint documentation, or setup instructions for Keycloak too!


Let me know if you want a Docker Compose file, API endpoint documentation, or setup instructions for Keycloak too!








