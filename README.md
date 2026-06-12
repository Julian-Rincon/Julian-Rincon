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

8th-semester CS & AI student at Universidad Sergio Arboleda, working at the intersection of machine learning engineering, distributed data infrastructure, and autonomous AI systems. My stack runs on real AWS infrastructure and a Linux workstation — not just notebooks.

```python
julian = {
    "focus":    ["ML Engineering", "Data Engineering", "Autonomous Agents", "Stochastic Systems"],
    "building": [
        "Jarvis IronMan — dual-brain local AI (Ollama routing + Gemini reasoning)",
        "SAVI v2     — autonomous valuation via RL pipeline (MDP → Q-Learning → DQN)",
        "ShopStream  — end-to-end AWS Big Data pipeline (Lambda → EMR → Glue → RDS)",
        "Dogma       — stochastic social propagation engine (Markov + HMM + Nash)",
    ],
    "stack":    ["Python", "PySpark", "PyTorch", "AWS", "Terraform", "FastAPI", "TypeScript"],
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

### 🧠 [Jarvis IronMan](https://github.com/Julian-Rincon/Jarvis-Public) — Dual-Brain Local AI Assistant `🟢 Active`

> Engineered a fully offline AI assistant on Linux (Fedora KDE) with a two-model inference architecture: **Ollama** handles sub-200ms local intent routing while **Gemini API** resolves complex multi-step reasoning — zero cloud dependency for the core pipeline.

**Architecture:** `Mic → Whisper STT → Pre-LLM Router → Ollama/Gemini → Skill Engine → Piper TTS → HUD`

**Technical highlights:**
- ZeroMQ multiprocessing IPC separating STT, LLM, and TTS processes
- 12 active skills including Gmail/Calendar OAuth2, Playwright browser automation, Telegram remote control
- Wake-word detection via openwakeword with STT fallback
- ChromaDB vector memory in development

`Python 3.11` `Whisper` `Ollama` `Gemini API` `Playwright` `ZeroMQ` `tkinter` `ChromaDB`

---

### 🏠 [SAVI v2 — Autonomous Real Estate Valuation](https://github.com/Julian-Rincon/ames-housing-ml) · [Live Demo](https://julian-rincon.github.io/ames-housing-ml/SAVI_v2_ParcialFinal.html) `🟢 Active`

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

### 🎲 Project Dogma — Stochastic Social Propagation Engine `✅ Done`

> Built a mathematically rigorous simulation of ideological propagation across an urban social graph. Four distinct mathematical models govern every layer of the system.

**Mathematical architecture:**
- **Dynamic Markov Chains** — agent state transitions (Neutral → Believer → Fanatic) modulated by solitude, skepticism, and charisma variables
- **Hidden Markov Model (Forward algorithm)** — authority behavior inferred from latent states via observable Heat entropy signal
- **Verhulst Logistic Differential Equation** — resource carrying capacity K generating natural S-curve propagation
- **Nash Equilibrium (2×2 mixed strategy, 55%/45%)** — schism resolution eliminating dominant pure strategies

**Validation:** 500 Monte Carlo simulations · μ=152 ticks · conversion 5.42 agents/tick (σ=0.39) · retention ratio 38:1

`TypeScript` `React` `Markov Chains` `HMM` `Game Theory` `Monte Carlo`

---

## All Projects

| Project | Description | Stack | Status |
|---------|-------------|-------|--------|
| [Jarvis IronMan](https://github.com/Julian-Rincon/Jarvis-Public) | Dual-brain local AI: Ollama routing + Gemini reasoning, Whisper STT, Piper TTS, full skill ecosystem | Python, Whisper, Ollama, Gemini, ZeroMQ | 🟢 Active |
| [SAVI v2](https://github.com/Julian-Rincon/ames-housing-ml) | Full RL pipeline (MDP → Q-Learning → DQN) for autonomous real estate valuation. XGBoost R²=0.9609 · [Demo](https://julian-rincon.github.io/ames-housing-ml/SAVI_v2_ParcialFinal.html) | XGBoost, PyTorch, MDP, DQN | 🟢 Active |
| [ShopStream](https://github.com/Julian-Rincon/shopstream-bigdata) | AWS Big Data pipeline: 2.5M events, Lambda, EMR/PySpark, Glue ETL, RDS, Flask/Zappa, CI/CD | PySpark, Lambda, Glue, EMR, Zappa | ✅ Done |
| Project Dogma | Stochastic social simulation: Markov Chains + HMM + Nash Equilibrium + Monte Carlo | TypeScript, React, Game Theory | ✅ Done |
| [Chinook Cloud Platform](https://github.com/Julian-Rincon/chinook-fullstack) | React + FastAPI on EC2, Terraform IaC, Glue → Athena → Power BI star schema | AWS, Terraform, FastAPI, Glue | ✅ Done |
| [ML DSL with ANTLR4](https://github.com/Julian-Rincon/Proyecto-Final-L) | Custom language for ML workflows: regression, MLP, clustering, plots | Python, ANTLR4, scikit-learn | ✅ Done |
| [HPC Workshops](https://github.com/Julian-Rincon/HPC) | TSP brute force, Sobel edge detection, video processing, distributed TSP with Docker Swarm | Python, Docker Swarm | ✅ Done |
| [Network Traffic Analysis](https://github.com/Julian-Rincon/Analisis-de-Trafico-de-Red-con-PowerShell-y-Python) | 1.5h real traffic capture, heavy-tail analysis on 384K files | Python, PowerShell, Pandas | ✅ Done |

---

## Currently Building

- **Jarvis v2** — Migrating to Gemini (LLM + STT + Vision), adding meeting agent skill (autonomous interview representation), calendar integration from internship pipeline
- **Internship Automation Pipeline** — LLM-scored job discovery across GetOnBoard + ATS sources, Telegram daily digest via n8n, Railway deploy
- **Next target:** ML Engineering or Data Engineering internship · MSc application Germany

---

## Education & Certifications

**Universidad Sergio Arboleda** — Bogotá, Colombia

*B.Sc. Computer Science & Artificial Intelligence* · 8th semester · 2021 – present

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
