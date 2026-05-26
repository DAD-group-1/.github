# 🎓 ENTropy — Academic ERP

> *"Shaping Tomorrow's Minds"*

Welcome to the official GitHub organization of the **ENTropy** development team.
This space hosts all repositories related to the design, development, and deployment of our internal Academic ERP — a unified platform to centralize multi-campus management, digitize administrative processes, and produce reliable strategic indicators across all Novacampus campuses.

---

## 📌 Project Overview

ENTropy is a rapidly expanding private higher education group operating across multiple campuses. After six years of strong growth, the organization is modernizing its information system to replace a fragmented set of tools with a single, integrated platform.

The ERP covers:

- 📅 Schedule & room management
- 🎓 Student academic tracking (grades, absences, history)
- 💳 Billing & payment follow-up
- 📊 Consolidated reporting across campuses
- 🤖 An AI agent integrated into key business processes

---

## 🗂️ Repositories

| Repository                        | Description                                                                  |
|-----------------------------------|------------------------------------------------------------------------------|
| `entropy-frontend`                | Angular-based web application: student, teacher, admin & management portals |
| `entropy-backend-common`          | Common package: shared models, utilities, and interfaces for all backend services |
| `entropy-backend-gateway`         | API Gateway: routing, auth middleware, rate limiting                        |
| `entropy-backend-ms-user`         | User microservice: authentication, roles, profiles                          |
| `entropy-backend-ms-course`       | Course microservice: course management, sessions, resources                 |
| `entropy-backend-ms-schedule`     | Schedule microservice: timetables, room assignment, conflict detection      |
| `entropy-backend-ms-grade`        | Grade & absence microservice: grade entry, attendance tracking              |
| `entropy-backend-ms-billing`      | Billing microservice: payments, invoices, reminders                         |
| `entropy-backend-ms-notification` | Notification microservice: in-app, email, and push notifications            |
| `entropy-backend-ms-ai-agent`     | AI agent microservice: automation and process assistance                    |

---

## 👥 Team

| Name               | Role                                     | GitHub                                    |
|--------------------|------------------------------------------|-------------------------------------------|
| Anthony SCHNEPP    | Frontend Engineer / UI/UX Designer       | [@Anthony](https://github.com/aschnepp)   |
| Guillaume FERRAND  | Backend Engineer / Architect             | [@Guillaume](https://github.com/Red-Hide) |
| Enorian RAJOELISOA | Backend Abstraction Engineer / Architect | [@Enorian](https://github.com/En0ri4n)    |

---

## 🏛️ Architecture

The platform is built on a **microservices architecture** exposed through a single API Gateway.
Each service owns its data and communicates via REST and asynchronous events.

```
┌─────────────────────────────────────────┐
│              ERP Frontend               │
│       (Angular — role-based UI)         │
└────────────────────┬────────────────────┘
                     │
           ┌─────────▼─────────┐
           │    API Gateway     │
           │  (auth, routing)   │
           └──┬──┬──┬──┬──┬───┘
              │  │  │  │  │
    ┌─────────┘  │  │  │  └──────────┐
    │        ┌───┘  │  └───┐         │
    ▼        ▼      ▼      ▼         ▼
 ms-user  ms-course ms-  ms-grade ms-billing
          ms-sched  notif ms-repor ms-ai-agent
```

---

## 🚀 Getting Started

### Prerequisites

Each service can also be run independently — refer to its own `README.md` for specific instructions.

---

## 🔀 Branching Strategy

| Branch | Purpose |
|---|---|
| `main` | Production-ready code only |
| `dev` | Integration branch — all features merged here first |
| `feature/xxx` | Individual feature branches |
| `fix/xxx` | Bug fix branches |
| `release/x.x.x` | Release preparation branches |

All pull requests must target `develop`. Direct pushes to `main` are disabled.

---

## 📄 License

This project is proprietary and confidential.
© 2026 ENTropy — All rights reserved.
