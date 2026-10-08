# Telecom Customer Churn Prediction

## Project Overview

Telecom companies lose significant revenue when customers leave their services. Acquiring new customers can also be more expensive than retaining existing customers.

This project develops a Machine Learning solution to predict whether a telecom customer is likely to churn.

The solution estimates the probability of customer churn and classifies customers into:

- Likely to Churn
- Likely to Stay

The goal is to help the telecom company identify high-risk customers and provide proactive retention offers.

---

## Business Problem

The telecom company is facing customer churn and wants to identify customers who are likely to leave.

Every customer who leaves can result in:

- Loss of recurring revenue
- Reduced customer lifetime value
- Increased customer acquisition costs
- Loss of cross-selling opportunities

A predictive model can help the company identify high-risk customers before they leave.

---

## Dataset

The project uses the Telco Customer Churn dataset from Kaggle.

Dataset:
https://www.kaggle.com/datasets/blastchar/telco-customer-churn

The dataset contains customer demographic information, service information, contract details, billing information, and churn status.

### Target Variable

`Churn`

- `0` = Customer stayed
- `1` = Customer churned

---

## Features

The dataset contains customer information such as:

### Customer Information

- Gender
- Senior Citizen
- Partner
- Dependents
- Tenure

### Services

- Phone Service
- Multiple Lines
- Internet Service
- Online Security
- Online Backup
- Device Protection
- Tech Support
- Streaming TV
- Streaming Movies

### Contract and Billing

- Contract
- Paperless Billing
- Payment Method
- Monthly Charges
- Total Charges

---

## Project Workflow

```text
Dataset
   ↓
Data Understanding
   ↓
Data Cleaning
   ↓
Exploratory Data Analysis
   ↓
Feature Analysis
   ↓
Train-Test Split
   ↓
Feature Encoding & Scaling
   ↓
Logistic Regression
   ↓
Churn Probability Prediction
   ↓
Customer Classification
   ↓
Model Evaluation
   ↓
Business Analysis
   ↓
Retention Recommendation
```

---

## Data Cleaning

The following preprocessing steps were performed:

1. Loaded the Telco Customer Churn dataset.
2. Inspected the dataset structure.
3. Checked for missing values.
4. Converted `TotalCharges` into numeric format.
5. Removed records with missing `TotalCharges`.
6. Checked for duplicate records.
7. Removed `customerID` because it is an identifier and does not provide useful predictive information.
8. Converted the target variable:
   - `No` → `0`
   - `Yes` → `1`

The final cleaned dataset contains approximately 7,032 customer records and 20 columns.

---

## Exploratory Data Analysis

Customer churn was analyzed against several customer characteristics, including:

- Contract type
- Internet service
- Payment method
- Tenure
- Monthly charges
- Total charges
- Customer support services
- Security services
- Demographic characteristics

These analyses helped identify customer characteristics associated with different levels of churn.

---

## Machine Learning

### Algorithm

The project uses:

**Logistic Regression**

Logistic Regression was selected because the target variable is binary:

```text
0 → Stay
1 → Churn
```
