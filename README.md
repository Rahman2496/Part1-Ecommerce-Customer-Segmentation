# E-Commerce Customer Segmentation using RFM and K-Means Clustering

## Project Overview

This project focuses on customer segmentation for an e-commerce business using RFM analysis and K-Means clustering.

The main goal of the project is to help the company understand customer purchasing behavior, identify high-value customers, improve customer retention, and create targeted marketing strategies.

The project uses transaction-level e-commerce data to perform:

- Data Cleaning
- Feature Engineering
- Exploratory Data Analysis (EDA)
- RFM Analysis
- Customer Segmentation
- Business Recommendations

---

# Business Problem

The e-commerce company wants to:

- Understand customer purchasing behavior
- Identify valuable customer groups
- Improve customer retention
- Design personalized marketing campaigns
- Increase overall sales and profitability

Customer segmentation helps the business target different customer groups more effectively.

---

# Dataset Description

The dataset contains e-commerce transaction records.

Each row represents a single product purchased in a transaction.

## Dataset Columns

- InvoiceNo → Unique invoice number
- StockCode → Product identifier
- Description → Product name
- Category → Product category
- Quantity → Number of units purchased
- InvoiceDate → Date and time of transaction
- UnitPrice → Price per unit
- CustomerID → Unique customer identifier
- Country → Customer country

---

# Data Cleaning Summary

The following cleaning steps were performed:

- Removed duplicate records
- Removed rows with missing CustomerID
- Removed rows with missing product descriptions
- Removed cancelled invoices
- Removed transactions with zero or negative quantity
- Removed transactions with zero or negative price
- Converted InvoiceDate to datetime format
- Created Revenue column

These steps ensured the dataset was accurate and suitable for analysis.

---

# Feature Engineering

Customer-level features were created from transaction-level data.

## Features Created

- TotalRevenue
- TotalPurchases
- TotalQuantity
- AverageOrderValue
- UniqueProducts
- Country

## RFM Features

- Recency → How recently the customer purchased
- Frequency → How often the customer purchased
- Monetary → Total amount spent by the customer

---

# Exploratory Data Analysis (EDA)

EDA was performed to understand customer and sales behavior.

## Key Insights

- Certain countries generated significantly higher revenue than others.
- Some products contributed heavily to total sales volume.
- A small number of customers generated a large portion of revenue.
- Purchase frequency distribution showed that most customers purchased only a few times.
- Outliers existed in quantity, revenue, and unit price.

---

# Customer Segmentation using K-Means

K-Means clustering was applied on RFM features.

## Steps Performed

1. Selected RFM features
2. Scaled the data using StandardScaler
3. Used the Elbow Method to determine optimal clusters
4. Applied K-Means clustering
5. Assigned cluster labels to customers

---

# Cluster Interpretation

## Cluster 1 — High Value Loyal Customers

- Highest spending customers
- Frequent buyers
- High customer value
- Important for long-term retention

### Recommendations
- Loyalty rewards
- VIP membership
- Personalized recommendations
- Exclusive offers

---

## Cluster 0 — Regular / Occasional Buyers

- Moderate purchase frequency
- Medium spending behavior
- Potential to become loyal customers

### Recommendations
- Promotional campaigns
- Product bundles
- Repeat purchase discounts
- Cross-selling strategies

---

## Cluster 2 — Inactive / At-Risk Customers

- High recency
- Low engagement
- Low purchase frequency
- Risk of customer churn

# Recommendations
- Win-back campaigns
- Reminder emails
- Discount coupons
- Re-engagement marketing

---

# Business Recommendations

- Focus on retaining high-value customers
- Use personalized marketing campaigns
- Target inactive customers with re-engagement offers
- Promote top-selling products strategically
- Use customer segmentation regularly for marketing decisions

---

# Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

# How to Run the Project

1. Clone the repository
2. Install dependencies

```bash
pip install -r requirements.txt