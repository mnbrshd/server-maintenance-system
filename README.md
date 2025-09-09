# Server Predictive Maintenance System

**Monitor, analyze, and maintain server health using rule-based logic**

---

## Table of Contents

1. [Overview](#overview)  
2. [Features](#features)  
3. [Tech Stack](#tech-stack)  
4. [Getting Started](#getting-started)  
   - Prerequisites  
   - Installation  
   - Running the Project  
5. [Usage](#usage)  
6. [Architecture & Workflow](#architecture--workflow)  
7. [Roadmap](#roadmap)  

---

## Overview

This project simulates (or optionally integrates with real) servers and monitors key performance indicators—CPU, memory, uptime, and temperature—against configurable rules to deliver predictive maintenance insights. It provides real-time dashboards, alerting mechanisms, historical logs, and optional integration with Prometheus and Grafana.

---

## Features

- Rule-based engine with customizable metrics and thresholds  
- Server simulation or real-time data collection via `psutil`  
- Full REST API powered by FastAPI (with pagination, filtering, validation, error handling, rate limiting)  
- Secure JWT-based user authentication and scoped access  
- Alerting and logging of maintenance triggers  
- React-based frontend dashboard for monitoring, trends, and alerts  
- Optional Prometheus & Grafana monitoring stack  
- Containerized with Docker and deployable to AWS environments  

---

## Tech Stack

| Component         | Technology                        |
|------------------|-----------------------------------|
| **Backend**       | FastAPI, SQLAlchemy (Python)      |
| **Database**      | PostgreSQL                        |
| **Frontend**      | React, JavaScript                 |
| **Simulation**    | Python + psutil or synthetic data |
| **Monitoring**    | Prometheus, Grafana (optional)    |
| **Containerization** | Docker                        |
| **Cloud Deployment** | AWS (EC2, RDS, S3)            |

---

## Getting Started

### Prerequisites

Make sure you have:

- Python 3.10+  
- Node.js & npm (for frontend)  
- Docker & Docker Compose  
- (Optional) AWS account for deployment  

### Installation

```bash
git clone https://github.com/yourusername/server-predictive-maintenance.git
cd server-predictive-maintenance
```
### Running the Project (Locally)

docker-compose up --build
This starts:
 - Backend at http://localhost:8000
 - Frontend at http://localhost:3000
 - Prometheus & Grafana dashboards (if enabled)

## Usage
1. Register or log in via the frontend.
2. Add new server instances or let the simulator auto-generate.
3. Define rules (e.g., CPU > 90%, memory > 85%, uptime > 365 days).
4. View server metrics, alerts, and maintenance logs in real time.
5. (Optional) Dive into Grafana dashboards for visual analytics.

## Architecture & Workflow
1. Simulation Agent creates or monitors server metrics.
2. Backend stores server data and rules.
3. A background task evaluates metrics against rules, generating alerts.
4. Frontend displays real-time status, historical trends, and alerts.
5. Prometheus optionally scrapes metrics for dashboarding in Grafana.

## Roadmap
 - [] Basic server simulation and CRUD endpoints
 - [] Rule engine and alert logging
 - [] User authentication and scoped access
 - [] React frontend with dashboards
 - [] Prometheus/Grafana integration
 - [] Email/Slack alert notifications
 - [] PDF/CSV reporting for trends and alerts
