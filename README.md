# 🧠 Credit Risk Prediction - Bank GoodCredit

> A Data Science project for predicting customer creditworthiness and minimizing credit default risk using ensemble learning and domain-driven feature engineering.

![Project Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![Tech Stack](https://img.shields.io/badge/TechStack-Python%20%7C%20Pandas%20%7C%20Sklearn%20%7C%20SQL-blue)
![Model Type](https://img.shields.io/badge/Model-Ensemble%20Classifier-lightgrey)

---

## 📌 Project Overview

**Client:** Bank GoodCredit  
**Domain:** Banking - Risk & Credit Scoring  
**Goal:** Develop a predictive model to determine whether a credit card customer is likely to default.  
**Target Variable:** `Bad_label`  
- `0`: Good Credit History  
- `1`: Bad Credit History (30+ DPD)

---

## 📊 Dataset Description

- **Cust_Account:** Historical account & payment behavior
- **Cust_Enquiry:** Credit enquiries, purposes, and amounts
- **Cust_Demographics:** Anonymized demographic features

📂 **Total Features Used**: 66  
🔐 **Data Source**: MySQL database with controlled access

---

## 🚀 Project Pipeline

### 1. 🔍 Data Exploration & Cleaning
- Merged and joined customer tables
- Handled missing values and outliers
- Conducted univariate & bivariate analysis

### 2. ✨ Feature Engineering
Selected impactful features based on gain, trend logic & domain knowledge:

| Feature | Description | Gain |
|--------|-------------|------|
| `payment_history_avg_dpd_0_29_bucket` | Mean count of accounts with 0–29 DPD | 0.0456 |
| `utilisation_trend` | Credit balance vs. limits trend | 0.0375 |
| `count_enquiry_recency_365` | Enquiries in last 365 days | 0.0362 |
| `min_months_last_30_plus` | Min months before 30+ DPD | 0.0382 |

> 📌 Total of 20+ high-performing, custom-engineered features

### 3. 🤖 Model Building
- Tried Logistic Regression, Random Forest, and Gradient Boosting
- Best result from **Ensemble Model** using XGBoost

📈 **Evaluation Metric**: Gini Coefficient  
🎯 **Benchmark Gini**: 0.379  
📊 **Model Decile Ranking** (Top 3 shown):

| Decile | Response Rate |
|--------|----------------|
| 10 | 11.71% |
| 9 | 8.05% |
| 8 | 6.00% |

---

## 🧾 Project Deliverables

- 🔧 Feature Matrix with gain values
- 📑 Model Evaluation (Gini, Decile rank)
- 💡 Risk-Based Customer Segmentation
- 📦 SQL + Python scripts for data extraction and model scoring

---

## 💡 Key Takeaways

- Domain knowledge and feature engineering played a crucial role.
- Ensemble models significantly improved rank ordering.
- The model can reduce defaults by focusing on high-risk segments effectively.

---

## 📂 Folder Structure


