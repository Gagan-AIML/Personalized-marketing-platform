# AI-Driven Personalized Marketing Platform (Flask + AWS Ready)

This project is a full-stack **AI-Driven Personalized Marketing Platform** that allows marketers to:
- manage customers
- launch personalized marketing campaigns
- analyze campaign performance (open rate, click rate, conversions)
- use an **AI/ML recommendation option** (“AI Recommended”) for product selection
- prepare for AWS deployment using **DynamoDB** (storage) and **SNS** (notifications)

---

## Features

### ✅ Authentication
- Sign up / Login
- Session-based protected pages

### ✅ Customer Management
- Add customer (Customer ID, name, interest)
- Delete customer (and optionally remove their campaigns)

### ✅ Campaign Management
- Launch campaign to a customer
- Choose product manually OR select **AI Recommended**
- Delete campaigns

### ✅ Analytics Dashboard
- Stats cards: total campaigns, avg open rate, avg click rate, conversions
- Search and filter campaigns by customer
- Campaign table view

### ✅ AWS-Ready Version
- Uses DynamoDB tables for users/customers/campaigns
- Publishes notifications to SNS topic (optional)

---

## Where AI is Used

The **AI-driven part** is the recommendation step in campaign creation:

- When “AI Recommended” is selected, the platform uses a recommendation function/model to select the best product for a customer.
- In the local version, this can be rule-based or ML-based.
- The platform design supports improving recommendations over time using customer engagement metrics.

---

## Tech Stack
- **Frontend:** HTML + CSS
- **Backend:** Python Flask
- **AWS (cloud-ready):**
  - DynamoDB (Users, Customers, Campaigns tables)
  - SNS (notifications)

---
