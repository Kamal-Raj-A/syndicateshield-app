# 🛡 SyndicateShield
### Mule Account Network Detection Platform

> **HackHustle CODE KNIGHT 2026** · Saveetha Engineering College · TechSociety  
> Domain: Fintech · Track: Fraud Detection & Financial Security

---

## 📌 Problem Statement

Every UPI scam, investment fraud, and job scam in India uses **mule accounts** to layer and move stolen money. Banks monitor accounts individually — but mule accounts look completely normal in isolation. The fraud only becomes visible when you detect **behavioral synchrony across multiple accounts simultaneously**.

-  **₹11,269 Crore** lost to cyber fraud in India in 2024
-  **85%** of all digital fraud routed through mule account networks
-  **1.8 crore** UPI fraud victims (RBI Annual Report 2024)
-  **<3%** of stolen funds ever recovered

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

|  Current Bank Systems |  SyndicateShield |
|---|---|
| Monitors accounts one by one | Monitors the entire network simultaneously |
| Reacts after money moves | Detects while money is still moving |
| Rule-based threshold alerts | ML-powered behavioral scoring (40+ features) |
| Hours to flag | Under 4 minutes |

---

## 🖥 Live Demo

> 🔗 **https://syndicateshield-app.vercel.app/**

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
|  **SDG 16** — Peace, Justice & Strong Institutions | Directly supports law enforcement in dismantling financial crime networks |
|  **SDG 10** — Reduced Inequalities | Protects rural and semi-urban Indians who are most targeted by UPI scams |
|  **SDG 9** — Industry, Innovation & Infrastructure | AI-powered fintech innovation for India's ₹200T digital payment ecosystem |
|  **SDG 8** — Decent Work & Economic Growth | Secures digital financial trust enabling safe economic participation |

---

## 🚀 Run Locally

```bash
# Clone the repository
git clone https://github.com/Kamal-Raj-A/syndicateshield-app.git

# Navigate into the folder
cd syndicateshield

# Open in browser — no dependencies needed
open index.html
```

> The prototype is a single self-contained HTML file. No npm install, no build step, no server needed. Just open in any modern browser.

---
## Demo Screenshots

<img width="1919" height="912" alt="Screenshot 2026-03-20 092847" src="https://github.com/user-attachments/assets/48e76d73-1854-44e1-9cad-dcb09f6a0c7c" />
<img width="1919" height="965" alt="Screenshot 2026-03-20 092957" src="https://github.com/user-attachments/assets/2179e1d6-4243-4849-b2db-999937635414" />
<img width="1919" height="903" alt="Screenshot 2026-03-20 093020" src="https://github.com/user-attachments/assets/48f30123-a5e3-4b79-ad09-c81dd3479dd2" />
<img width="1919" height="899" alt="Screenshot 2026-03-20 093041" src="https://github.com/user-attachments/assets/95270562-39e8-4a75-b05c-d4ce50402e03" />
<img width="1919" height="895" alt="Screenshot 2026-03-20 093121" src="https://github.com/user-attachments/assets/b4c0603b-7227-498f-8d60-dcefd4b7ac52" />
<img width="1919" height="907" alt="Screenshot 2026-03-20 093154" src="https://github.com/user-attachments/assets/72398f88-4733-45d9-b739-18dccf221dd5" />
<img width="1919" height="906" alt="Screenshot 2026-03-20 093232" src="https://github.com/user-attachments/assets/41a8f66d-db07-4414-8208-4f7561e69ee4" />

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
