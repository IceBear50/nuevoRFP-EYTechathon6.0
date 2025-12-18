# nuevoRFP-EYTechathon6.0

# 🚀 NuevoRFP — Intelligent RFP Automation Platform

> **Automate RFP discovery, evaluation, prioritization, and response generation using agentic AI.**

NuevoRFP is a configurable, agent-driven system designed to help seller organizations **identify the right RFPs, evaluate feasibility, prioritize opportunities, and generate professional response documents** — all with traceability and business control.

Built for **EY Techathon** with extensibility toward real-world enterprise use.

---

## 🧠 Why NuevoRFP?

RFP handling today is:
- Manual and time-consuming
- Heavily dependent on tribal knowledge
- Difficult to prioritize objectively
- Error-prone and non-auditable

NuevoRFP replaces this with a **structured, explainable, and configurable decision pipeline**.

---

## 🧩 Core Architecture (Agent-Driven)

NuevoRFP operates using **four specialized agents**, coordinated by a central orchestrator:

### 🧭 1. Sales Agent
- Scans procurement portals and vendor websites for RFPs
- Tracks submission deadlines within a configurable time window
- Extracts high-level metadata (client, scope, due date)
- Shortlists RFPs worth evaluating further

### 🧠 2. Master Agent (Orchestrator)
- Coordinates the full workflow
- Triggers document ingestion and downstream agents
- Resolves conflicts between technical, pricing, and strategy inputs
- Applies final prioritization logic

### 🛠️ 3. Technical Agent
- Parses RFP documents (digital + scanned PDFs via OCR)
- Extracts technical requirements and line items
- Matches requirements against internal SKU catalogs
- Scores technical compliance and confidence

### 💰 4. Pricing Agent *(partially implemented / extensible)*
- Evaluates commercial feasibility
- Factors in cost drivers, risks, and testing requirements
- Produces inputs for bid/no-bid decisions

---

## ⚙️ Configurable RISP Scoring Engine (MVP → Next Round)

NuevoRFP introduces a **RISP (Relative Importance Scoring & Prioritization)** engine that allows sellers to control decision logic.

### Example configurable weights:
- 🧑‍💼 Existing client relationship — `0.20`
- 💵 Revenue potential — `0.30`
- ⚠️ Delivery / risk complexity — `0.15`
- 🛠️ Technical confidence — `0.25`
- 📅 Timeline feasibility — `0.10`

👉 Sellers can **tune these weights** without changing code.

---

## 📄 Automated Response Generation

Once an RFP is approved:
- Selected SKUs and compliance data are consolidated
- A **professional, submission-ready PDF response** is generated
- Includes audit-friendly language and traceability
- Generated using `ReportLab` (no external system dependencies)

---

## 🖥️ Frontend Capabilities (React)

- 📤 Upload RFP PDFs
- 📊 View matched SKUs and confidence levels
- 🟢 Visual compliance indicators (Full / Review)
- 🕓 Activity history & session restore
- 📄 One-click response PDF generation

---

## 🧱 Tech Stack

### Frontend
- ⚛️ React (Vite)
- 🎨 Tailwind CSS
- 🔐 Clerk Authentication

### Backend
- ⚡ FastAPI
- 🧠 Agent orchestration (Crew-style execution)
- 📄 OCR + PDF parsing
- 📑 ReportLab for document generation

---

## 📌 Current MVP Scope

✅ RFP upload & ingestion  
✅ OCR support for scanned PDFs  
✅ SKU matching & confidence scoring  
✅ Agent-based orchestration  
✅ Configurable decision logic (foundation)  
✅ Automated response PDF generation  

---

## 🚧 Planned Next-Round Enhancements

- 🌐 Live web-scraping of procurement portals
- ⏰ Deadline-aware RFP discovery
- 🧮 Full RISP weight UI for sellers
- 📊 Opportunity ranking dashboard
- 🧾 Approval workflows & audit logs
- 🔁 Feedback loop to improve matching accuracy

---

## 🎯 Vision

NuevoRFP is designed to evolve into a **decision intelligence platform for enterprise sales teams**, enabling:

> **“Bid on the right RFPs, for the right reasons, every time.”**

---

## 👥 Team & Hackathon Context

This project was built as part of **EY Techathon**, focusing on:
- Real-world feasibility
- Explainability
- Enterprise readiness
- Clear upgrade path beyond MVP

---

## 📜 License

This repository is intended for hackathon evaluation and demonstration purposes.

---

⭐ *If this project resonates with you, feel free to star the repo or reach out for collaboration.*
