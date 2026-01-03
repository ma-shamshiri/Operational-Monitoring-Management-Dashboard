# Operational Monitoring & Management Dashboard

A full-stack operational dashboard that provides visibility into system metrics, events, and operational health through aggregated APIs and resilient user interfaces.

This project focuses on building reliable monitoring surfaces backed by scalable data access patterns rather than one-off visualizations.

---

## 📑 Table of Contents
<details open>
<summary>Click to collapse</summary>

- [Project Overview](#toc-overview)
- [Core Capabilities](#toc-capabilities)
- [High-Level Architecture](#toc-architecture)
- [Technology Stack](#toc-tech-stack)
- [Backend Responsibilities](#toc-backend)
- [Frontend Responsibilities](#toc-frontend)
- [Data Aggregation Strategy](#toc-data)
- [Operational Flow](#toc-flow)
- [Running Locally](#toc-local)
- [Contact](#toc-contact)

</details>

---

<a id="toc-overview"></a>
## 📊 Project Overview

Operational teams rely on accurate, timely information to understand system behavior and respond to issues. Raw logs and metrics alone are rarely sufficient without aggregation and structured presentation.

This project implements a monitoring and management dashboard that:
- Aggregates operational metrics and events via backend services
- Exposes structured APIs optimized for time-based queries
- Presents data through a responsive, role-aware interface
- Remains usable under partial failures or delayed data

The emphasis is on **clarity, resilience, and scalability**.

---

<a id="toc-capabilities"></a>
## 🧭 Core Capabilities

- Centralized visibility into operational metrics and system events
- Time-window filtering and data segmentation
- Role-based access to views and actions
- Graceful handling of loading, empty, and error states
- API-driven design supporting scheduled data refresh
- Clear separation between data aggregation and presentation

---

<a id="toc-architecture"></a>
## 🏗️ High-Level Architecture

The system follows a clean full-stack separation:

### Client Layer
- Next.js application for server-rendered and client-side pages
- Modular React components with shared state management
- Role-aware routing and conditional UI rendering

### Service Layer
- FastAPI backend exposing REST endpoints
- Scheduled background jobs for aggregation
- Predictable response contracts for frontend consumption

### Storage Layer
- PostgreSQL database for raw events and aggregated metrics
- Indexed tables optimized for read-heavy dashboard access

---

<a id="toc-tech-stack"></a>
## 🧰 Technology Stack

- **Frontend:** Next.js, React, TypeScript  
- **Backend:** FastAPI (Python)  
- **Database:** PostgreSQL  
- **Containerization:** Docker  

All components are containerized to support consistent local development and deployment.

---

<a id="toc-backend"></a>
## 🔍 Backend Responsibilities

The backend is designed to prioritize predictable performance:

- Exposes REST endpoints for metrics and operational events
- Supports time-based filtering and pagination
- Performs aggregation outside request paths when possible
- Returns stable schemas for frontend rendering

This minimizes frontend complexity while keeping query costs controlled.

---

<a id="toc-frontend"></a>
## 🖥️ Frontend Responsibilities

The frontend is built with operator experience in mind:

- Responsive layouts for large datasets
- Filtering and segmentation controls
- Role-based visibility for sensitive data
- Explicit UI states for loading, errors, and empty results

The UI remains usable even when backend data is incomplete or delayed.

---

<a id="toc-data"></a>
## 🗄️ Data Aggregation Strategy

The data layer distinguishes between raw and derived data:

- Raw tables store incoming operational events
- Aggregation tables summarize data over time windows
- Indexes support range queries and ordering
- Aggregations reduce runtime computation during dashboard requests

This approach balances performance with traceability.

---

<a id="toc-flow"></a>
## 🔄 Operational Flow

1. Backend services emit metrics and operational events.
2. Scheduled jobs aggregate data into time-based summaries.
3. The frontend queries APIs with filters and time ranges.
4. Aggregated results are rendered based on user role.
5. UI adapts to loading, error, or empty conditions.

---

<a id="toc-local"></a>
## 🧪 Running Locally

The full system can be started using Docker:

```bash
docker-compose up --build
```

---

<a id="toc-contact"></a>
## 📬 Contact

Feel free to reach out or explore more of my work:

[![GitHub Badge](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/ma-shamshiri)
[![LinkedIn Badge](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ma-shamshiri)
