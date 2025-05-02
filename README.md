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
### Gateway and routing
├── api-gateway/
### Campaign CRUD microservice
├── campaign-service/ 
### Event ingestion via queue
├── ingestion-service/ 
### Analytics & reporting logic
├── analytics-service/ 
### Shared DTOs and utils
├── common-lib/ 
### (Optional) React.js dashboard
├── frontend/ 
### For local orchestration
├── docker-compose.yml

└── README.md


---

## 📊 Sample REST API

**POST /campaigns**
```json
{
  "name": "Eid Sale",
  "budget": 500,
  "startDate": "2025-10-10",
  "endDate": "2025-10-20",
  "keywords": ["discount", "sale", "eid"]
}
```

**POST /events/click**

```json

{
"campaignId": 123,
"timestamp": "2025-10-11T12:00:00Z",
"userId": "user-456"
}
```

**GET /analytics/daily-report?campaignId=123**

```json

{
"impressions": 800,
"clicks": 120,
"ctr": 15,
"costPerClick": 0.42
}
```


## 📈 Metrics Tracked
Impressions & Clicks

Click-Through Rate (CTR)

Cost Per Click (CPC)

Budget Utilization

Optimization Suggestions

## 📊 Sample Dashboards
Campaign overview with CTR trends

Budget burn-down charts

Keyword performance reports

🚀 How to Run Locally

`` bash
# Spin up services
docker-compose up --build
# Access services
# Campaign API: http://localhost:8081
# Analytics API: http://localhost:8082
# RabbitMQ Dashboard: http://localhost:15672
# Grafana: http://localhost:3000
``
# 📜 License
MIT License

