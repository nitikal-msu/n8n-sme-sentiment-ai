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
              ↓
      LINE Messaging API
