# 🚗 AI-Powered Vehicle Condition Assessment — Hiring Sprint

## 📚 Table of Contents

1. [Overview](#-overview)
2. [Goal / Business Requirements](#goal--business-requirements)
3. [Deliverables](#deliverables)
4. [Selection Criteria](#selection-criteria)
5. [Technical Requirements](#technical-requirements)
6. [Deployment Requirements](#deployment-requirements)
7. [Bonus Points](#bonus-points)
8. [Resources](#resources)
9. [Pro Tips / Implementation Notes](#-pro-tips--implementation-notes)

---

## 🧩 Overview

Build a working prototype for **AI-powered vehicle condition assessment**. The system should allow users to capture/upload vehicle images at pick-up and return, automatically detect damages, and display a report.

The solution can be a **web** or **mobile** app. Use of pretrained AI/ML models or APIs is allowed.

---

## 🎯 Goal / Business Requirements

**Business Goal:** Automate and simplify vehicle condition inspections for rental businesses (cars, scooters, boats, equipment). Enable customers and staff to:

- Capture/upload vehicle images at pick-up and return
- Detect and compare damages between pick-up and return
- Estimate severity and cost of damages
- Display results in a dashboard or report
- Integrate with 3rd party systems via API

**Example Workflow:**

1. Customer picks up a car, takes photos via the app.
2. On return, new photos are taken.
3. The system compares images, highlights new damages, and estimates repair costs.
4. A summary report is shown in the UI and available via API.

---

## 📦 Deliverables

- Deployed Service URL: Public link or Docker run instructions
- UI: Web or mobile interface for image upload, damage detection, and report display
- API: REST or GraphQL endpoint for 3rd party integration (API documentation is a bonus)
- Dockerfile: Required for reproducible deployment
- README: Setup and usage instructions
- Demo Credentials: If authentication is required, provide sample credentials in `.env.example`
- Video Walkthrough: 2–5 minute demo (optional but recommended)

---

## 🏆 Selection Criteria

- Functionality: End-to-end working prototype
- AI Accuracy: Detects and highlights new damages
- UX & Design: Clean, intuitive, and fits rental workflow
- Engineering Quality: Structure, docs, and reproducibility
- Integration Readiness: API clarity and documentation
- Innovation & Extras: Bonus features or creative additions

---

## ⚙️ Technical Requirements

- Frontend: Web or mobile UI is required
- Backend: Any language/framework is allowed
- API: Must provide an endpoint for 3rd party integration
- API Documentation: Bonus points for OpenAPI/Swagger or GraphQL docs
- Deployment: Must be publicly accessible or runnable via Docker
- Dockerfile: Required
- Testing: Optional, but bonus points for automated tests
- CI/CD: Optional, but bonus points for integration
- Mobile Deployment: If cloud deployment is not possible, share the APK or Expo link
- No persistent storage required: Simulate uploads and results in memory

---

## ☁️ Deployment Requirements

- Free to deploy anywhere: [Vercel](https://vercel.com/), [Netlify](https://www.netlify.com/), [Render](https://render.com/), [Google Cloud Run](https://cloud.google.com/run), [Hugging Face Spaces](https://huggingface.co/spaces), etc.
- Dockerfile is required for reproducibility
- CI/CD integration is a huge plus
- For mobile apps, if cloud deployment is not possible, share the APK or Expo link

---

## 💎 Bonus Points

- Testing: Automated tests + instructions to run them
- Documentation: API docs (Swagger/OpenAPI/GraphQL)
- CI/CD: Pipeline for automated deployment

---

## 🛠️ Resources

### Deployment Free Resources

- [Vercel](https://vercel.com/) — Web frontend
- [Netlify](https://www.netlify.com/) — Web frontend
- [Render](https://render.com/) — Web or backend
- [Google Cloud Run](https://cloud.google.com/run) — Backend containers
- [Hugging Face Spaces](https://huggingface.co/spaces) — Web / AI demos
- [Expo](https://expo.dev/) — React Native mobile apps

### LLM / AI APIs (Free Tiers)

- [Hugging Face Inference API](https://huggingface.co/inference-api)
- [Replicate](https://replicate.com/)
- [Google Cloud Vision](https://cloud.google.com/vision)
- [OpenAI GPT-4V](https://platform.openai.com/docs/guides/vision)
- [Roboflow](https://roboflow.com/)

---

## 📝 Pro Tips / Implementation Notes

**1. Frontend Choice (Web vs Mobile)**

- Pick one: web or mobile.
- Web: React + Next.js or Vite + Tailwind works well.
- Mobile: React Native (Expo) is easiest; Flutter is also fine.
- Mobile deployment: Expo link or APK if cloud hosting isn’t possible.

**2. Backend / API**

- Single endpoint approach works great: upload **before** and **after** images → return JSON with damages.
- Stateless: process images in memory, no storage required.
- Any language/framework is allowed (Node.js, Python, Go, etc.).

**3. AI / Damage Detection**

- Use **pretrained models**: YOLOv8, Detectron2, Segment Anything + Grounding DINO, or Hugging Face/Replicate APIs.
- Optional: LLM (OpenAI GPT-4V) for generating human-readable summaries or severity estimation.
- Compare “before” and “after” images to identify **new damages only**.

**4. UI / Reporting**

- Show **side-by-side images** with highlights on new damages.
- Include JSON summary for API consumption.
- Optional: downloadable PDF or CSV report.

**5. Tips & Tricks**

- Focus on MVP first; nice-to-have features come later.
- Keep AI inference async if using slow models.
- Use `.env.example` for all API keys.
- Screen record your workflow for demo clarity.

---

> 🏁 **Good luck!** Focus on a **working prototype**, clear UI, and AI-powered inspection summary. Make it fast, ethical, and demo-ready 🚀
