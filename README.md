<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f0c29,50:302b63,100:24243e&height=180&section=header&text=SHAURYA%20SEHGAL&fontSize=40&fontColor=a78bfa&animation=twinkling&fontAlignY=38&desc=DEVOPS%20%7C%20PLATFORM%20ENGINEERING%20%7C%20CLOUD&descSize=18&descAlignY=62&descAlign=50" width="100%"/>

<br>

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono\&weight=600\&size=17\&duration=2800\&pause=900\&color=A78BFA\&center=true\&vCenter=true\&multiline=false\&width=850\&lines=%24+whoami+%E2%86%92+DevOps+%7C+Platform+Engineering;%24+cat+%2Fetc%2Fmission+%E2%86%92+automate+the+path+to+production;%24+git+push+%E2%86%92+build+%E2%86%92+secure+%E2%86%92+deploy+%E2%86%92+observe;%24+kubectl+get+projects+%E2%86%92+VeloCore+%F0%9F%9A%80;%24+status+%E2%86%92+building+cloud-native+systems;%24+ping+recruiter+-t+%E2%86%92+open+to+work+%F0%9F%9F%A2)](https://git.io/typing-svg)

<br>

**BCA @ UPES Dehradun** · **DevOps / Platform Engineering** · **Open to Internships & Opportunities**


<br>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-shauryasehgal-0A66C2?style=for-the-badge\&logo=linkedin\&logoColor=white)](https://www.linkedin.com/in/shaurya-s-701b7a305/)
[![GitHub](https://img.shields.io/badge/GitHub-shaurya--sehgal5-181717?style=for-the-badge\&logo=github\&logoColor=white)](https://github.com/shaurya-sehgal5)
[![Email](https://img.shields.io/badge/Email-shauryasehgal555-EA4335?style=for-the-badge\&logo=gmail\&logoColor=white)](mailto:shauryasehgal555@gmail.com)

</div>

---

```bash
┌──(shaurya㉿devops)-[~]
└─$ cat /etc/identity
```

```yaml
name        : Shaurya Sehgal
education   : BCA — UPES Dehradun
role        : DevOps / Platform Engineering
focus       : Cloud Infrastructure · Kubernetes · CI/CD · DevSecOps
currently   : Building VeloCore
mindset     : "understand the system, automate the system"
open_to     : DevOps · Platform · Cloud · DevSecOps · SRE
```

---

# ⚡ I Build Platforms, Not Just Projects

Most of my work revolves around one question:

> **What happens between a developer writing code and that code becoming a reliable production service?**

That's the layer I'm interested in.

Infrastructure.
Containers.
CI/CD.
Kubernetes.
Security.
Observability.
Automation.
Failure recovery.

Instead of building another CRUD application, I built **VeloCore** — a self-hosted Platform-as-a-Service that turns a GitHub repository into a running application on Kubernetes.

---

# 🚀 VeloCore

<div align="center">

### **Self-hosted PaaS / Deployment Orchestration Platform**

**Git Push → Build → Security Scan → Kubernetes → Live Application → Monitoring**

<br>

[![VeloCore](https://img.shields.io/badge/🚀%20VeloCore-Explore%20Project-a78bfa?style=for-the-badge)](https://github.com/shaurya-sehgal5/VeloCore)

</div>

VeloCore is my flagship Platform Engineering project.

It provides a deployment experience similar to platforms such as Vercel, Railway, Render and Coolify — but the infrastructure is **owned and controlled by the user**.

The developer connects GitHub, selects a repository and deploys.

VeloCore handles the infrastructure underneath:

VeloCore currently brings together **170+ backend modules, 17 deployment stages, 4 supported framework categories and 3 observability systems**.

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

The backend coordinates the complete deployment lifecycle rather than simply running a shell script.

Deployment stages are explicitly tracked so failures can be reasoned about and recovered from.

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
| **Trivy**                   | Container security scanning                   |
| **Helm**                    | Dynamic Kubernetes workload generation        |
| **Kubernetes**              | Application runtime                           |
| **Runtime Manager**         | Tracks live deployments and runtime state     |
| **Prometheus**              | Metrics collection                            |
| **Grafana**                 | Visualization and dashboards                  |
| **Loki**                    | Persistent log aggregation                    |
| **Socket.IO**               | Real-time deployment logs                     |

The architecture and component responsibilities are based directly on the VeloCore implementation.

---
# 🛠️ Technology Stack

<div align="center">

### Platform & Infrastructure

![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square\&logo=linux\&logoColor=black)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square\&logo=docker\&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square\&logo=kubernetes\&logoColor=white)
![Helm](https://img.shields.io/badge/Helm-0F1689?style=flat-square\&logo=helm\&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-FF9900?style=flat-square\&logo=amazonaws\&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat-square\&logo=terraform\&logoColor=white)

### Backend & Systems

![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square\&logo=node.js\&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat-square\&logo=express\&logoColor=white)
![BullMQ](https://img.shields.io/badge/BullMQ-DC382D?style=flat-square)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square\&logo=redis\&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square\&logo=postgresql\&logoColor=white)

### DevSecOps & Observability

![Trivy](https://img.shields.io/badge/Trivy-1904DA?style=flat-square)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square\&logo=prometheus\&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square\&logo=grafana\&logoColor=white)
![Loki](https://img.shields.io/badge/Loki-F5A800?style=flat-square\&logo=grafana\&logoColor=white)
![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=flat-square\&logo=jenkins\&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square\&logo=githubactions\&logoColor=white)

### Application

![React](https://img.shields.io/badge/React-61DAFB?style=flat-square\&logo=react\&logoColor=black)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square\&logo=vite\&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square\&logo=javascript\&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square\&logo=python\&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square\&logo=gnubash\&logoColor=white)

</div>

The core VeloCore stack is Node.js/Express, React, Docker, Kubernetes, Helm, BullMQ/Redis, PostgreSQL, Prometheus/Grafana/Loki and Trivy.

---

# 🧪 Beyond VeloCore

VeloCore is my main project, but it wasn't built in isolation.

I've also built **hands-on AWS and infrastructure labs** covering cloud networking, compute, storage, IAM, load balancing, CI/CD, Kubernetes and Infrastructure as Code.

Those labs were primarily used to build the underlying infrastructure knowledge that I applied while building VeloCore.

**VeloCore is where those concepts come together into one system.**

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

I'm currently looking for opportunities where I can work close to infrastructure and production systems.

```text
DevOps Engineering
Platform Engineering
Cloud Infrastructure
DevSecOps
Site Reliability Engineering
Infrastructure Engineering
DevOps / Cloud Internships
```

I'm particularly interested in teams where I can work with:

```text
Linux
   +
AWS
   +
Docker
   +
Kubernetes
   +
Terraform
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

[![LinkedIn](https://img.shields.io/badge/Let's%20Connect-0A66C2?style=for-the-badge\&logo=linkedin\&logoColor=white)](https://www.linkedin.com/in/shaurya-s-701b7a305/)
[![GitHub](https://img.shields.io/badge/Explore%20My%20Work-181717?style=for-the-badge\&logo=github\&logoColor=white)](https://github.com/shaurya-sehgal5)

<br><br>

<sub><code>infrastructure is the product · automation is the interface · reliability is the goal</code></sub>

<br><br>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:24243e,50:302b63,100:0f0c29&height=110&section=footer" width="100%"/>

</div>
