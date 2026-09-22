# 🚀 Automated SME Customer Sentiment Analysis

> An AI-powered workflow automation solution for processing customer messages, generating responses, analyzing sentiment, and organizing customer feedback for SME businesses.

---

## 📌 Project Overview

**Automated SME Customer Sentiment Analysis** is an AI-powered workflow automation project designed to support Small and Medium-sized Enterprises (SMEs) in managing customer messages and feedback more efficiently.

The workflow is built with **n8n** and integrates **LINE Official Account**, **Google Sheets**, and **Google Gemini** to automate the customer-feedback processing flow.

When a customer sends a message, the workflow receives the event through a webhook, retrieves relevant product information from Google Sheets, and uses Google Gemini to generate an appropriate response.

Depending on the workflow conditions, customer feedback can also be sent through a sentiment analysis process. The analysis result is stored in Google Sheets, and potentially negative feedback is routed to an alert process for further attention.

This project demonstrates how **Generative AI, workflow automation, API integration, conditional logic, and structured data management** can be combined to support a practical customer-service process.

<img width="1600" alt="Automated SME Customer Sentiment Analysis Workflow" src="https://github.com/user-attachments/assets/addb4df4-9232-4a2e-bf9f-1e290a7f7703" />

---

## 🎯 Project Objectives

The project aims to:

- Automate the processing of customer messages.
- Assist in generating responses to customer inquiries.
- Analyze customer feedback using AI-powered sentiment analysis.
- Identify potentially negative customer feedback.
- Store customer interactions and review results in a structured format.
- Reduce repetitive manual work in customer-feedback processing.
- Connect customer communication, AI processing, and business data within one workflow.
- Provide a foundation for future customer-service analytics and dashboards.

---

## 💡 Business Problem

SMEs often use messaging platforms such as LINE to communicate with customers.

As customer interactions increase, businesses may need to manually:

1. Read incoming customer messages.
2. Check product information.
3. Understand customer intent.
4. Prepare an appropriate response.
5. Identify customer complaints or negative feedback.
6. Record customer feedback for later analysis.

Handling these activities manually can become repetitive and make it difficult to maintain structured customer-feedback data.

### 💡 Proposed Solution

This project uses **n8n as the central automation platform** to connect customer communication, product information, AI processing, sentiment analysis, data storage, and notification logic into a single workflow.

The overall process is:

```text
Customer Message
       ↓
LINE Official Account
       ↓
Webhook
       ↓
Get Product Data
       ↓
Google Gemini
Generate Response
       ↓
Check for Review
       │
       ├── No Review
       │      ↓
       │  Save Interaction
       │
       └── Review Required
              ↓
        Sentiment Analysis
              ↓
        Save Review Data
              ↓
       Check for Negative
              ↓
        Alert if Required

## 🛠️ Tech Stack & Tools
* **Workflow Automation:** n8n (Node-based automation)
* **AI & NLP:** GenAI / LLM APIs (for sentiment classification)
* **Data Sources/Integrations:** LINE OA API, Webhooks
* **Storage/Dashboarding:** Google Sheets / BI Tools

## 💡 Key Highlights & Business Impact
* **Zero Manual Intervention:** Fully automated end-to-end pipeline that eliminates manual data extraction, tagging, and logging.
* **Real-World Deployment:** Successfully deployed and tested with **6 active SME test users**.
* **Actionable Insights:** Enables business owners to immediately identify negative feedback and respond in real-time.

## 📂 Repository Contents
* `workflow_export.json`: The raw n8n workflow file. (You can easily import this into your local n8n instance to see the pipeline structure).
* *(Note: All API keys and sensitive credentials have been replaced with placeholders e.g., `YOUR_LINE_CHANNEL_ACCESS_TOKEN` for security purposes).*

## ⚙️ How to Use
1. Install [n8n](https://n8n.io/).
2. Go to the workflows tab and click **Import from File**.
3. Select the `.json` file from this repository.
4. Re-configure the credentials (LINE API, LLM API) to test the workflow.

## 📊 Live Dashboards & Previews
## 🔗 Direct Project Links
Click the badges below to directly view the live data outputs:

[![Looker Studio](https://img.shields.io/badge/Looker_Studio-Live_Dashboard-blue?style=for-the-badge&logo=googlecloud&logoColor=white)](https://datastudio.google.com/s/lmC0nS_JDuM)

[![Google Sheets](https://img.shields.io/badge/Google_Sheets-Database_View-green?style=for-the-badge&logo=googlesheets&logoColor=white)](https://docs.google.com/spreadsheets/d/1XqixdYgmsd9SPp59CxfjZl82ogS9keV7bbKVPh8ZVj8/edit?usp=sharing)
              ↓
      LINE Messaging API
