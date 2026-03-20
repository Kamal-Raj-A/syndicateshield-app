# 🛡 SyndicateShield
### Mule Account Network Detection Platform

> **HackHustle CODE KNIGHT 2026** · Saveetha Engineering College · TechSociety  
> Domain: Fintech · Track: Fraud Detection & Financial Security

---

## 📌 Problem Statement

Every UPI scam, investment fraud, and job scam in India uses **mule accounts** to layer and move stolen money. Banks monitor accounts individually — but mule accounts look completely normal in isolation. The fraud only becomes visible when you detect **behavioral synchrony across multiple accounts simultaneously**.

- 🔴 **₹11,269 Crore** lost to cyber fraud in India in 2024
- 🔴 **85%** of all digital fraud routed through mule account networks
- 🔴 **1.8 crore** UPI fraud victims (RBI Annual Report 2024)
- 🔴 **<3%** of stolen funds ever recovered

**No existing bank system does cross-account temporal correlation detection in real time.**

---

## 💡 Our Solution

SyndicateShield is a real-time mule account network detection platform that identifies fraud syndicates **before money laundering completes** — not after.

### How It Works — 3-Layer ML Pipeline

```
VICTIM TRANSFER
      ↓
[Layer 1] Isolation Forest
      → Detects dormancy-burst anomaly per account
      ↓
[Layer 2] XGBoost Classifier
      → Scores every account 0–100 on 40+ behavioral features every 5 min
      ↓
[Layer 3] DBSCAN Clustering
      → Groups high-risk accounts into coordinated syndicates
      ↓
FREEZE RECOMMENDATION + EVIDENCE PACKAGE → < 4 minutes
```

| ❌ Current Bank Systems | ✅ SyndicateShield |
|---|---|
| Monitors accounts one by one | Monitors the entire network simultaneously |
| Reacts after money moves | Detects while money is still moving |
| Rule-based threshold alerts | ML-powered behavioral scoring (40+ features) |
| Hours to flag | Under 4 minutes |

---

## 🖥 Live Demo

> 🔗 **[syndicateshield.vercel.app](https://your-deployment-link.vercel.app)**

### Demo Walkthrough
1. Open the dashboard → Click **▶ RUN FRAUD SIMULATION**
2. Watch Isolation Forest detect dormancy-burst anomaly in real time
3. Watch XGBoost scores climb as mule pattern is confirmed
4. Watch DBSCAN cluster 9 accounts into Syndicate #47
5. Click **⬡ FREEZE ALL 9 ACCOUNTS** → ₹3,12,400 intercepted
6. Click any account → Full XGBoost feature breakdown modal
7. Navigate to **◎ Geo Map** → Click Simulate Propagation
8. Navigate to **▦ Analytics** and **◈ ML Metrics** pages

---

## 🧠 Features

| Page | What It Shows |
|---|---|
| **⬡ Dashboard** | Live account monitoring, animated transaction graph, particle money flow, fraud simulation, freeze recommendation |
| **◎ Geo Map** | India fraud propagation map — animated arcs spreading city-to-city in real time |
| **▦ Analytics** | 30-day detection chart, risk score distribution, fraud category breakdown, top flagged accounts |
| **◈ ML Metrics** | Precision / Recall / F1 live bars, Confusion Matrix, ROC Curve (AUC 0.94), XGBoost feature importance |

---

## ⚙️ Tech Stack

| Layer | Technologies |
|---|---|
| **Frontend** | React.js, D3.js, WebSockets, React Native |
| **Backend** | Python, FastAPI, Celery, Redis |
| **ML Models** | Isolation Forest (scikit-learn), XGBoost, DBSCAN, Pandas, NumPy |
| **Database** | TimescaleDB, PostgreSQL, Redis Cache |
| **Data Pipeline** | Apache Kafka, PaySim Dataset (6.3M transactions), Synthetic Mule Simulator |
| **Cloud / Infra** | AWS EC2, AWS S3, Vercel, GitHub |

---

## 📊 Model Performance

| Metric | Score |
|---|---|
| **Precision** | 0.91 |
| **Recall** | 0.87 |
| **F1 Score** | 0.89 |
| **AUC-ROC** | 0.94 |
| **Avg Detection Time** | < 4 minutes |

**Confusion Matrix (n = 10,900 test samples)**

|  | Predicted Mule | Predicted Normal |
|---|---|---|
| **Actual Mule** | 847 ✅ TP | 127 ❌ FN |
| **Actual Normal** | 84 ❌ FP | 9,842 ✅ TN |

---

## 🌍 UN Sustainable Development Goals

| SDG | Alignment |
|---|---|
| ⚖️ **SDG 16** — Peace, Justice & Strong Institutions | Directly supports law enforcement in dismantling financial crime networks |
| 📉 **SDG 10** — Reduced Inequalities | Protects rural and semi-urban Indians who are most targeted by UPI scams |
| 💡 **SDG 9** — Industry, Innovation & Infrastructure | AI-powered fintech innovation for India's ₹200T digital payment ecosystem |
| 💼 **SDG 8** — Decent Work & Economic Growth | Secures digital financial trust enabling safe economic participation |

---

## 🚀 Run Locally

```bash
# Clone the repository
git clone https://github.com/your-username/syndicateshield.git

# Navigate into the folder
cd syndicateshield

# Open in browser — no dependencies needed
open index.html
```

> The prototype is a single self-contained HTML file. No npm install, no build step, no server needed. Just open in any modern browser.

---

## 📁 Project Structure

```
syndicateshield/
├── index.html          # Full prototype — Dashboard, Geo Map, Analytics, ML Metrics
├── README.md           # This file
└── assets/             # Screenshots (optional)
```

---

## 📚 References & Dataset

- **PaySim Dataset** — Kaggle (6.3M synthetic financial transactions for fraud simulation)
- **RBI Annual Report 2024** — Cyber fraud statistics and UPI fraud data
- **Indian Cyber Crime Coordination Centre (I4C)** — Mule account network data
- **XGBoost** — Chen & Guestrin, 2016 — Scalable and accurate boosting classifier
- **DBSCAN** — Ester et al., 1996 — Density-based spatial clustering for syndicate mapping
- **Isolation Forest** — Liu et al., 2008 — Anomaly detection for dormancy-burst patterns

---

## 👥 Team

> Team Name: **Neuro Sprint**  
> College: Saveetha Engineering College, Chennai  
> Hackathon: HackHustle CODE KNIGHT 2026

| Name | Role |
|---|---|
| KAMAL RAJ A | ML Pipeline & Backend |
| SANDHIYA P | Frontend & Dashboard |
| YUVARAJ V | Data Engineering & Research |
| LAVANYA S | System Design & Presentation |

---

<div align="center">
  <strong>Built for HackHustle CODE KNIGHT 2026 🛡</strong><br>
  <em>Detecting syndicates. Protecting India.</em>
</div>
