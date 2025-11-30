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
• Accepts incoming leads via Webhook POST API<br>
• Validates payload<br>
• Stores clean data into Leads Sheet<br>

### ✅ Workflow 2 — Lead Scoring (AI + Rules)
• Applies scoring rules:<br>
  - Budget tier<br>
  - Source reliability<br>
  - Service intent<br>
  - Message seriousness<br>
• Sends structured prompt to Groq<br>
• Combines rule score + AI score<br>
• Calculates:<br>
  - leadScore (0-100)<br>
  - priority (HIGH/MEDIUM/LOW)<br>
  - follow-up schedule<br>
• Updates database<br>

### ✅ Workflow 3 — Instant Auto-Reply
• Generates personalized response email (AI or template)<br>
• Sends immediately via Gmail<br>
• Logs message history<br>

### ✅ Workflow 4 — Follow-Up Scheduler
• Automated outreach:<br>
  • 1-day follow-up<br>
  • 3-day follow-up<br>
  • 7-day follow-up<br>
  • Skips if:<br>
    - Lead replied<br>
    - Lead closed<br>
    - Follow-up already sent<br>
    
### ✅ Workflow 5 — High Priority Alerts
• Triggers for leads marked HIGH priority<br>
• Sends alert email to founder/sales team<br>
• Adds record to “Hot Leads” sheet<br>
• Marks alerts as completed to prevent duplicates<br>

### ✅ Workflow 6 — Weekly AI Summary Report
• Every Monday:<br>
  - Weekly new lead count<br>
  - HIGH/MEDIUM/LOW breakdown<br>
  - Follow-up statistics<br>
  - Auto-reply stats<br>
• Report delivered via email to sales/admin teams.<br>

## 📊 System Architecture
![System Architecture](./diagrams/system-architecture.png)

## 🎯 Project Goals
✅ Build job-ready automation skills<br>
✅ Implement real-world AI workflows<br>
✅ Integrate OAuth APIs<br>
✅ Practice model orchestration logic<br>
✅ Create professional portfolio artifacts<br>

## ✅ Outcome
✔ Fully automated AI lead processing system<br>
✔ Handles hundreds of leads without manual work<br>
✔ Demonstrates end-to-end system design ability<br>

## 👨‍💻 Author
Varun Wagle<br>
AI Automation Developer | n8n Specialist | Prompt Engineer

## 📬 Contact
[LinkedIn](https://www.linkedin.com/in/varunwagle/) | [Instagram](https://www.instagram.com/varun.wagle/) | [WhatsApp](https://wa.me/9156095415)
