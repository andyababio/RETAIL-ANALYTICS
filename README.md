# RETAIL ANALYTICS DASHBOARD: SALES, PROFITABILITY & CUSTOMER INSIGHTS

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

Relevant relationships were then established between the above table to produce the following data model:
 <p align="center">
 <img alt="Data Model" src="https://github.com/andyababio/RETAIL-ANALYTICS/blob/main/Images/Retail%20Data%20Model.png" width="60%" />
 </p>
 
 ---
 
## 📊 Dashboard Overview  

<!-- Summary Page -->
<h3 align="center">Summary Page</h3>
<p align="center">
   <img src="https://github.com/andyababio/RETAIL-ANALYTICS/blob/main/Images/Dashboard.png" 
        alt="Dashboard" width="60%" />
</p>

<!-- Products & Customers Pages Side by Side -->
<h4 align="center">Products & Customer Page</h4>
<p align="center">
      <img src="https://github.com/andyababio/RETAIL-ANALYTICS/blob/main/Images/Products.png" 
           alt="Products" width="45%" />
      <img src="https://github.com/andyababio/RETAIL-ANALYTICS/blob/main/Images/Customer.png" 
           alt="Customer" width="45%" />
</p>


---
## Key Insights
### Summary Page:
<p> Overall Business Performance (Sales, Revenue, and Trends) </p>

- Axis and Oak demonstrates strong overall business performance, generating a cumulative **$54 million** in revenue and **$14 million** in profit since its inception in 2011.
 - The business achieves its peak performance in January, contributing the highest shares of **revenue (9%)**, **profit (9.01%)**, and **transactions (8.8%)**, indicating strong customer activity at the start of the year.
 - However, product returns have a notable financial impact, reducing total revenue by approximately 10%. Return volumes are highest in January and July, highlighting potential issues related to post-holiday or mid-year product cycles that may warrant closer review.

<p> ◻ Profit Trends (Month-on-Month) </p> 
Monthly profit levels remain relatively stable, averaging around $1.2 million. January ($1.33M) and October ($1.32M) are top-performing months, mirroring transaction peaks, while June ($1.12M) records the lowest profit.

Recommended Action:
 - Align inventory and marketing strategies with peak months to sustain profitability.
 - Strengthen promotional and sales strategies in months with declining profits to boost revenue consistency and mitigate seasonal dips.

<p> ◻ Year-on-Year Profit Growth </p>
Profits were consistent between 2011–2013, averaging $4.6–4.8 million annually, but dropped sharply to $683K in 2014 — an ~85% decline. This suggests possible operational, pricing, or product-mix changes that severely impacted overall performance.

Recommended Action:
 - Conduct a root cause review of 2014’s decline (e.g., increased returns, reduced prices, or loss of key product lines).
 - Establish annual performance benchmarks and early-warning indicators to prevent similar profit erosion.


<p> ◻ Revenue and Profit by Product Category </p> 
The Books and Electronics categories are the top revenue generators, together accounting for over 40% of total sales, while Footwear delivers the highest profit margin (≈30%), signaling efficient pricing and cost control.

Recommended Action:
 - Sustain strong performers (Books, Electronics) through targeted upselling or bundle offers.
 - Expand Footwear marketing or new product lines given its high margin potential.
 - Reassess Bags and Clothing strategies—lower revenue might be improved through promotions or assortment refreshes.

<p> ◻ Transactions by Gender </p>
 Female customers account for 57% of total transactions (13,148 vs. 9,787), indicating stronger engagement and purchasing behavior among women.

Recommended Action:
 - Tailor marketing campaigns and loyalty programs toward female shoppers to sustain engagement.
 - Identify opportunities to increase male customer participation through personalized product recommendations or male-focused categories.
 - Leverage demographic insights to refine promotional messaging for balanced customer outreach.

<p> ◻ Transactions by Product Category </p>
Customer activity is concentrated in Books (6,039 transactions) and Electronics (4,878). Bags have the lowest transaction volume (1,985), reinforcing earlier profit insights about limited demand.

Recommended Action:
 - Continue optimizing top-selling categories through targeted advertising and inventory prioritization.
 - Revitalize underperforming categories (e.g., Bags and Clothing) with refreshed product designs, limited-time offers, or influencer partnerships.
 - Conduct product demand analysis to align inventory levels with high-interest categories and reduce overstock risk.
