# 🏬 RETAIL ANALYTICS DASHBOARD: SALES, PROFITABILITY & CUSTOMER INSIGHTS

## Introduction
In today’s retail landscape, understanding the key drivers of sales, profitability, and customer behavior is essential for sustaining growth and maintaining competitiveness. The ability to identify what influences performance — from product categories to customer demographics — empowers decision-makers to act strategically and efficiently.

This dashboard was developed for Axis and Oak, a U.S.-based retail store dealing in books, clothing, electronics, and other consumer goods. The goal is to provide a clear snapshot of the store’s current business performance and uncover insights that will help executives determine where to focus effort and resources for maximum impact.

◼ Financial Overview
 - Evaluate overall financial performance, including revenue, profit, and trend over time.
 - Assess the total number of transactions and analyze the ratio of sales to returns to measure efficiency.

◼ Product and Store Insights
 - Identify the most profitable product categories and subcategories.
 - Compare product and store performance in terms of sales volume, profit margin, and contribution to total revenue.

◼ Customer Insights
 - Analyze the average number of transactions per customer to gauge engagement and loyalty.
 - Measure sales contribution by gender and distribution of customers by state.
 - Determine the most profitable age group to guide marketing and inventory decisions.

---
## 🔄 Process Flow

Data Preparation (MySQL):
The raw retail data was cleaned and transformed in MySQL to ensure consistency and accuracy across all tables — including transactions, customers, products, and dates.

Data Modeling (Power BI):
The cleaned datasets were imported into Power BI, where relationships were defined between fact and dimension tables to create a robust star schema model.

Data Visualization & Analysis:
With the model established, interactive visuals and KPIs were developed in Power BI to highlight trends, relationships, and performance metrics across sales, profit, and customer dimensions.

---

## 🗂️ Dataset Overview

The data model follows a Star Schema, consisting of one central fact table and supporting dimension tables, ensuring efficient relationships and calculations within Power BI.

🟥 Fact Table: Transactions
 - Transaction_ID – Unique identifier for each transaction
 - Cust_ID – Links each transaction to a specific customer
 - Tran_Date – Transaction date (used to connect with the Date table)
 - Prod_Cat_Code / Prod_Sub_Cat_Code – Identify product category and subcategory
 - Qty, Rate, Tax, Total_Amt – Metrics for financial calculations
 - Profit_Margin_%, Profit – Indicators of product-level profitability
 - Store_Type – Channel or store type (e.g., online, in-store)
 - Transaction_Status – Indicates sale or return

🟥 Dimension Table: Customer
 - Customer_ID, DOB, Gender, City_Code

🟥 Dimension Table: Product_Category
 - Prod_Cat_Code, Prod_Cat, Prod_Sub_Cat_Code, Prod_SubCat, Profit_Margin_%

🟥 Dimension Table: Date_Table
 - Date, Month, Quarter, Year, MonthNumber, DayOfWeek

