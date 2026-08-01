# AI Lead Analyzer

## Overview

AI Lead Analyzer is an automation workflow built with n8n that automatically evaluates incoming leads using Google Gemini AI.

The system receives lead information through a webhook, analyzes the lead's intent and business potential, assigns a lead score, categorizes the lead as Hot, Warm, or Cold, stores the results in a database, and notifies the sales team.

---

## Features

* Receive leads through Webhook API
* AI-powered lead analysis using Google Gemini
* Automatic lead scoring (0–100)
* Lead categorization:

  * Hot Lead
  * Warm Lead
  * Cold Lead
* AI-generated reasoning for every score
* Store lead data in PostgreSQL
* Send email notifications for high-value leads
* Daily analytics and reporting

---

## Workflow

Webhook
↓
Receive Lead Data
↓
Google Gemini Analysis
↓
Generate:

* Lead Score
* Lead Category
* Reasoning
  ↓
  Store in PostgreSQL
  ↓
  Send Email Alert
  ↓
  Generate Analytics

---

## Sample Input

```json
{
  "name": "John Smith",
  "email": "john@abccompany.com",
  "budget": "50000",
  "message": "We need 500 custom t-shirts for our company event next month."
}
```

## Sample Output

```json
{
  "lead_category": "Hot",
  "lead_score": 92,
  "reasoning": "The lead shows strong purchase intent, clear requirements, a large order quantity, and a realistic budget."
}
```

---

## Tech Stack

* n8n
* Google Gemini AI
* PostgreSQL
* Webhooks
* Gmail / Email Notifications
* JSON APIs

---

## Database Fields

| Field         | Description        |
| ------------- | ------------------ |
| name          | Lead Name          |
| email         | Lead Email         |
| budget        | Budget Mentioned   |
| message       | Lead Inquiry       |
| lead_category | Hot / Warm / Cold  |
| lead_score    | AI Generated Score |
| reasoning     | AI Analysis        |
| received_at   | Lead Timestamp     |

---

## Use Cases

* Lead Qualification
* Sales Automation
* Customer Inquiry Analysis
* Marketing Campaign Evaluation
* CRM Enrichment

---

## Future Improvements

* WhatsApp Integration
* Facebook Lead Ads Integration
* CRM Integration
* Dashboard Analytics
* Multi-Agent Lead Analysis
* PDF Report Generation

---

## Author

Dhinesh

AI Automation Developer | n8n | Gemini AI | RAG Systems
