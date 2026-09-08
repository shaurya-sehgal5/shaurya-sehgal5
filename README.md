<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f0c29,50:302b63,100:24243e&height=180&section=header&text=SHAURYA%20SEHGAL&fontSize=40&fontColor=a78bfa&animation=twinkling&fontAlignY=38&desc=BACKEND%20%7C%20DEVOPS%20%7C%20PLATFORM%20ENGINEERING&descSize=17&descAlignY=62&descAlign=50" width="100%"/>

<br>

### Backend engineer who also owns the infrastructure it runs on.

<br>

![Backend Modules](https://img.shields.io/badge/Backend%20Modules-170%2B-a78bfa?style=for-the-badge)
![Pipeline](https://img.shields.io/badge/CI%2FCD%20Pipeline-17--stage-7C3AED?style=for-the-badge)
![Deploy Time](https://img.shields.io/badge/Push--to--Live-~60--100s-6d28d9?style=for-the-badge)
![Metrics](https://img.shields.io/badge/Tracked%20Metrics-20%2B-4c1d95?style=for-the-badge)
![Solo Build](https://img.shields.io/badge/Solo%20Build-~35%20days-a78bfa?style=for-the-badge)

<br>

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=17&duration=2800&pause=900&color=A78BFA&center=true&vCenter=true&multiline=false&width=850&lines=%24+whoami+%E2%86%92+Backend+%7C+DevOps+%7C+Platform+Engineer;%24+psql+-c+%22select+*+from+deployments%22+%E2%86%92+170%2B+modules+served;%24+docker+build+-t+velocore+.+%26%26+trivy+image+velocore+%E2%86%92+0+critical+CVEs;%24+kubectl+rollout+status+deployment%2Fvelocore+%E2%86%92+deployment+successful;%24+terraform+plan+-out%3Dtfplan+%E2%86%92+12+to+add%2C+0+to+destroy;%24+curl+-s+localhost%3A8080%2Fhealthz+%E2%86%92+200+OK;%24+echo+%24STATUS+%E2%86%92+open_to_work+%F0%9F%9F%A2)](https://git.io/typing-svg)

<br>

**BCA (Cyber Security) @ UPES Dehradun** · **Backend Development · DevOps · Platform Engineering** · **Open to Internships & Opportunities**

<br>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-shauryasehgal-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/shaurya-s-701b7a305/)
[![GitHub](https://img.shields.io/badge/GitHub-shaurya--sehgal5-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/shaurya-sehgal5)
[![Email](https://img.shields.io/badge/Email-shauryasehgal555-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:shauryasehgal555@gmail.com)

</div>

---

```bash
┌──(shaurya㉿devops)-[~]
└─$ cat /etc/identity
```

```yaml
name        : Shaurya Sehgal
education   : BCA (Cyber Security) — UPES Dehradun, expected July 2027
role        : Backend Development · DevOps · Platform Engineering
focus       : APIs · Distributed Systems · Kubernetes · CI/CD · DevSecOps
currently   : Building VeloCore
mindset     : "understand the system, automate the system"
open_to     : Backend · DevOps · Platform · Cloud · SRE
```

---

# ⚡ I Build Backend Systems — And the Infrastructure That Runs Them

Most of my work revolves around two questions:

> **How do you design a backend that holds up under real, asynchronous, failure-prone conditions?**
> **And what happens between a developer writing code and that code becoming a reliable production service?**

Both are the same problem from different sides — APIs, data models, and job queues on one end; containers, orchestration, and CI/CD on the other.

Instead of building another CRUD application, I built **VeloCore** — a self-hosted Platform-as-a-Service that turns a GitHub repository into a running application on Kubernetes, backed by a PostgreSQL-modeled, queue-driven backend.

---

# 🚀 VeloCore

<div align="center">

### **Self-hosted PaaS / Deployment Orchestration Platform**

**Git Push → Build → Security Scan → Kubernetes → Live Application → Monitoring**

<br>

[![VeloCore](https://img.shields.io/badge/🚀%20VeloCore-Explore%20Project-a78bfa?style=for-the-badge)](https://github.com/shaurya-sehgal5/VeloCore)

</div>

VeloCore is my flagship Platform Engineering project, built solo in ~35 days.

It provides a deployment experience similar to platforms such as Vercel, Railway, Render and Coolify — but the infrastructure is **owned and controlled by the user**.

The developer connects GitHub, selects a repository and deploys. VeloCore handles the infrastructure underneath.

VeloCore currently brings together **170+ backend modules, a 17-stage deployment pipeline, 5+ supported framework categories, and 20+ tracked platform/runtime metrics — taking a push live end-to-end in ~60–100 seconds.**

---

## 🧠 What VeloCore Actually Does

### 🔄 Deployment Orchestration

```text
GitHub
  ↓
Clone
  ↓
Framework Detection
  ↓
Dependency Graph
  ↓
Deployment Planning
  ↓
Docker Build
  ↓
Security Scan
  ↓
Helm Generation
  ↓
Kubernetes Deployment
  ↓
Health Verification
  ↓
Runtime Registration
  ↓
Monitoring
  ↓
Live Application
```

The backend — Node.js/Express, PostgreSQL, and BullMQ/Redis — coordinates the complete deployment lifecycle rather than simply running a shell script.

Deployment stages are explicitly tracked as state transitions, so failures can be reasoned about and recovered from — automatic rollback validates rollout health against Kubernetes liveness/readiness probes and restores the last known-good Helm release on failure.

---

# 🏗️ Architecture

```mermaid
flowchart LR

    A[React Dashboard]
    B[Express Backend]
    C[GitHub OAuth]
    D[BullMQ + Redis]
    E[Deployment Orchestrator]
    F[Builder]
    G[Docker / BuildKit]
    H[Trivy]
    I[Helm]
    J[Kubernetes]
    K[Prometheus]
    L[Grafana]
    M[Loki]
    N[Live Application]

    A --> B
    B --> C
    B --> D
    D --> E

    E --> F
    E --> G
    E --> H

    F --> I
    G --> I
    H --> I

    I --> J
    J --> N

    J --> K
    J --> M

    K --> L
    M --> L
```

### Core Components

| Component                   | Responsibility                                |
| --------------------------- | --------------------------------------------- |
| **Deployment Orchestrator** | Coordinates the complete deployment lifecycle |
| **Builder**                 | Detects frameworks and generates build plans  |
| **BullMQ**                  | Queues and controls deployment jobs           |
| **Redis**                   | Queue backend                                 |
| **Docker / BuildKit**       | Builds application images                     |
| **Trivy**                   | Container + CVE-severity security scanning    |
| **Helm**                    | Dynamic Kubernetes workload generation        |
| **Kubernetes**              | Application runtime                           |
| **Runtime Manager**         | Tracks live deployments and runtime state     |
| **PostgreSQL**              | Deployment metadata, events, rollback history |
| **Prometheus**              | Metrics collection                            |
| **Grafana**                 | Visualization and dashboards                  |
| **Loki**                    | Persistent log aggregation                    |
| **Socket.IO**               | Real-time deployment logs                     |

The architecture and component responsibilities are based directly on the VeloCore implementation.

---

# 🛠️ Technology Stack

<div align="center">

### Platform & Infrastructure

![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Helm](https://img.shields.io/badge/Helm-0F1689?style=flat-square&logo=helm&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-FF9900?style=flat-square&logo=amazonaws&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white)

### Backend & Systems

![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white)
![BullMQ](https://img.shields.io/badge/BullMQ-DC382D?style=flat-square)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)

### DevSecOps & Observability

![Trivy](https://img.shields.io/badge/Trivy-1904DA?style=flat-square)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)
![Loki](https://img.shields.io/badge/Loki-F5A800?style=flat-square&logo=grafana&logoColor=white)
![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=flat-square&logo=jenkins&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)

### Application

![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white)

</div>

The core VeloCore stack is Node.js/Express, React, Docker, Kubernetes, Helm, BullMQ/Redis, PostgreSQL, Prometheus/Grafana/Loki and Trivy.

---

# 💼 Beyond VeloCore

VeloCore is my main project, but it wasn't built in isolation.

**Cloud & Kubernetes Labs** — Hands-on AWS and infrastructure labs covering cloud networking, compute, storage, IAM, load balancing, CI/CD, Kubernetes (Minikube, Kind), and Terraform IaC. Used to build the infrastructure knowledge applied directly in VeloCore.

**Freelance — Nitro Media** — Independently deliver client web projects end-to-end (requirements → build → deployment), including sites for Harjas Hostel (React/Tailwind/Framer Motion), Om Residency (mobile-first, glassmorphism), and R.C. Eye & Dental Hospital.

**VeloCore is where the infrastructure concepts come together into one system.**

---

# 📚 What I'm Deepening

```bash
┌──(shaurya㉿devops)-[~]
└─$ ./current-focus.sh
```

```text
[01] Kubernetes
     ├── workloads
     ├── networking
     ├── scheduling
     ├── probes
     ├── scaling
     └── Helm

[02] Cloud
     ├── AWS
     ├── networking
     ├── compute
     ├── IAM
     └── managed Kubernetes

[03] Infrastructure
     ├── Terraform
     ├── Linux
     ├── Docker
     └── automation

[04] Delivery
     ├── CI/CD
     ├── GitHub Actions
     └── deployment orchestration

[05] Reliability
     ├── Prometheus
     ├── Grafana
     ├── Loki
     └── failure recovery

[06] Security
     ├── container scanning
     ├── secrets
     ├── CVEs
     └── DevSecOps
```

---

# 🎯 What I'm Looking For

I'm currently looking for opportunities where I can work close to backend systems, infrastructure, or both.

```text
Backend Development / SDE
DevOps Engineering
Platform Engineering
Cloud Infrastructure
DevSecOps
Site Reliability Engineering
Backend / DevOps / Cloud Internships
```

I'm particularly interested in teams where I can work with:

```text
Node.js / APIs
   +
PostgreSQL / Redis
   +
Docker / Kubernetes
   +
AWS / Terraform
   +
CI/CD
   +
Observability
   +
Security
```

---

# 📊 GitHub Activity

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=shaurya-sehgal5&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0d1117&title_color=a78bfa&icon_color=7C3AED&text_color=c9d1d9&border_radius=12&rank_icon=github&include_all_commits=true&count_private=true" height="170"/>

<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=shaurya-sehgal5&layout=compact&theme=tokyonight&hide_border=true&bg_color=0d1117&title_color=a78bfa&text_color=c9d1d9&border_radius=12&langs_count=8" height="170"/>

<br><br>

<img src="https://streak-stats.demolab.com?user=shaurya-sehgal5&theme=tokyonight-duo&hide_border=true&background=0d1117&ring=7C3AED&fire=a78bfa&currStreakLabel=c9d1d9&border_radius=12&dates=c9d1d9&sideLabels=a78bfa&sideNums=ffffff" height="170"/>

<br><br>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=shaurya-sehgal5&bg_color=0d1117&color=a78bfa&line=7C3AED&point=ffffff&area=true&area_color=302b63&hide_border=true&radius=12&custom_title=Contribution%20Activity" width="95%"/>

</div>

---

<div align="center">

### `build → automate → observe → secure → improve`

<br>

[![LinkedIn](https://img.shields.io/badge/Let's%20Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/shaurya-s-701b7a305/)
[![GitHub](https://img.shields.io/badge/Explore%20My%20Work-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/shaurya-sehgal5)

<br><br>

<sub><code>infrastructure is the product · automation is the interface · reliability is the goal</code></sub>

<br><br>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:24243e,50:302b63,100:0f0c29&height=110&section=footer" width="100%"/>

</div>
