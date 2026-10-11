<div align="center">

# 💧 Borewell Ledger

### Know your groundwater before it runs dry.

A community groundwater early-warning platform for India, powered by serverless AWS and Amazon Bedrock.

[![Hackathon](https://img.shields.io/badge/WeMakeDevs%20×%20AWS-Environmental%20Hackathon%202024-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)](#)
[![Track](https://img.shields.io/badge/Track-Heat%20%26%20Water-0EA5E9?style=for-the-badge)](#)
[![Demo Video](https://img.shields.io/badge/▶%20Watch-Demo%20Video-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://youtu.be/T-XL3rzUCkU)
[![Live App](https://img.shields.io/badge/🌐%20Try-Live%20App-0A5C8A?style=for-the-badge)](https://main.d3kbqo47f82ouc.amplifyapp.com/home)

![Python](https://img.shields.io/badge/Python-3.12-3776AB?logo=python&logoColor=white)
![React](https://img.shields.io/badge/React-18-61DAFB?logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?logo=typescript&logoColor=white)
![AWS SAM](https://img.shields.io/badge/IaC-AWS%20SAM-FF9900?logo=amazonaws&logoColor=white)
![Bedrock](https://img.shields.io/badge/AI-Amazon%20Bedrock-232F3E?logo=amazonaws&logoColor=white)
![Tests](https://img.shields.io/badge/tests-39%20passing-brightgreen)

[**🌐 Live App**](https://main.d3kbqo47f82ouc.amplifyapp.com/home) · [**🎬 Demo Video**](https://youtu.be/T-XL3rzUCkU) · [**📖 Writeup**](docs/WRITEUP.md) · [**🏗️ Architecture**](docs/architecture.md)

</div>

---

## 📑 Table of Contents

- [Demo Video](#-demo-video)
- [Overview](#-overview)
- [Screenshots](#-screenshots)
- [Features](#-features)
- [Live URLs](#-live-urls)
- [Architecture](#️-architecture)
- [Quick Start](#-quick-start)
- [Analysis Rules](#-analysis-rules-deterministic)
- [AI Layer](#-ai-layer)
- [Repository Layout](#️-repository-layout)
- [Tech Stack](#️-frontend-tech-stack)
- [Cost Estimate](#-cost-estimate)
- [What Is Simulated](#-what-is-simulated--template-based)

---

## 🎬 Demo Video

[![Borewell Ledger Demo](https://img.youtube.com/vi/T-XL3rzUCkU/maxresdefault.jpg)](https://youtu.be/T-XL3rzUCkU)

> Click the thumbnail to watch the full walkthrough: https://youtu.be/T-XL3rzUCkU

---

## 📌 Overview

Groundwater is India's lifeline, yet most borewell owners have no way to tell whether their well is declining faster than their neighbours'. **Borewell Ledger** turns scattered depth-to-water readings into a shared early-warning system.

Housing societies, farmers, water officers and NGOs log readings from borewells. The platform then:

- 🗺️ Displays all wells on a **shared map**
- 📉 Calculates each well's **decline rate** and compares it with **nearby peers**
- 🚨 Raises **WATCH / CRITICAL** and **area-wide alerts**
- 🤖 Provides **AI analysis, water-saving plans and chat** via Amazon Bedrock
- 🌍 Supports **English, हिन्दी and ગુજરાતી**, with light and dark themes

> ### ⚠️ Demo Data Notice
> All data currently displayed is **simulated demo data**, labeled with a "Demo data" badge throughout the UI, in the About page data-sources table, and in this README. It does **not** represent real groundwater readings.

---

## 📸 Screenshots

### Get started in seconds, no account needed
Choose a role (Society Manager, Farmer, Water Officer / Panchayat, NGO / Volunteer) and a language, then dive in or explore the demo data.

<img width="1763" height="1154" alt="Screenshot_11-10-2026_112321_main d3kbqo47f82ouc amplifyapp com" src="https://github.com/user-attachments/assets/2a321e6e-c079-4051-87ed-dd417756e495" />

### Dashboard
Community overview with key stats, an **AI Insight of the Day**, wells that need attention, and recent alerts.

<img width="1763" height="3174" alt="Screenshot_11-10-2026_112341_main d3kbqo47f82ouc amplifyapp com" src="https://github.com/user-attachments/assets/026eacca-9ddc-4012-9610-1e0eabbf6f8c" />

### Shared Map
Every well on one map, colour-coded by status (Normal, Watch, Critical, No data), with filters, search and official-well markers.

<img width="1763" height="853" alt="Screenshot_11-10-2026_11241_main d3kbqo47f82ouc amplifyapp com" src="https://github.com/user-attachments/assets/520a1c51-5689-4e59-ad0a-b9982bf08c4c" />

### Wells
Search, sort by urgency and export to CSV. Each card shows depth, decline rate and the nearby peer median.

<img width="1763" height="844" alt="Screenshot_11-10-2026_112430_main d3kbqo47f82ouc amplifyapp com" src="https://github.com/user-attachments/assets/07e38cfd-4df8-4889-b6d5-c48e726c27e2" />

### Alerts
Transparent, rule-based alerts with the well's rate versus its peer median. Mark them seen or resolve them, and filter by All, New, Critical, Area-wide or Resolved.

<img width="1763" height="3764" alt="Screenshot_11-10-2026_112524_main d3kbqo47f82ouc amplifyapp com" src="https://github.com/user-attachments/assets/edcbe52b-c6b7-4683-a034-af34520915af" />

### AI Assistant
Ask questions about a specific well or all your wells. Every answer shows what it was based on (readings and nearby wells used).

<img width="1763" height="853" alt="Screenshot_11-10-2026_112542_main d3kbqo47f82ouc amplifyapp com" src="https://github.com/user-attachments/assets/97208a7e-d880-4be8-ac0c-8f60a99973f5" />

### Water-Saving Plan
An AI-generated action plan grouped into **This Week**, **This Month** and **Before Summer**, with effort levels and indicative cost ranges in ₹. Export it to PDF.

<img width="1763" height="1333" alt="Screenshot_11-10-2026_112614_main d3kbqo47f82ouc amplifyapp com" src="https://github.com/user-attachments/assets/daba9318-e69b-4fd8-93fc-6ef342cc8ea2" />

### Community Insights
A hotspot ranking of localities by median decline rate, plus **coverage gaps** with a one-click invite to add more wells.

<img width="1763" height="868" alt="Screenshot_11-10-2026_112625_main d3kbqo47f82ouc amplifyapp com" src="https://github.com/user-attachments/assets/004d10ef-e236-48ae-9e3f-ea0622f445b8" />

---

## ✨ Features

| Feature | Description |
|---|---|
| **Community Map** | Shared MapLibre map of wells with status colouring and filters |
| **Peer Comparison** | Each well's slope compared to the median of wells within 3 km |
| **Deterministic Alerts** | Transparent, unit-tested rules for WATCH, CRITICAL and area alerts |
| **Hotspot Ranking** | Localities ranked by median decline rate, with coverage-gap detection |
| **AI Analysis & Plans** | Nova Micro explains trends and suggests staged actions with cost ranges |
| **AI Chat** | Ask about a well, with server-computed sources |
| **Multilingual** | English, Hindi and Gujarati |
| **Role-Based Onboarding** | Society manager, farmer, water officer or NGO / volunteer |
| **Exports** | CSV of wells, PDF of water-saving plans |
| **Daily Analyzer** | EventBridge-scheduled Lambda re-evaluates all wells |
| **Email Alerts** | SNS notifications for critical and area-wide events |
| **Graceful Fallback** | Template advice when Bedrock is unavailable, clearly labeled |

---

## 🔗 Live URLs

| | |
|---|---|
| **Live App (HTTPS)** | https://main.d3kbqo47f82ouc.amplifyapp.com/home |
| **API** | https://r0kskruke2.execute-api.ap-south-1.amazonaws.com/prod |
| **Demo Video** | https://youtu.be/T-XL3rzUCkU |
| **S3 static site (legacy, HTTP)** | http://borewell-ledger-frontend-796973511540-prod.s3-website.ap-south-1.amazonaws.com |
| **App Region** | `ap-south-1` |
| **Bedrock Region / Model** | `us-east-1` / `amazon.nova-micro-v1:0` |

> **Note:** The app is hosted over **HTTPS on AWS Amplify**, so browser features that need a secure context, such as GPS ("Use My Location"), work. A CloudFront distribution (HTTPS, OAC, Price Class 100) is also defined in `template.yaml` as an alternative deployment path.

---

## 🏗️ Architecture

```
Browser → AWS Amplify Hosting (HTTPS, SPA)
Browser → API Gateway (HTTP API)  → Lambda (Python 3.12, arm64)
Lambda  → DynamoDB (on-demand, 4 tables)
Lambda  → SNS (email alerts)
Lambda  → Bedrock Converse API (AI)
EventBridge → Analyzer Lambda (daily schedule)
```

See [`docs/architecture.md`](docs/architecture.md) for the full Mermaid diagram.

### AWS Services

| Service | Purpose |
|---------|---------|
| **AWS Amplify Hosting** | HTTPS hosting for the React SPA |
| **S3 / CloudFront** | Static site bucket and optional HTTPS CDN (OAC, SPA fallback, Price Class 100) defined in the SAM template |
| **API Gateway (HTTP API)** | CORS-secured REST API, per-route throttling (burst 20, rate 10/s) |
| **Lambda (Python 3.12, arm64)** | 11 functions, no idle billing |
| **DynamoDB (on-demand)** | 4 tables: Wells, Readings, Alerts, Meta (TTL) |
| **EventBridge Scheduler** | Daily analyzer (`rate(1 day)`) |
| **SNS** | Email alerts for CRITICAL and area-wide events |
| **Amazon Bedrock** | Converse API with Nova Micro for analysis, plans and chat |
| **AWS SAM / CloudFormation** | Backend infrastructure defined in `template.yaml` |
| **AWS Budgets** | $5/month cost guard, separate from the app stack |

Forbidden services (NAT Gateway, EC2, ECS, RDS, OpenSearch, SageMaker, WAF, load balancers, provisioned DynamoDB, reserved Lambda concurrency) are **not used**.

---

## 🚀 Quick Start

**Prerequisites:** AWS CLI (configured), SAM CLI, Node 18+, Python 3.12+

```bash
git clone https://github.com/speedprav/borewell-ledger
cd borewell-ledger
bash scripts/deploy.sh
```

The deploy script is idempotent and will:

1. Run preflight checks (tools, credentials, Bedrock model access)
2. Create a cost-guard AWS Budget ($5/month, alerts at 50/80/100%)
3. Run `sam build && sam deploy` (Lambda, API Gateway, DynamoDB, SNS, S3, CloudFront, EventBridge)
4. Seed ~40 demo wells around Vadodara
5. Build the React frontend and sync it to S3
6. Invalidate CloudFront
7. Smoke-test every endpoint
8. Print the live URL

### Run the tests

```bash
cd backend
pytest        # 39 tests, all pure functions
```

### Tear down

```bash
bash scripts/teardown.sh
```

---

## 📊 Analysis Rules (Deterministic)

Documented and unit-tested in [`backend/common/analysis.py`](backend/common/analysis.py).

| Rule | Value |
|------|-------|
| Analysis window | Last 90 days |
| Minimum readings | 3 readings spanning 14+ days |
| Decline rate | OLS slope in metres/month (positive = water level falling) |
| Peer radius | 3 km (haversine) |
| Minimum peers | 3 wells with computed slopes |
| 🔴 **CRITICAL** | slope ≥ 0.8 m/mo **and** ≥ 2.5× peer median *(starting value)* |
| 🟡 **WATCH** | slope ≥ 0.3 m/mo **and** ≥ 1.5× peer median *(starting value)* |
| 🌐 **Area alert** | ≥ 5 wells in a locality with median slope ≥ 0.5 m/mo |
| Large jump warning | > 3 m change vs previous reading (flagged, not rejected) |

> Thresholds are **starting assumptions**, labeled as such on the app's About page.

---

## 🤖 AI Layer

- **Model:** Amazon Nova Micro (`amazon.nova-micro-v1:0`) via the Bedrock Converse API (`us-east-1`)
- **Fallback:** Every AI call falls back to deterministic template text, marked *"Template advice — AI unavailable"*, so the app works fully without Bedrock
- **Cost controls:** `maxTokens` 450 (analyze/plan) and 350 (chat); 24h response caching in the Meta table; daily caps of 300 total and 30 per hashed IP; temperature 0.3
- **Prompt safety:** User-provided text (names, notes, chat) is placed in delimited DATA BLOCK sections, and the model is instructed to treat it as data only
- **Trustworthy sources:** Chat `sources` (`readingsUsed`, `peersUsed`, `alertIdsReferenced`) are computed server-side, never by the model
- **Guardrail messaging:** Every AI screen states it is guidance only and not a substitute for professional hydrogeology advice

---

## 🗂️ Repository Layout

```
borewell-ledger/
├── template.yaml              # SAM: all infrastructure
├── samconfig.toml             # Non-secret defaults
├── backend/
│   ├── common/                # analysis, geo, validate, ddb, ai, ratelimit, templates
│   ├── handlers/              # map, wells, readings, alerts, community, admin,
│   │                          # ai_analyze, ai_plan, ai_chat, analyzer, health
│   └── tests/                 # pytest — 39 tests
├── frontend/                  # React 18 + Vite + TypeScript + Tailwind
├── scripts/
│   ├── preflight.sh           # Tool/credential check
│   ├── create_budget.sh       # AWS Budgets safeguard (run once)
│   ├── seed.py                # ~40 demo wells, idempotent, --reset flag
│   ├── deploy.sh              # Full one-command deploy
│   ├── smoke_test.sh          # Endpoint checks
│   └── teardown.sh            # Empty bucket + delete stack
└── docs/
    ├── screenshots/           # README screenshots
    ├── architecture.md        # Mermaid diagram
    ├── WRITEUP.md             # Hackathon submission writeup
    └── DEMO_SCRIPT.md         # 3-minute video script
```

---

## 🖥️ Frontend Tech Stack

React 18 · Vite · TypeScript · Tailwind CSS · React Router · MapLibre GL JS (OpenStreetMap tiles, attribution shown) · Recharts · lucide-react

---

## 💰 Cost Estimate

| Service | Monthly Cost |
|---------|-------------|
| Lambda (arm64, 256 MB, on-demand) | ~$0 (Free Tier) |
| DynamoDB (on-demand, low traffic) | ~$0 (Free Tier) |
| API Gateway (HTTP API) | ~$0 (Free Tier) |
| S3 + CloudFront / Amplify | ~$0 (Free Tier / low traffic) |
| SNS | ~$0 (Free Tier) |
| Bedrock (Nova Micro) | ~$0.01–$0.10 depending on usage |
| **Total** | **~$0 idle, < $1 with light demo use** |

---

## 🧪 What Is Simulated / Template-Based

- All demo data (41 wells and their readings), labeled `source: "seed"` throughout
- AI template fallbacks when Bedrock is unavailable, labeled "Template advice" in every response
- CRITICAL / WATCH thresholds, which are documented starting assumptions rather than hydrogeological standards

---

## 🛠️ AI Coding Tools Used

- **IBM Bob** (Claude Sonnet 3.5): primary agent that wrote the codebase
- **GitHub Copilot**: inline suggestions during manual edits

---

## 📚 Documentation

- [Live app](https://main.d3kbqo47f82ouc.amplifyapp.com/home)
- [Demo video on YouTube](https://youtu.be/T-XL3rzUCkU)
- [Project writeup](docs/WRITEUP.md)
- [Architecture diagram](docs/architecture.md)
- [Demo video script](docs/DEMO_SCRIPT.md)

---

<div align="center">

Built for the **WeMakeDevs × AWS Environmental Hackathon 2026** · Track: Heat and Water (Groundwater)

💧 *Every reading counts.*

</div>
