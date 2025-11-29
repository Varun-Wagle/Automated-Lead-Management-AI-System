# 🚀 Automated Lead Management & AI Follow-Up System
This project demonstrates a full real-world AI-powered lead automation pipeline built using n8n (self-hosted), Groq LLM, Google Sheets, and Gmail API.

The system handles:
• Lead intake via Webhook API
• Rule-based + AI lead scoring
• Automated personalized email replies
• Priority-based follow-ups
• High-priority alerts for founders/sales teams
• Weekly analytics summary reports

## 🔧 Tech Stack
| Tool                  | Purpose                                             |
| --------------------- | --------------------------------------------------- |
| **n8n**               | Workflow automation platform (Docker local install) |
| **Groq (LLama 3.3)**  | AI lead scoring + message generation                |
| **Google Sheets API** | Lead database + tracking                            |
| **Gmail OAuth**       | Email dispatch for replies & alerts                 |
| **Postman**           | API testing                                         |
| **JavaScript**        | Decision logic & workflow scripting                 |

## 🧩 Workflow Overview
### ✅ Workflow 1 — Lead Capture API
• Accepts incoming leads via Webhook POST API
• Validates payload
• Stores clean data into Leads Sheet

### ✅ Workflow 2 — Lead Scoring (AI + Rules)
• Applies scoring rules:
  - Budget tier
  - Source reliability
  - Service intent
  - Message seriousness
• Sends structured prompt to Groq
• Combines rule score + AI score
• Calculates:
  - leadScore (0-100)
  - priority (HIGH/MEDIUM/LOW)
  - follow-up schedule
• Updates database

### ✅ Workflow 3 — Instant Auto-Reply
• Generates personalized response email (AI or template)
• Sends immediately via Gmail
• Logs message history

### ✅ Workflow 4 — Follow-Up Scheduler
• Automated outreach:
  • 1-day follow-up
  • 3-day follow-up
  • 7-day follow-up
  • Skips if:
    - Lead replied
    - Lead closed
    - Follow-up already sent
    
### ✅ Workflow 5 — High Priority Alerts
• Triggers for leads marked HIGH priority
• Sends alert email to founder/sales team
• Adds record to “Hot Leads” sheet
• Marks alerts as completed to prevent duplicates

### ✅ Workflow 6 — Weekly AI Summary Report
• Every Monday:
  - Weekly new lead count
  - HIGH/MEDIUM/LOW breakdown
  - Follow-up statistics
  - Auto-reply stats
• Report delivered via email to sales/admin teams.

## 📊 System Architecture
POST API (Webhook)
       ↓
Google Sheets <←→ n8n Orchestration Engine ←→ Groq AI
       ↓
 Gmail API   +  Scheduler Triggers

## 🎯 Project Goals
✅ Build job-ready automation skills
✅ Implement real-world AI workflows
✅ Integrate OAuth APIs
✅ Practice model orchestration logic
✅ Create professional portfolio artifacts

## ✅ Outcome
✔ Fully automated AI lead processing system
✔ Handles hundreds of leads without manual work
✔ Demonstrates end-to-end system design ability

## 👨‍💻 Author
Varun Wagle
AI Automation Developer | n8n Specialist | Prompt Engineer

## 📬 Contact
[LinkedIn](https://www.linkedin.com/in/varunwagle/)
[Instagram](https://www.instagram.com/varun.wagle/)
[WhatsApp](https://wa.me/+91-9156095415)
