# Zoo Management System — Bases de Dados

Course project developed for **Bases de Dados** (Databases) at **Instituto Superior Técnico (IST)**.

---

## 🐘 Overview

Design, implementation, and deployment of a relational database system for a **Zoo Management and Ticketing Platform**, covering domain modeling, database programming, web services, and analytical querying.

---

## 📂 Project Phases

### 🔹 Part 1 — Conceptual & Logical Modeling
* **Entity-Relationship (E-R) Design**: Complete conceptual model capturing animals, species compatibility, enclosure hierarchies, ticket sales, and staff supervision.
* **Integrity Constraints (ICs)**: Business rules formalized outside graphical E-R limits.
* **Relational Mapping & Normalization**: Conversion to relational schema normalized to **Boyce-Codd Normal Form (BCNF)** / 3NF.
* **Relational Algebra**: Formulation of formal algebraic queries on ticketing and enclosure access.

---

### 🔹 Part 2 — Implementation, Web Service & Analytics
* **PostgreSQL Schema & Triggers**:
  * Implemented tables, constraints, and custom ENUM types in PostgreSQL.
  * Enforced business integrity rules (RI-1 to RI-4) using **PL/pgSQL Triggers**.
* **Database Population**: Synthetic data generation respecting strict statistical coverage (200+ species, ticket sales, enclosure voting).
* **RESTful Web API**:
  * Lightweight web service in **Python (Flask)** with endpoints for browsing enclosures, purchasing tickets, and casting votes.
  * Implemented secure transactions (ACID) and parameterized queries to prevent SQL injection.
* **Data Engineering & OLAP Analytics**:
  * Created materialized views (`vendas_zoo`) to analyze revenue, ticket volume, and enclosure popularity.
  * Executed OLAP and analytical SQL queries.
* **Query Optimization**: Performance tuning using custom **B-Tree indexes**, verified and evaluated via `EXPLAIN ANALYSE`.

---

## 💻 Tech Stack
* **Database**: PostgreSQL
* **Backend**: Python 3, Flask, Psycopg
* **Tools**: Docker, Jupyter Notebook, Draw.io
