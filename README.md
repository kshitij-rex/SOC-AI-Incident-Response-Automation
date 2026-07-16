# SOC-AI-Incident-Response-Automation

An end-to-end Security Operations Center (SOC) automation project that integrates Splunk SIEM, Elastic Defend,  n8n, Google Gemini AI, AbuseIPDB,  and Slack to automate alert enrichment, analyst approval, and endpoint isolation.

---

## 📌 Project Overview

Security Operations Center (SOC) analysts often spend valuable time manually investigating alerts, enriching Indicators of Compromise (IOCs), notifying analysts, and performing endpoint containment.

This project automates the complete incident response workflow after a high-severity alert is generated.

The workflow receives alerts from Splunk via Webhook, enriches indicators using AbuseIPDB, performs AI-powered incident analysis with Google Gemini, requests analyst approval through Slack, and automatically isolates the affected endpoint using Elastic Defend after approval.

This demonstrates how AI-assisted automation can reduce analyst workload, improve response time, and standardize incident handling while still keeping a human-in-the-loop for critical response actions.

---

## 🏗 Workflow Architecture
```text
Splunk Alert
      │
      ▼
Webhook (n8n)
      │
      ▼
Google Gemini AI
(Alert Summary & Severity)
      │
      ▼
AbuseIPDB
(IOC Enrichment)
      │
      ▼
Slack Analyst Approval
      │
 ┌────┴────┐
 │         │
Approve   Reject
 │         │
 ▼         ▼
Elastic   Slack Notification
Defend
(Isolate Host)
 │
 ▼
Slack Confirmation
```

---

## ✨ Key Features

- Automated incident response workflow using n8n
- AI-powered incident summarization using Google Gemini
- IOC enrichment using AbuseIPDB
- Analyst approval workflow through Slack
- Automatic endpoint isolation using Elastic Defend
- Human-in-the-loop decision making
- Reject path with analyst notification
- REST API integration with AbuseIPDB, Google Gemini AI, Slack, and Elastic Defend

# 📸 Project Demonstration

## 1. Complete Automation Workflow

![Workflow](screenshots/n8n-workflow.png)


---

## 2. Analyst Approval via Slack

![Slack Approval](screenshots/Slack-approval.png)

---

## 3. Analyst Approved

![Approved](screenshots/analyst-approved.png)



## 4. Endpoint  Isolation

![Isolated](screenshots/host-isolated.png)

---

## 5. Endpoint Successfully Isolated

![Isolated](screenshots/elastic-host-isolated.png)

---

## 6. Successful n8n Workflow Execution

![Execution](screenshots/n8n-successful-execution.png)

---

## 7. Analyst Rejected

![Rejected](screenshots/analyst-rejected.png)

---

## 8. Rejected n8n Workflow Execution

![Rejected](screenshots/reject-workflow.png)

---

## 9. Endpoint Unisolation

![Released](screenshots/host-released-successful.png)

---

## 10. Endpoint Successfully Released

![Released](screenshots/elastic-host-released.png)

---
