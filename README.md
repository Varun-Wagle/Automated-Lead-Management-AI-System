# 🚀 Automated Lead Management & AI Follow-Up System (n8n + Groq)

A **production-grade AI automation system** designed to capture, score, and nurture leads using fully-orchestrated workflows built in **n8n** with **Groq LLM integration**.

This project demonstrates end-to-end real-world automation engineering including:

✅ API-based lead intake  
✅ Rule-based + LLM lead scoring  
✅ AI-generated email replies  
✅ Multi-stage follow-up automation  
✅ High-priority lead alerts  
✅ Scheduled performance reporting

---

## ⚙️ Technology Stack

| Layer | Tools |
|------|-------|
| **Automation Engine** | n8n (Self-Hosted via Docker) |
| **LLM Scoring & Content** | Groq API (LLaMA-3.3-70B) |
| **Datastore / CRM** | Google Sheets API |
| **Email Delivery** | Gmail API (OAuth 2.0) |
| **Workflow Logic** | JavaScript |
| **Testing** | Postman |

---

---

## 🧠 System Architecture

![System Architecture](./diagram/system-architecture.png)

---

---

## 🔁 Workflow Breakdown

---

### ✅ Workflow 1 — Lead Capture API

Webhook API captures new inbound leads from:

• Website forms  
• CRMs / integrations  
• Direct API clients (Postman)

Validation & normalization occurs before storing into the **Google Sheets lead database**.

---

---

### ✅ Workflow 2 — Lead Scoring (Hybrid AI + Rules Engine)

Each lead is processed using both:

#### Rule-Based Scoring
Evaluates:
- Budget size
- Service intent
- Lead source reliability
- Message clarity & length

Produces a **Rule Score (0–60)**.

#### AI Scoring (Groq LLM)

The full lead profile is sent to Groq’s LLaMA-3.3 model to generate:

- **AI Score (0-100)**  
- Short quality reasoning

---

#### Combined Lead Intelligence Output

```json
{
  "leadScore": 0–100,
  "aiScore": 0–100,
  "priority": "HIGH | MEDIUM | LOW",
  "nextFollowUpAt": "ISO Timestamp",
  "scoredAt": "ISO Timestamp"
}
```

### ✅ Workflow 3 — Instant Auto-Reply

Immediately after scoring:

• Personalized email reply is generated
• Gmail API dispatches to the prospect
• Subject + content logged inside the CRM

### ✅ Workflow 4 — Follow-Up Automation

Scheduled campaigns trigger:

| Stage |	Timing |
|-------|-------|
| Follow-Up 1 |	+1 Day |
| Follow-Up 2 |	+3 Days |
| Follow-Up 3 |	+7 Days |

Emails are only sent if:

✅ Lead has not replied
✅ Lead is not marked closed
✅ Follow-up step hasn’t already been executed

### ✅ Workflow 5 — High-Priority Alerts

When:
```json
"priority": "HIGH"
```

The system instantly:

• Emails founder/sales team
• Adds record to Hot Leads List
• Locks lead to prevent duplicate alerts

### ✅ Workflow 6 — Weekly Analytics Summary

Every Monday:

• Total weekly leads
• Priority breakdowns
• Auto-reply & follow-up metrics
• Hot-lead alert counts

All statistics are emailed as a business performance report.

## 🛠️ Key Engineering Capabilities Demonstrated

✅ End-to-end workflow automation at production scale
✅ OAuth 2.0 API integrations (Google Sheets / Gmail)
✅ Prompt engineering & LLM output parsing
✅ Hybrid AI + deterministic decision systems
✅ Scheduled task orchestration
✅ Data normalization & merging pipelines
✅ Alerting systems & reporting loops
✅ Docker-based self-hosting

## 🎯 Business Value Delivered

This system replaces hours of weekly sales manual work by:

✔ Automating lead qualification
✔ Improving response speed
✔ Preventing opportunity loss
✔ Maintaining clean CRM records
✔ Ensuring hot-lead visibility

Perfect for:

• Marketing agencies
• SaaS sales teams
• Consultants
• Lead generation businesses

## 👨‍💻 Author
Varun Wagle
AI Automation Developer | Workflow Engineer | LLM Integrator

## 💬 Contact
Reach out on [LinkedIn]([https://](https://www.linkedin.com/in/varunwagle/) for collaborations or freelance AI automation projects.
