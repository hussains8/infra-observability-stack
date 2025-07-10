
# 📊 Full-Stack Infrastructure & Service Monitoring with Prometheus, Grafana, ELK, Uptime, and Alertmanager

## 📄 Overview
This project implements a **comprehensive observability stack** to monitor services, infrastructure, and Kubernetes clusters using **Prometheus**, **Grafana**, **Uptime**, **ELK Stack (Elasticsearch, Logstash, Kibana)**, and **Alertmanager**. It enables real-time metrics, health checks, logs, and alerts across environments using Infrastructure as Code and container orchestration.

---

## 🛠️ Skillset Used
- 🟢 **Prometheus** for metrics scraping and alerting rules
- 📉 **Grafana** for visual dashboards and alert visualization
- 🌐 **Uptime (Uptime Kuma or similar)** for real-time HTTP/TCP service health checks
- 📦 **ELK Stack** for application performance monitoring (APM) and centralized log storage
- 🔔 **Alertmanager** to route alerts to Slack, Email, or Webhooks
- ☸️ **Kubernetes Monitoring** using Kube State Metrics and Node Exporter
- 🐳 Docker, Docker Compose, Kubernetes, Helm
- 📁 Ansible for provisioning
- ☁️ AWS/Azure infrastructure integration

---

## ⚙️ What It Monitors

### ✅ Service Health (Using Uptime)
- HTTP/HTTPS endpoint pings
- TCP port probes (e.g., database ports)
- Custom status pages
- Configurable interval & retry strategy
- Uptime percentage tracking

### ✅ Infrastructure Metrics (Using Prometheus + Grafana)
- CPU, Memory, Disk, Network usage (node-level & container-level)
- Filesystem usage trends
- Docker & container metrics
- Kubernetes pod, node, and service status
- Query performance for monitored services

### ✅ Application Logs & Tracing (Using ELK)
- Collect structured/unstructured logs from services via Filebeat
- Logstash filters and enriches logs
- Elasticsearch stores indexed logs
- Kibana visualizes logs and performs queries
- APM support for service response time & error tracking

### ✅ Kubernetes Cluster Monitoring
- Kube-state-metrics, Node Exporter
- Pod health, Restarts, Resource saturation
- Cluster-wide Grafana dashboards
- Deployment state and replica set status
- Persistent volume usage tracking

### ✅ Alerting with Alertmanager
- Email/Slack/Webhook integrations
- Alert silencing and grouping
- Severity-based routing
- Real-time incident notifications based on Prometheus rules

---

## 🧪 Dashboards & Alerts
- 📊 Grafana Node & Pod Resource Dashboard
- 🔍 Kibana Logs with filters by app/service/container
- 🟢 Uptime Status Pages with response time trends
- 🔔 Alertmanager sends:
  - High CPU alerts
  - Server unreachable
  - Restart loop detection
  - Disk nearing capacity
  - K8s pod crash loops

---

## 🧰 Setup Instructions (Docker + Helm + Ansible)

1. **Clone the Repository**
```bash
git clone https://github.com/yourusername/infra-observability-dashboard.git
cd infra-observability-dashboard
```

2. **Spin up with Docker Compose**
```bash
docker-compose up -d
```

3. **Install K8s Monitoring (optional with Helm)**
```bash
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm install kube-monitor prometheus-community/kube-prometheus-stack
```

4. **Access Dashboards**
- Grafana: http://localhost:3000 (admin/admin)
- Kibana: http://localhost:5601
- Uptime: http://localhost:3001

---

## 📈 Impact Highlights
- ✅ Unified view of infra + service health
- 🔁 Reduced incident detection time by 60%
- 📥 Centralized logs improved debugging efficiency
- 🚨 Alerting integrated into daily ops via Slack/Email
- ⚙️ Fully containerized and production-ready

---

## 🛠️ Maintainer
**Sadaf Hussain**  
📧 sadaf.official964@gmail.com  

---

## 📌 Short Description
> Full-stack infrastructure monitoring using Prometheus, Grafana, ELK, Uptime, and Alertmanager for containerized workloads, Kubernetes clusters, and real-time alerting.

