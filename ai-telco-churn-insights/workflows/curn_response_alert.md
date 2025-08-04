# ⚙️ Workflow Title: Real-Time Churn Response Alert

## 🎯 Purpose
Detect churned customers (churn = "Yes") in real-time and alert the team to trigger proactive outreach.

## 🧩 Trigger
Google Sheets — Watch for Changes in `Churn` Column

## 🔗 Tools Used
- Google Sheets (Customer_Churn_Summary_by_Segment.csv)
- Gmail or Slack (Alert system)
- Google Sheets (churn_log.csv)

## 🔁 Step-by-Step Flow
1. **Module 1: Google Sheets — Watch Changes**
   - Sheet: Customer_Churn_Summary_by_Segment.csv
   - Condition: Churn value changed from "No" to "Yes"

2. **Module 2: Google Sheets — Add Row**
   - Target: churn_log.csv
   - Log churned customer’s info and timestamp

3. **Module 3: Gmail — Send Alert Email**
   - Subject: “Customer Churned: [Customer ID]”
   - Body: Details of the customer and recommended follow-up

## ✅ Expected Outcome
Immediate alerts when customers churn, allowing faster retention or follow-up actions.
