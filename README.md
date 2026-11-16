# NexaCommerce 🚀
### Cloud-Native E-Commerce Platform | Microservices Architecture

NexaCommerce is a cloud-native e-commerce platform built using a distributed microservices architecture. It consists of 13 Spring Boot backend microservices, a Next.js frontend, an API Gateway, and supporting infrastructure.

The platform is designed to demonstrate scalable backend development, distributed system communication, authentication, containerization, and Kubernetes-based deployment.

> **Project origin:** This project is adapted from [ecommerce-microservices](https://github.com/hoangtien2k3/ecommerce-microservices) by Hoàng Anh Tiến. It is being customized and extended as NexaCommerce. Original MIT license and copyright notices are retained.

---

## 🛠️ Technology Stack

| Category | Technologies |
|---|---|
| Backend | Java 21, Spring Boot 3 |
| Security | Spring Security, Keycloak, OAuth2, JWT |
| Frontend | Next.js 16, React 19 |
| Styling | Tailwind CSS 4 |
| Database | PostgreSQL 16 |
| Caching | Redis 7 |
| Search | Elasticsearch 8 |
| Messaging | Apache Kafka 3.9 |
| API Gateway | Apache APISIX 3.9 |
| Object Storage | RustFS (S3-compatible) |
| Containerization | Docker, Docker Compose |
| Orchestration | Kubernetes, k3d |
| CI/CD | GitHub Actions |
| Monitoring | Prometheus, Micrometer |
| Build Tool | Maven |

---

## 🏗️ Architecture

NexaCommerce follows a microservices architecture where each service handles a specific business responsibility.

### Backend Microservices

| Service | Responsibility |
|---|---|
| Auth Service | Authentication and authorization |
| Product Service | Product management |
| Inventory Service | Stock management |
| Order Service | Order processing |
| Payment Service | Payment processing |
| Shipping Service | Shipping management |
| Favourite Service | Customer favourites |
| Rating Service | Product ratings |
| Search Service | Product search |
| Promotion Service | Discounts and promotions |
| Notification Service | Customer notifications |
| Media Service | Media and file management |
| Tax Service | Tax management |

### Infrastructure

- Apache APISIX – API Gateway
- Keycloak – Identity and access management
- Apache Kafka – Asynchronous messaging
- Redis – Caching
- PostgreSQL – Relational data storage
- Elasticsearch – Search and indexing
- RustFS – Object storage

---

## 📁 Project Structure

```text
NexaCommerce/
├── auth-service/
├── common-lib/
│   ├── common-core/
│   ├── common-spring/
│   ├── common-security/
│   ├── common-keycloak/
│   ├── common-kafka/
│   ├── common-logging/
│   └── common-storage/
├── deploy/
│   └── apisix/
├── docker/
├── favourite-service/
├── frontend/
├── inventory-service/
├── media-service/
├── notification-service/
├── order-service/
├── payment-service/
├── product-service/
├── promotion-service/
├── rating-service/
├── search-service/
├── shipping-service/
├── tax-service/
├── k8s/
├── docker-compose.yml
├── pom.xml
├── Makefile
└── start-ecommerce.sh
```

---

## ⚙️ Getting Started

### Prerequisites

Make sure you have installed:

- Java 21
- Maven
- Node.js
- Docker Desktop
- kubectl
- Git

### Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd nexa-commerce-microservices
```

### Run with Docker Compose

```bash
docker compose up --build -d
```

### Run with Kubernetes (k3d)

```bash
bash start-ecommerce.sh
```

Check the deployment status:

```bash
kubectl get pods -n ecommerce
```

**Note:** Configure the required environment variables and review the deployment scripts before running the application.

---

## 📊 Monitoring and Observability

The original architecture includes:

- Spring Boot Actuator health endpoints
- Prometheus metrics
- Micrometer instrumentation
- Distributed correlation IDs
- APISIX metrics

---

## 🎯 Project Objectives

- Understand microservices architecture and service boundaries.
- Implement distributed backend applications.
- Explore asynchronous communication using Kafka.
- Work with API Gateway patterns.
- Implement authentication and authorization.
- Manage application infrastructure using Docker.
- Deploy distributed services using Kubernetes.
- Explore monitoring and observability.

---

## 🛣️ Development Roadmap

- [ ] Customize the frontend and application branding.
- [ ] Understand and customize individual microservices.
- [ ] Implement additional business features.
- [ ] Improve service-to-service communication.
- [ ] Add integration and unit tests.
- [ ] Configure CI/CD pipelines.
- [ ] Improve monitoring and deployment workflows.

