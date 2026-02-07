# 🚀 CI/CD Pipeline with DevSecOps & Kubernetes Monitoring

This project demonstrates a complete production-style CI/CD pipeline built from scratch using DevOps and DevSecOps best practices. It covers automated build, test, code quality analysis, security scanning, artifact management, containerization, Kubernetes deployment, and full-stack monitoring.

The pipeline is designed to simulate a real corporate software delivery workflow — from developer commit to monitored production deployment.

---

# 📌 Project Objectives

* Build an end-to-end CI/CD pipeline
* Integrate code quality and security checks
* Automate artifact and container image management
* Deploy application to Kubernetes cluster
* Enforce RBAC security model
* Implement system + application monitoring
* Enable automated notifications

---

# 🧱 Architecture Overview

```
Developer → GitHub → Jenkins Pipeline →
Build & Test → SonarQube → Trivy FS Scan →
Maven Package → Nexus Artifact Repo →
Docker Build → Trivy Image Scan →
DockerHub Push → Kubernetes Deploy →
RBAC + ServiceAccount →
Prometheus + Blackbox Exporter →
Grafana Dashboards → Email Alerts
```
<img width="913" height="605" alt="Screenshot 2026-02-07 at 4 54 00 PM" src="https://github.com/user-attachments/assets/c952f704-5c58-4c84-849b-3113843526b6" />

---

# ⚙️ Tech Stack

## CI/CD

* Jenkins (Pipeline as Code)
* Maven
* GitHub (Private Repo)

## Code Quality & Security

* SonarQube
* Trivy (Filesystem + Image scanning)

## Artifact & Container

* Nexus Repository
* Docker
* DockerHub

## Container Orchestration

* Kubernetes Cluster (kubeadm multi-node)
* RBAC + ServiceAccount

## Monitoring

* Prometheus
* Grafana
* Node Exporter
* Blackbox Exporter

## Infrastructure

* AWS EC2 (multi-VM setup)
* Ubuntu 20.04 servers

---

<img width="1438" height="775" alt="Screenshot 2026-02-06 at 9 17 28 PM" src="https://github.com/user-attachments/assets/6d9c4569-20d8-4f9a-9a48-3f1f80c32006" />


# 🔄 CI/CD Pipeline Stages

## ✅ Stage 1 — Source Checkout

* Pulls code from private GitHub repository using access token credentials

📸 Screenshot:
<img width="1440" height="900" alt="Screenshot 2026-02-06 at 9 19 25 PM" src="https://github.com/user-attachments/assets/86c070f3-052d-4350-bc08-75952b97343d" />


---

## 🛠 Stage 2 — Build & Compile

* Maven compile
* Dependency resolution
* Syntax validation



---

## 🧪 Stage 3 — Unit Testing

* Maven test execution
* Test report generation



---

## 🔍 Stage 4 — Code Quality Analysis

* SonarQube static code analysis
* Bug, vulnerability, code smell detection
* Quality Gate enforcement

📸 Screenshot:
<img width="1435" height="855" alt="Screenshot 2026-02-06 at 9 16 59 PM" src="https://github.com/user-attachments/assets/6a24683e-4100-4b8c-b288-d6de4e6cde6f" />

---

## 🛡 Stage 5 — Filesystem Security Scan

* Trivy FS scan
* Dependency vulnerability detection
* HTML report exported


---

## 📦 Stage 6 — Package & Artifact Publish

* Maven package
* Artifact versioning
* Upload to Nexus repository


---

## 🐳 Stage 7 — Docker Build & Tag

* Docker image build
* Version tagging
* Multi-stage build (if used)



---

## 🔐 Stage 8 — Container Security Scan

* Trivy image scan
* Vulnerability detection before push


---

## 🚚 Stage 9 — Docker Push

* Push image to DockerHub registry


---

## ☸️ Stage 10 — Kubernetes Deployment

* Deployment YAML applied
* Service created
* LoadBalancer exposure
* Replica configuration


---

## 🔑 Stage 11 — RBAC Security

* ServiceAccount created
* Role & RoleBinding configured
* Least-privilege deployment access



---

## 📬 Stage 12 — Notifications

* Email alerts on:

  * Pipeline success
  * Pipeline failure
  * Scan reports attached

📸 Screenshot:
<img width="1440" height="900" alt="Screenshot 2026-02-06 at 9 19 39 PM" src="https://github.com/user-attachments/assets/a24a3bcd-dbfa-4a9c-a79b-5c1ef0ee943e" />


---

# 📊 Monitoring Stack

## 🌐 Application Monitoring

* Blackbox exporter probes
* HTTP uptime checks
* Endpoint health monitoring

📸 Screenshot:
<img width="1440" height="900" alt="Screenshot 2026-02-06 at 9 17 53 PM" src="https://github.com/user-attachments/assets/d2433997-b50a-4750-97aa-a4beca097efd" />


---

## 🖥 System Monitoring

* Node exporter metrics
* Jenkins server CPU / RAM / Load tracking

📸 Screenshot:
<img width="1440" height="900" alt="Screenshot 2026-02-06 at 9 18 28 PM" src="https://github.com/user-attachments/assets/6af36f27-ccb5-4835-8095-6404d7e64c12" />


---

## 📈 Grafana Dashboards

* Prometheus datasource
* Blackbox dashboard
* Node exporter dashboard

📸 Screenshot:
<img width="1436" height="853" alt="Screenshot 2026-02-06 at 9 18 16 PM" src="https://github.com/user-attachments/assets/ff0236cf-432f-46d1-a21a-3487eeb3a159" />


---

# 🔐 Security Measures Implemented

* Private Git repository
* Token-based authentication
* SonarQube quality gates
* Trivy vulnerability scanning
* Kubernetes RBAC
* ServiceAccount isolation
* Credential store in Jenkins
* No hardcoded secrets

---

# 🧠 Key DevOps Concepts Demonstrated

* Pipeline as Code
* DevSecOps integration
* Shift-left security
* Artifact lifecycle management
* Container scanning
* Kubernetes RBAC
* Observability design
* Infrastructure isolation

---

# 🚀 How To Run (High Level)

1. Provision VMs
2. Install Jenkins, SonarQube, Nexus
3. Configure Docker & Kubernetes
4. Configure Jenkins tools + credentials
5. Create pipeline job
6. Commit code → pipeline triggers
7. Monitor via Grafana

---

# 📂 Repo Structure

```
.
├── Jenkinsfile
├── pom.xml
├── Dockerfile
├── k8s/
│   ├── deployment.yaml
│   └── service.yaml
├── docs/
│   └── screenshots/
```

---
