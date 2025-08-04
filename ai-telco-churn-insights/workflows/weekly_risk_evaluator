# ⚙️ Workflow Title: Weekly Churn Risk Evaluator

## 🎯 Purpose
Evaluate new customer records weekly and classify them as high or low churn risk using AI, enabling early intervention and customer retention efforts.

## 🧩 Trigger
Scheduled: Every Monday at 8:00 AM PST

## 🔗 Tools Used
- Google Sheets (churn_weekly.csv)
- OpenAI (Prompt-based risk assessment)
- Gmail (Email summary to team)

## 🔁 Step-by-Step Flow
1. **Module 1: Google Sheets — Search Rows**
   - Sheet: churn_weekly.csv
   - Filter: created_at is within the last 7 days

2. **Module 2: OpenAI — Prompt Completion**
   - Input: Customer details (tenure, monthly charges, contract type)
   - Prompt: “Evaluate churn risk and classify as high or low”
   - Output: Risk category + rationale

3. **Module 3: Google Sheets — Add Row**
   - Target: churn_risk_log.csv
   - Log: Customer ID, risk classification, rationale, timestamp

4. **Module 4: Gmail — Send Email**
   - Recipient: Customer Experience Manager
   - Subject: “Weekly Churn Risk Report”
   - Body: Summary of high-risk accounts

## ✅ Expected Outcome
Weekly digest of high-risk customers for immediate review and engagement.
