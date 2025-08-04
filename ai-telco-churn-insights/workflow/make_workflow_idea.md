# 🔄 Make.com Workflow: Dual Trigger Automation for Telco Churn

This Make.com scenario is designed to monitor two conditions using a Google Sheet connected to your Telco churn data:

---

## 🟢 TRIGGER A: Watch **New Rows** (New Customers Added)
- **Module:** Google Sheets > Watch New Rows
- **Trigger Frequency:** Every 15 minutes (or adjust to your needs)
- **Purpose:** Detect new customer entries in the dataset.

### ✅ What It Does:
- When a new row is added (new customer), it will:
  - Send a Slack or Email alert
  - Optionally create a new CRM or Notion entry
  - Run the risk evaluation logic based on their contract, tenure, and charges

---

## 🔴 TRIGGER B: Watch **Churn Column Changes** (No → Yes)

- **Module:** Google Sheets > Watch Changes
- **Settings:**
  - **Field to monitor:** `Churn` column
  - **Condition:** Change from `No` → `Yes`

### ✅ What It Does:
- When an existing customer’s churn value updates to “Yes,” it will:
  - Trigger a Slack alert or internal team notification
  - Log the churned customer to a “churn_log” sheet
  - Kick off a potential follow-up email workflow

---

## 🧠 Filters & Logic

### After Watch Changes:
- **Filter:** `Churn (New)` equals `Yes`
- **AND:** `Churn (Old)` equals `No`

This ensures that only meaningful churn transitions are captured.

---

## 💬 Optional Slack Module (for both triggers)
- **Module:** Slack > Send Message
- **Message Template:**
  ```
  🔔 *Churn Alert*  
  Customer *{{Name}}* (ID: {{CustomerID}}) has churned.  
  Tenure: {{Tenure}} months  
  Monthly Charges: ${{MonthlyCharges}}  
  Contract: {{ContractType}}
  ```

---

## 📥 Data Source
Make sure your Google Sheet has the following columns:

- `CustomerID`
- `Churn`
- `Tenure`
- `MonthlyCharges`
- `ContractType`
- `PaymentMethod`
- `OnlineSecurity`
- `TechSupport`

---

## 📁 Suggested Sheet Tabs
- `Churn_Weekly` – active monitored sheet
- `Churn_Log` – historical log of churned customers

---
