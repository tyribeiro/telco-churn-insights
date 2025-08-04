# ⚙️ Workflow Title: Personalized Retention Email Campaign

## 🎯 Purpose
Generate personalized, AI-written retention emails for high-risk customers flagged by churn risk analysis.

## 🧩 Trigger
New entry added to churn_risk_log.csv with status = High Risk

## 🔗 Tools Used
- Google Sheets (churn_risk_log.csv)
- OpenAI (Email prompt generation)
- Gmail (Send custom retention email)

## 🔁 Step-by-Step Flow
1. **Module 1: Google Sheets — Watch New Rows**
   - Sheet: churn_risk_log.csv
   - Filter: Risk = High

2. **Module 2: OpenAI — Prompt Completion**
   - Prompt: “Write a friendly, personalized email to a customer with high churn risk. Their tenure is [X], monthly bill is [Y], and they use [Z] services.”
   - Output: Email body

3. **Module 3: Gmail — Send Email**
   - Recipient: Customer Email
   - Subject: “We’re here for you, [First Name]”
   - Body: Output from OpenAI

## ✅ Expected Outcome
Stronger customer engagement and improved retention through human-like personalized outreach.