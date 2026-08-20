<div align="center">

![Miguel Mora — Backend Developer](banner.svg)

[![Portfolio](https://img.shields.io/badge/Portfolio-migueldevplusplus.github.io-2496ED?style=flat-square&logo=googlechrome&logoColor=white)](https://migueldevplusplus.github.io)
[![Email](https://img.shields.io/badge/Email-amvmiguelito@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:amvmiguelito@gmail.com)

</div>

---

## About me

```java
public class Miguel {

    private final String role     = "Backend Developer";
    private final String based    = "Venezuela";
    private final String studying = "Software Engineering @ UNEG";

    public String howIWork() {
        return "Model the data first. Put the rules where they belong. Then build around it.";
    }

    public Map<String, String> currently() {
        return Map.of(
            "Clinic Book", "Scheduling API — Spring Boot 4, hexagonal architecture",
            "FarmaHumana", "Data Coach — database architecture for a pharmacy ecosystem",
            "Learning",    "Query optimization, testing strategy, distributed data"
        );
    }
}
```

I work on the part of a system that is expensive to get wrong: the schema and the business rules. Most bugs I have chased were not bad code — they were a data model that allowed something it never should have.

---

## 🏥 Clinic Book — main project

**Java 21 · Spring Boot 4 · PostgreSQL · Flyway · Docker · Testcontainers** · [**Repository →**](https://github.com/migueldevplusplus/clinic-book-app)

A medical appointment scheduling API with four roles, JWT authentication and an availability engine that derives free slots from each doctor's weekly schedule and consultation length — nothing is stored that can be computed.

Built with **ports and adapters**: the domain package imports nothing from Spring, JPA or the web, so the booking rules are tested in milliseconds without a database. What that architecture buys, concretely:

- The appointment lifecycle is a real **state machine** — `complete()` on a pending appointment throws no matter which endpoint asked
- Booking calls the same availability function the client uses, so **what you see and what you can book never disagree**
- Ownership is enforced beyond roles: having the `DOCTOR` role does not let you close someone else's appointment
- Schema ships as **versioned Flyway migrations**, replayed on an empty PostgreSQL container on every build

---

## Experience

### 🧬 Data Coach — FarmaHumana
**FastAPI · SQLAlchemy 2.0 · PostgreSQL · Alembic · Docker** · 3 months

A digital pharmacy ecosystem — e-commerce plus medication tracking — built for a real pharmacy as part of the Software Engineering programme at UNEG. I owned the database architecture for **both systems** and set the standards the rest of the team built against, coordinating a team of **~8 developers**.

Decisions I designed and defended:

- **Joined-table inheritance** for identity — `User → Customer, Employee, Doctor, Patient` — so one person is one identity, with role-specific data in its own table
- A **hierarchical catalogue**: active ingredient → medication → presentation → product variant, so pricing and stock live at the right level instead of being duplicated per SKU
- **`doctor_patient_links`** as the single source of truth for the doctor–patient relationship, rather than inferring it from prescriptions
- **`medication_possession_confirmations`** as the anchor that starts a treatment — a tracked plan begins when the patient actually holds the medication, not when it is prescribed
- A **Super-Admin approval flow** for patient accounts
- Team-wide conventions: one repository per aggregate root, soft deletes through `disabled_at`, and explicit `to_domain()` / `to_model()` mappers at the persistence boundary
- **Vector search with pgvector** and HNSW indexes

---

## Also

### 📊 [Automated Weekly Sales Report](https://github.com/migueldevplusplus/automated-report)
**Python · Pandas · OpenPyXL**

A pipeline that validates incoming CSVs, computes weekly KPIs against historical baselines, fills a styled Excel template, bundles the output into a dated ZIP and emails it to stakeholders. Python does the computation and validation; Excel does the presentation.

---

## Stack

<div align="center">

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=for-the-badge&logo=springsecurity&logoColor=white)
![Hibernate](https://img.shields.io/badge/Hibernate-59666C?style=for-the-badge&logo=hibernate&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?style=for-the-badge&logo=sqlalchemy&logoColor=white)
![Flyway](https://img.shields.io/badge/Flyway-CC0200?style=for-the-badge&logo=flyway&logoColor=white)
![Alembic](https://img.shields.io/badge/Alembic-6BA81E?style=for-the-badge&logo=alembic&logoColor=white)

![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Maven](https://img.shields.io/badge/Maven-C71A36?style=for-the-badge&logo=apachemaven&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)

</div>

---

<div align="center">

**Open to backend and data engineering roles.**

[![Portfolio](https://img.shields.io/badge/Portfolio-2496ED?style=for-the-badge&logo=googlechrome&logoColor=white)](https://migueldevplusplus.github.io)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:amvmiguelito@gmail.com)

</div>
