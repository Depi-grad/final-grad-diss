# Monitoring a Containerized URL Shortener Webservice


## 👥 Team Members

- Ziad Ahmed Attia Mohamed  **Team Leader**
- Omar Samir Elmallah
- Yasmeen Mohamed Talaat 
- Mohamed Sabry Abdelrahim 


---

## 📌 Project Name

**Monitoring a Containerized URL Shortener Webservice**

---

## 📌 Project Idea

A webservice that allows users to shorten long URLs into short codes and handle redirections from those codes to the original URLs. The service is fully containerized using Docker, with integrated monitoring and visualization via Prometheus and Grafana. The goal is to build a robust, observable, and persistent stack that provides real-time performance insights and reliability.

---

## 🗂️ Project Plan and Timeline

- **Week 1 – Build & Containerize**
  - Develop a webservice with two API endpoints:
    - `POST /shorten`: Accepts a long URL, returns a short code
    - `GET /<short_code>`: Redirects to original URL
  - Implement data storage using SQLite
  - Write Dockerfile and docker-compose.yml for local deployment

- **Week 2 – Instrument with Prometheus Metrics**
  - Add custom metrics:
    - Counter: URLs shortened
    - Counter: Successful redirects
    - Counter: Failed lookups (404)
    - Histogram: Request latency
  - Integrate Prometheus (prometheus.yml, service in docker-compose.yml)

- **Week 3 – Visualization with Grafana**
  - Add Grafana service to docker-compose.yml
  - Connect Grafana to Prometheus
  - Build dashboard:
    - URL creation & redirect rates
    - Total shortened links (single stat)
    - 95th percentile latency
    - 404 error rate

- **Week 4 – Alerting & Data Persistence**
  - Configure meaningful alerts in Grafana:
    - High latency
    - 404 spikes
  - Set up persistent volumes in Docker for SQLite, Prometheus, and Grafana
  - Final testing and documentation (README, API specs)

---

## 📝 Individual Roles and Responsibilities

| Member                    | Role & Tasks                                                             |
|---------------------------|--------------------------------------------------------------------------|
| Mohamed Sabry Abdelrahim  | Coordination, Webservice backend, API development (Flask/Express), documentation                   |
|Yasmeen Mohamed Talaat     |  Grafana, Advanced Visualization      |
| Ziad Ahmed Attia Mohamed  | Container setup, Dockerfile, docker-compose.yml                          |
| Omar Samir Elmallah       | Prometheus metrics integration, persistence, documentation         |

---
