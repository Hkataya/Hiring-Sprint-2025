# 🚗 AI-Powered Vehicle Condition Assessment — Hiring Sprint

> **⏱️ Duration:** 48 hours
> **🎯 Purpose:** Build a working prototype that automates vehicle condition inspections for rental businesses (cars, scooters, boats, equipment).
> **👥 Format:** Solo or team participation.

---

## 🧭 Table of Contents

1. [Overview](#-overview)
2. [Deliverables & Checklist](#-deliverables--checklist)
3. [Judging Criteria](#-judging-criteria)
4. [Technical Requirements](#-technical-requirements)
5. [Repository Guidelines](#-repository-guidelines)
6. [Deployment Requirements](#-deployment-requirements)
7. [API Specification](#-api-specification)
8. [AI / LLM Resources](#-ai--llm-resources)
9. [Frontend Recommendations](#-frontend-recommendations)
10. [Testing & Bonus Points](#-testing--bonus-points)
11. [Security & Privacy](#-security--privacy)
12. [Submission Instructions](#-submission-instructions)
13. [FAQ & Tips](#-faq--tips)

---

## 🧩 Overview

Challenge developers to design and implement an **AI-powered vehicle condition assessment** feature. The system should enable customers to capture photos at **pick-up and return**, automatically detect damages, and display reports.

**Accepted formats:** web app 🌐, mobile app 📱, or chatbot 🤖.
Use of pretrained AI/ML models or APIs is **allowed** ✅.

**The goal:**

* Capture/upload vehicle images.
* Detect & compare damages between pick-up and return.
* Estimate severity & cost 💰.
* Display results in a simple, intuitive dashboard.
* Provide APIs for integration.

---

## 📦 Deliverables & Checklist

Each submission **must include**:

| Deliverable                 | Description                                           |
| --------------------------- | ----------------------------------------------------- |
| 🌐 **Deployed Service URL** | Publicly accessible link or Docker image instructions |
| 💻 **GitHub Repo**          | All code, infra configs, and setup steps              |
| 📘 **Documentation**        | README, API docs (OpenAPI/GraphQL), AI model notes    |
| 🎥 **Video Walkthrough**    | 2–5 minute demo showing capture → detection → report  |
| 🔑 **Demo Credentials**     | Username/password or tokens (in `.env.example`)       |

**Submission checklist:**

* [ ] Deployed URL
* [ ] GitHub repo (link)
* [ ] Architecture diagram
* [ ] API docs
* [ ] Model integration notes
* [ ] Walkthrough video
* [ ] Test plan / sample tests

---

## 🏁 Judging Criteria (100 pts)

| Criteria                 | Points | Description                                    |
| ------------------------ | ------ | ---------------------------------------------- |
| ⚙️ Functionality         | 40     | End-to-end working prototype                   |
| 🧠 AI Accuracy           | 20     | Detects and highlights new damages             |
| 🎨 UX & Design           | 15     | Clean, intuitive, aligned with rental workflow |
| 🧩 Engineering Quality   | 10     | Structure, docs, and reproducibility           |
| 🔌 Integration Readiness | 5      | API clarity and documentation                  |
| 💡 Innovation & Extras   | 10     | Bonus features or creative additions           |

**Tiebreakers:** demo clarity, documentation quality, deployment reliability.

---

## ⚙️ Technical Requirements

* **Timeframe:** 48 hours ⏰
* **Photo Capture:** browser/mobile camera APIs (no external SDKs)
* **AI Models:** pretrained or API-based (YOLO, Detectron, Vision APIs)
* **Damage Comparison:** side-by-side or overlay visual diff 🆚
* **Reporting:** JSON + UI (severity, estimated cost)
* **API:** REST or GraphQL endpoints
* **Privacy:** no real customer data, mask sensitive info

---

## 📁 Repository Guidelines

```
/ (root)
├── README.md
├── /docs
│   ├── architecture.md
│   ├── api-schema.yaml
├── /backend
├── /frontend
├── /models
├── /infra
├── /tests
├── .env.example
├── Dockerfile
└── docker-compose.yml
```

Include:

* `CONTRIBUTING.md` (team guide)
* `LICENSE` (MIT recommended)
* CI/CD pipeline (GitHub Actions optional)

---

## ☁️ Deployment Requirements

### 🌐 Web App

* Deploy via **Cloud Run**, **Render**, **Vercel**, or **Netlify**.
* Include `Dockerfile` & `.env.example`.
* Must be publicly accessible or runnable via Docker.

### 📱 Mobile App

* Use **React Native/Expo** or **Flutter**.
* Provide simulator instructions or TestFlight/Expo link.

### 🤖 Chatbot UI

* Host a minimal web chat interface accepting image uploads.
* Display damage detection summaries.

📘 Include setup steps in `docs/deployment.md`.

---

## 🔗 API Specification (Suggested)

| Method | Endpoint                      | Description                                   |
| ------ | ----------------------------- | --------------------------------------------- |
| `POST` | `/api/inspections`            | Create new inspection (upload pick-up images) |
| `POST` | `/api/inspections/:id/return` | Upload return images & trigger comparison     |
| `GET`  | `/api/inspections/:id`        | Retrieve inspection results (JSON + UI)       |
| `GET`  | `/api/inspections`            | List all inspections for a vehicle            |

💡 **Tip:** Include Swagger/OpenAPI docs or GraphQL schema + curl samples.

---

## 🧠 AI / LLM Resources

**Cloud APIs:**

* ☁️ Google Cloud Vision
* 🔍 Azure Computer Vision
* 🧩 AWS Rekognition

**Hosted APIs:**

* 🤖 OpenAI Vision / GPT-4V
* 🧬 Hugging Face / Replicate (YOLO, DETR, SAM)

**Open Source Models:**

* 🦾 YOLOv8 / YOLOv7
* 🧩 Detectron2 / Mask R-CNN
* 🖼️ Segment Anything (SAM)
* 🎯 Grounding DINO

**LLM Integration Ideas:**

* Convert model output → human-readable summary
* Example: *“Detected new scratch on front bumper; estimated repair cost: $80.”*

---

## 💅 Frontend Recommendations

**Core Flow:** Vehicle info → photo capture → AI detection → damage report

**UX Tips:**

* Side-by-side comparison with highlight overlays 🔍
* Manual correction (false positive/negative)
* Exportable PDF/JSON reports 📄
* Mobile-first UI 📱

**Stacks:**

* Web: **React (Next.js/Vite) + Tailwind CSS**
* Mobile: **React Native + Expo** or **Flutter**
* Chatbot: **React + Chat UI + image upload**

---

## 🧪 Testing & Bonus Points

| Bonus Area                 | Points |
| -------------------------- | ------ |
| ✅ Automated tests          | +20    |
| 🔁 CI/CD pipeline          | +10    |
| 📊 Model evaluation        | +10    |
| 📶 Offline capture/sync    | +10    |
| 🧩 Explainability features | +10    |

Include instructions to run tests (`npm test`, `pytest tests/`, etc.)

---

## 🔒 Security & Privacy

* Mask/blur license plates & personal data 🕵️‍♂️
* Store minimal image data 🔐
* Use `.env` for all API keys 🔑
* Add a `DELETE` API for image cleanup ♻️

---

## 🚀 Submission Instructions

1. Finalize repo → PR to `main` branch.
2. Tag release: `v1-hackathon` 🏷️
3. Include deployed URL + walkthrough video in release notes.
4. Submit via the official sprint form before deadline.

⏰ **Deadline:** exactly 48 hours after kickoff. Late submissions are not accepted unless due to verified platform issues.

---

## 💬 FAQ & Tips

**Q:** Can we use stock/synthetic images?
**A:** ✅ Yes, label them clearly.

**Q:** Is custom training required?
**A:** ❌ No. Use pretrained or API-based models.

**Q:** How do we estimate cost?
**A:** 💰 Rule-based model or LLM mapping.

**Tip:** Plan first 6–8 hours for setup & architecture, then focus on MVP.

---

## 🧮 Example Cost Function

```js
const COST_BY_SEVERITY = {
  minor: 50,
  moderate: 150,
  severe: 450
};

function estimateCost(detections) {
  return detections.reduce(
    (sum, d) => sum + COST_BY_SEVERITY[d.severity || 'moderate'],
    0
  );
}
```

---

> 🏁 **Good luck!** Build smart, fast, and ethically. Let your prototype redefine rental inspections 🚀.
