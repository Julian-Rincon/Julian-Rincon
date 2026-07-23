<div align="center">

<h1>Julian Rincón</h1>
<h3>ML Engineering · Distributed Systems · Autonomous AI · Stochastic Modeling</h3>

<br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/julian-esteban-rinc%C3%B3n-rodriguez-1a05501b7/)
[![Portfolio](https://img.shields.io/badge/Portfolio-1B4F8A?style=for-the-badge&logo=githubpages&logoColor=white)](https://julian-rincon.github.io)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:julianer2002@gmail.com)
[![AWS](https://img.shields.io/badge/AWS_Certified-Data_Engineering-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)](https://www.credly.com/go/UGp1CUEB)
![Location](https://img.shields.io/badge/Colombia-FFCD00?style=for-the-badge&logo=googlemaps&logoColor=white)

</div>

---

## About

I don't build demos. I build systems that run.

9th-semester (final term) CS & AI student at Universidad Sergio Arboleda, working at the intersection of machine learning engineering, distributed data infrastructure, and autonomous AI systems. My stack runs on real AWS infrastructure and a Linux workstation — not just notebooks.

```python
julian = {
    "focus":    ["ML Engineering", "Data Engineering", "Autonomous Agents", "Stochastic Systems"],
    "building": [
        "NEXUS — autonomous personal AI system (5-tier LLM routing, 38 skills, GCP hybrid, MCP server)",
        "SAVI v2     — autonomous valuation via RL pipeline (MDP → Q-Learning → DQN)",
        "ShopStream  — end-to-end AWS Big Data pipeline (Lambda → EMR → Glue → RDS)",
    ],
    "stack":    ["Python", "PySpark", "PyTorch", "AWS", "Terraform", "FastAPI", "TypeScript"],
    "won":      ["USABOT Robotics Challenge — 1st Place Overall (Nov 2025)",
                 "Wisibilízalas, Univ. Pompeu Fabra — 1st Place (WarmiTics)"],
    "goal":     "ML/Data Engineering internship → MSc in Germany",
    "open_to":  ["internships", "research collaborations", "freelance"],
}
```

---

## Tech Stack

**Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=for-the-badge&logo=gnubash&logoColor=white)

**ML / AI**

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-FF6600?style=for-the-badge&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=for-the-badge&logoColor=white)

**Cloud & Data Engineering**

![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=for-the-badge&logo=terraform&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Apache Spark](https://img.shields.io/badge/PySpark-E25A1C?style=for-the-badge&logo=apachespark&logoColor=white)

**Tools**

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

---

## Featured Projects

### 🤖 [NEXUS](https://github.com/Julian-Rincon/NEXUS-Public) — Autonomous Personal AI System `🟢 Active`

> Built a production-grade personal AI system on Linux that manages the machine, not just conversation. Evolved from a voice assistant into a 5-tier LLM routing system (Ollama → Groq → Cerebras 2600 tok/s → NVIDIA NIM 128K-context multimodal → Gemini) with 38 self-discovered skills, a hybrid GCP/local deployment with automated cost governance, an MCP server exposing its own capabilities as tools for other AI agents, and safety-gated automation across home, finance, and dev workflows.

**Architecture:** `5-tier LLM routing (Cerebras + NVIDIA NIM) → Skill Engine (38 auto-discovered) → MCP Server → GCP Hybrid Deploy → Native Desktop HUD`

**Technical highlights:**
- MCP server exposing NEXUS capabilities as tools for external AI agents
- Hybrid cloud/local architecture on a free-tier GCP VM (Tailscale tunnel, service-account impersonation) running core services 24/7, with automated cost-guard cutoff against the free-tier limit
- Home automation (IoT), personal finance parsing (bank email summaries), and passive security monitoring (process/port/USB/auth anomaly detection) — all active in daily use
- Dev-workflow automation: test runner, log triage, build, natural-language code generation with validation
- Safety-first design: confirmation-gated system power control, allowlisted automation, passive-only monitoring
- Custom-trained wake word (ONNX, no PyTorch) and cloned voice via ElevenLabs with local fallback

`Python 3.11` `MCP` `GCP` `Cerebras` `NVIDIA NIM` `ChromaDB` `Native Desktop HUD`

---

### 🏠 [SAVI v2 — Autonomous Real Estate Valuation](https://github.com/Julian-Rincon/ames-housing-ml) · [Live Demo](https://julian-rincon.github.io/ames-housing-ml/SAVI_v2_ParcialFinal.html) `🟢 Active`

*Team project — with Valeria Larea, Nicolás Garzón, and Juan Niño, for our Machine Learning course.*

> Architected a full Reinforcement Learning pipeline that moves beyond price prediction into autonomous risk-based decision making. Three RL agents trained in sequence — consensus policy determines the final APPROVE / REVIEW / REJECT verdict.

**Pipeline:** `K-Means segmentation → XGBoost pricing (R²=0.9609) → MDP Value Iteration (259 iter) → Q-Learning tabular (8K episodes) → Double DQN PyTorch (150 epochs) → Consensus policy`

**Results:** 93.1% auto-approved · 6.9% escalated · IEEE technical paper delivered

`XGBoost` `PyTorch` `MDP` `Q-Learning` `DQN` `K-Means` `scikit-learn`

---

### 🛒 [ShopStream — AWS Big Data Pipeline](https://github.com/Julian-Rincon/shopstream-bigdata) `✅ Done`

> Engineered a production-grade end-to-end data pipeline for a fictional e-commerce platform on AWS. Every layer is instrumented, tested, and deployed via CI/CD.

**Architecture:** `Python datagen (2.5M events) → S3 partitioned storage → Lambda validator (CloudWatch metrics + quarantine) → EMR/PySpark (6 analytics KPIs + anomaly detection) → Glue ETL → RDS PostgreSQL DWH → Flask API via Zappa`

**Engineering details:** 86% test coverage · GitHub Actions CI/CD · security group hardening on RDS

`PySpark` `AWS Lambda` `AWS EMR` `AWS Glue` `RDS PostgreSQL` `Flask` `Zappa` `pytest`

---

## All Projects

| Project | Description | Stack | Status |
|---------|-------------|-------|--------|
| [NEXUS](https://github.com/Julian-Rincon/NEXUS-Public) | Autonomous personal AI system: 5-tier LLM routing, 38 skills, GCP hybrid deploy, MCP server, home/finance/security automation | Python, MCP, GCP, Cerebras, NVIDIA NIM | 🟢 Active |
| [SAVI v2](https://github.com/Julian-Rincon/ames-housing-ml) | Full RL pipeline (MDP → Q-Learning → DQN) for autonomous real estate valuation. XGBoost R²=0.9609 · [Demo](https://julian-rincon.github.io/ames-housing-ml/SAVI_v2_ParcialFinal.html) · team project | XGBoost, PyTorch, MDP, DQN | 🟢 Active |
| [ShopStream](https://github.com/Julian-Rincon/shopstream-bigdata) | AWS Big Data pipeline: 2.5M events, Lambda, EMR/PySpark, Glue ETL, RDS, Flask/Zappa, CI/CD | PySpark, Lambda, Glue, EMR, Zappa | ✅ Done |
| Project Dogma | Team project (led by a classmate): stochastic social propagation simulator. Presented at Data Fest — Universidad Sergio Arboleda ([Rulo Científico](https://www.instagram.com/p/DYU3Q1BlUdn/)). No public repo. | TypeScript, React | — |
| [Chinook Cloud Platform](https://github.com/Julian-Rincon/chinook-cloud-platform) | React + FastAPI on EC2, Terraform IaC, Glue → Athena → Power BI star schema · team project with Juan Hurtado & David Martinez | AWS, Terraform, FastAPI, Glue | ✅ Done |
| [ML DSL with ANTLR4](https://github.com/Julian-Rincon/Proyecto-Final-L) | Custom language for ML workflows: regression, MLP, clustering, plots | Python, ANTLR4, scikit-learn | ✅ Done |
| [HPC Workshops](https://github.com/Julian-Rincon/HPC) | TSP brute force, Sobel edge detection, video processing, distributed TSP with Docker Swarm | Python, Docker Swarm | ✅ Done |
| [Network Traffic Analysis](https://github.com/Julian-Rincon/Analisis-de-Trafico-de-Red-con-PowerShell-y-Python) | 1.5h real traffic capture, heavy-tail analysis on 384K files | Python, PowerShell, Pandas | ✅ Done |

---

## Hackathons & Leadership

### 🤖 USABOT Robotics Challenge — 1st Place Overall `Nov 2025`

> Led hardware design and commercial strategy for an intelligent automatic irrigation system, winning first place overall at the USABOT Robotics Challenge against competing university teams.

**Technical contribution:** Designed the 3D hardware model for the physical prototype and integrated ultrasonic sensor architecture for real-time water level detection and automated valve control.

**Business contribution:** Authored and delivered the go-to-market strategy and commercial pitch — demonstrating that engineering solutions need to be sold, not just built.

`3D Modeling` `Sensor Integration` `Hardware Design` `Business Strategy` `Pitching`

---

### 🌐 [WarmiTics — Wisibilízalas, Universidad Pompeu Fabra](https://sites.google.com/view/warmitics) — 1st Place `2019`

> Served as **Technical PM and Lead Frontend/UX** for WarmiTics, a web platform highlighting women leaders in STEM. Won 1st Place at Wisibilízalas (organized by Universidad Pompeu Fabra, Barcelona), competing against teams from Latin America and Europe.

**Technical contribution:** Architected and developed the full web application; owned all frontend and UX decisions from information architecture to deployment.

**Leadership contribution:** Managed cross-functional logistics and stakeholder coordination; conducted structured interviews with women leaders in technology and ICT to gather primary content.

`Project Management` `Frontend/UX` `Stakeholder Management` `Social Impact`

---

## Currently Building

- **NEXUS** — In production daily. Actively expanding: deeper calendar/email automation, enhanced dev-workflow skills, broader MCP tool exposure for multi-agent orchestration
- **Internship Automation Pipeline** — LLM-scored job discovery across GetOnBoard + ATS sources, Telegram daily digest via n8n, Railway deploy
- **Next target:** ML Engineering or Data Engineering internship · MSc application Germany

---

## Education & Certifications

**Universidad Sergio Arboleda** — Bogotá, Colombia

*B.Sc. Computer Science & Artificial Intelligence* · 9th semester of 9 (final term) · 2021 – present

| Certification | Issuer | Date |
|---|---|---|
| AWS Academy Graduate — Data Engineering | Amazon Web Services | May 2026 |
| Database Programming with SQL | Oracle Academy | Dec 2024 |
| Database Design | Oracle Academy | Aug 2024 |

---

<div align="center">

**Open to ML Engineering / Data Engineering internships and research collaborations**

[julian-rincon.github.io](https://julian-rincon.github.io)

</div>
