# Workflow Architecture

### Workflow 1 — Lead Capture API
Webhook → Validation → Google Sheets → Confirm Response

### Workflow 2 — AI Lead Scoring
Normalize → Rule Score → Groq AI Score → Merge → Calculate priority

### Workflow 3 — Auto Reply
AI draft → Gmail → Log History

### Workflow 4 — Follow-Up Automation
Daily scheduler → Conditional filters → Gmail messages

### Workflow 5 — High Priority Alert
Priority filter → Email alert → HotLeads sheet

### Workflow 6 — Weekly Report
Weekly schedule → Stats calculation → Summary email
