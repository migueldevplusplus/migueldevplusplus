<div align="center">

# Miguel Mora

**Backend Developer — Java · Spring Boot · Python**

[![Email](https://img.shields.io/badge/Email-amvmiguelito@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:amvmiguelito@gmail.com)
[![Location](https://img.shields.io/badge/Puerto_Ordaz-Venezuela-FCE300?style=flat-square)](#)

</div>

---

## About

I build backends where the business rules actually matter — appointment scheduling with real conflict detection, pharmacy inventory with pgvector search, data pipelines that turn raw CSVs into something a manager can act on.

Computer Engineering student at UNEG. Currently focused on **Java + Spring Boot** with Clean Architecture, coming from a Python/FastAPI background.

- 🔭 Building **[ClinicBook](https://github.com/migueldevplusplus/clinic-book-app)** — a role-based medical scheduling API with JWT auth and computed slot availability
- 🌱 Going deeper into software architecture, testing strategy, and query optimization
- 💼 Also run a small SaaS: digital menu & ordering systems for local restaurants (2 paying clients)

---

## Tech Stack

**Languages**

![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)

**Backend**

![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white)
![Hibernate](https://img.shields.io/badge/Hibernate-59666C?style=flat-square&logo=hibernate&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white)

**Data & Infra**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Flyway](https://img.shields.io/badge/Flyway-CC0200?style=flat-square&logo=flyway&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

---

## Projects

### 🏥 ClinicBook API
**Java · Spring Boot 4 · PostgreSQL · Docker**

Medical appointment scheduling backend for small private clinics. Four roles with distinct permissions, stateless JWT auth, and an availability engine that computes free/busy slots on the fly from each doctor's weekly schedule minus what's already booked — no pre-generated slots table to keep in sync.

Built with Clean Architecture: the domain layer has zero framework imports, business rules live inside the domain models themselves (`Appointment.confirm()`, `.overlapsWith()`), and infrastructure implements interfaces the domain defines. Schema versioned with Flyway, containerized with Docker Compose.

[**→ Repository**](https://github.com/migueldevplusplus/clinic-book-app)

---

### 💊 FarmaHumana
**Python · FastAPI · SQLAlchemy 2.0 · PostgreSQL · pgvector**

Pharmacy digital ecosystem built as a team project — I served as **Data Coach**, leading the database architecture design and coordinating technical decisions across the team.

Designed the relational schema, defined the repository/mapper patterns the team followed, implemented pgvector with HNSW indexes for semantic product search, and set up Alembic migrations. Applied Clean Architecture and DDD principles across the data layer.

---

### 📊 Automated Weekly Sales Report
**Python · Pandas · OpenPyXL**

End-to-end pipeline that ingests raw sales CSVs, validates their structure, computes weekly KPIs with historical week-over-week comparisons, fills a styled Excel template, bundles it into a dated ZIP, and emails it to stakeholders.

A deliberate hybrid: Python handles computation and validation, Excel handles presentation — because the people receiving the report live in Excel, not in a dashboard.

[**→ Repository**](https://github.com/migueldevplusplus/automated-report)

---

### 📈 Superstore Sales & Operations Dashboard
**Excel · Data Analysis**

51,000+ transaction rows turned into an executive dashboard with dynamic slicers, profitability analysis by category and region, and shipping-efficiency insights.

Focused on the analysis itself, not just the visualization — which margins are actually being eaten by shipping costs, and where.

[**→ Repository**](https://github.com/migueldevplusplus/superstore-orders-analysis)

---

## Also

I build and sell **digital menu and ordering systems** for restaurants in Puerto Ordaz — currently 2 paying clients running the product live. Client repos are private, but happy to walk through the architecture on request.

---

<div align="center">

**Open to backend and data engineering opportunities.**

[![Email](https://img.shields.io/badge/Email-Say_hi-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:amvmiguelito@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/migueldevplusplus)

</div>
