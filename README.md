# 📊 CRM Sales Performance Analysis using SQL Server

## 🔎 Project Summary
Performed end-to-end CRM data analysis using SQL Server to evaluate sales pipeline performance, revenue distribution, and sales effectiveness across agents, products, industries, and regions using advanced SQL queries.

## 📁 Dataset Description

The project uses a relational CRM dataset consisting of four tables:

- **sales_pipeline** (Fact Table – deal-level data)
- **accounts** (Customer information)
- **products** (Product hierarchy and series)
- **sales_teams** (Sales agents, managers, regional offices)

The data models a real-world sales pipeline including deal stages, revenue, customer sectors, and sales hierarchy.

## 🎯 Business Objectives

- Analyze deal distribution across pipeline stages  
- Identify top-performing sales agents  
- Evaluate revenue contribution by product and industry  
- Assess regional sales performance  
- Detect revenue concentration patterns  
- Identify high-value accounts and above-average deal performance  

## 🧠 Analytical Approach

### 1️⃣ Data Exploration
- Reviewed table structures using `sp_help` and `INFORMATION_SCHEMA`
- Validated data types and NULL values
- Verified primary join keys across tables

### 2️⃣ Data Preparation
- Filtered revenue analysis using `deal_stage = 'Won'`
- Handled missing values using `COALESCE()`
- Excluded incomplete records in time-based queries

### 3️⃣ SQL Techniques Applied
- `GROUP BY` aggregations
- `HAVING` clause filtering
- `INNER JOIN` & `LEFT JOIN`
- Subqueries
- Common Table Expressions (CTE)
- Window Functions (`RANK() OVER`)
- Date filtering using `BETWEEN`
- Revenue benchmarking using overall averages

## 🛠 Tools & Technologies

- Microsoft SQL Server
- SQL Server Management Studio (SSMS)
- Relational Data Modeling
- Advanced SQL Querying

## 📊 Key Analytical Areas

### 🔹 Sales Pipeline Analysis
- Deal count by stage
- Deal value distribution
- Pipeline bottleneck identification

### 🔹 Sales Agent Performance
- Deal volume per agent
- Revenue ranking (Top 10 using Window Functions)
- Above-average deal performers

### 🔹 Revenue & Product Analysis
- Revenue by product series
- Product performance benchmarking
- Industry × Product revenue matrix

### 🔹 Regional & Industry Insights
- Revenue by regional office
- Deals won by office location (time-bound analysis)
- Sector-based revenue distribution

### 🔹 Key Account Analysis
- Top 3 accounts by total revenue
- Sector and managerial alignment of high-value accounts

## 📈 Core Business Insights

- Revenue is concentrated among a limited number of high-performing sales agents.
- Product performance varies significantly across industries.
- Regional revenue contribution is largely balanced, with slight performance variation.
- Short-term deal wins show geographic concentration.
- High-value accounts span multiple sectors, indicating diversified revenue sources.

## ⚠ Assumptions

- Only `Won` deals represent realized revenue.
- NULL revenue values do not inflate financial calculations.
- All monetary values are comparable (single currency).
- Each row in `sales_pipeline` represents one unique deal.

## 🏁 Results & Conclusion

This SQL-based CRM analysis provides actionable insights into sales efficiency, revenue drivers, and performance concentration. The findings highlight opportunities to optimize sales resource allocation, strengthen underperforming regions, scale high-performing strategies, and improve revenue stability through diversified industry focus.

## 📄 Full Report

[View Full CRM Analysis Report](./Customer_Relationship_Management_Analysis_SQL.pdf)

## 📌 Repository Structure

```plaintext
customer-relationship-management-analysis-sql/
│
├── README.md
├── Customer_Relationship_Management_Analysis_SQL.pdf
├── data/
│   ├── sales_pipeline.csv
│   ├── accounts.csv
│   ├── products.csv
│   └── sales_teams.csv
