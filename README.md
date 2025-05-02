# AdInsight – Scalable Ad Performance Analyzer

AdInsight is a mock advertising analytics platform designed to demonstrate scalable system design, data-driven decision-making, and modern software engineering practices. It simulates ad campaign management, real-time event ingestion, and analytics reporting.

---

## 📐 System Architecture

![System Design](./adinsight_system_design.png)

---

## 🧩 Features

- **Campaign Management API**: Create, update, and delete ad campaigns.
- **Event Ingestion System**: Collect ad impressions and clicks via APIs or queues.
- **Analytics Engine**: Aggregate daily metrics such as impressions, clicks, CTR, and cost-per-click.
- **Insights Module**: Recommend keyword optimizations based on performance.
- **Authentication Layer**: Secured endpoints with JWT (Spring Security).
- **Monitoring and Metrics**: Observability via Prometheus and Grafana.
- **(Optional)** React.js dashboard to visualize reports.

---

## 🔧 Tech Stack

| Category          | Technology                            |
|-------------------|----------------------------------------|
| Backend           | Java 17, Spring Boot, Spring Data JPA  |
| Data Ingestion    | Kafka / RabbitMQ                      |
| Database          | PostgreSQL, BigQuery (mocked)         |
| CI/CD             | GitHub Actions / Jenkins              |
| Monitoring        | Micrometer, Prometheus, Grafana       |
| Frontend (Opt.)   | React.js / Angular                    |
| Containerization  | Docker, Kubernetes                    |
| Testing           | JUnit 5, Mockito                      |

---

## 📁 Repository Structure

adinsight/
├── api-gateway/ # Gateway and routing
├── campaign-service/ # Campaign CRUD microservice
├── ingestion-service/ # Event ingestion via queue
├── analytics-service/ # Analytics & reporting logic
├── common-lib/ # Shared DTOs and utils
├── frontend/ # (Optional) React.js dashboard
├── docker-compose.yml # For local orchestration
└── README.md
