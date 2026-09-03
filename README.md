# 🗃️ Sales Insights: Customers & Products Analysis

## 📖 Overview

This project focuses on:

1. **Data Architecture**: Building a scalable and organized data warehouse using the **Medallion Architecture**.

2. **ETL Pipelines**:  Extracting, transforming, and loading data from source systems into the warehouse.

3. **Data Modeling**: Building fact and dimension tables structured optimized for analytical queries.

4. **Analytics & Reporting**: Creating SQL-based reports and dashboards to deliver actionable insights. 

## 🧱 Data Architecture
The data architecture is designed around the Medallion Architecture framework, organized into Bronze, Silver, and Gold layers.

![Data Architecture](docs/Data_Architecture.png)

1. **Bronze Layer**: Stores raw, unprocessed data directly ingested from source systems. Data is loaded from CSV files into a SQL Server database. [more details](scripts/bronze/BRONZE.md)

2. **Silver Layer**: Applies data cleaning, standardization, and normalization to ensure data quality and consistency, making it suitable for analysis. [more details](scripts/silver/SILVER.md)

3. **Gold Layer**: Stores curated, business-ready datasets organized into star schema models, optimized for reporting and analytical queries. [more details](scripts/gold/GOLD.md)

## 📂 Datasets
🔹CRM: Customer Relationship Management
- **cust_info.csv**: customer informations
- **prd_info.csv**: product informations
- **sales_details.csv**: transactional Records about Sales & Orders

🔹ERP: Enterprise Resource Planning
- **CUST_AZ12.csv**: extra customer informations → birth date 
- **LOC_A101.csv**: extra customer informations → country
- **PX_CAT_G1V2.csv**: extra procuct informations → category, subcategory, maintenance

## 📊 Analytics & Reporting

### Analysis using SQL ([click here to view code](scripts/_data_analysis))
The **Gold Layer** served as the foundation for analysis, enabling: ([gold layer info](docs/Gold_Info.md))
1. Exploration of customer behavior  
2. Evaluation of product performance  
3. Identification of sales trends over time  
4.  Segmentation and market share insights  
5.  Development of business-oriented reports  
    

### Data Visualization using Power BI dashboard

![Data Visualization using Power BI dashboard](docs/Sales_Dashboard.png)



## Findings

Revenue reached **$29.35M across the three full years (2011–2013)**, with performance showing significant volatility. After declining from **$7.08M in 2011 to $5.84M in 2012**, revenue surged to **$16.34M in 2013**, a **180% increase**.

The business remains highly concentrated, with **Bikes contributing 96.5% of total revenue**, creating reliance on a single category.

The strongest opportunity for sustainable growth lies in the customer base: **VIP customers represent just 8.9% of customers but generate 36.7% of revenue**, spending approximately **9x more than New customers**.

**Strategic priority:** Strengthen VIP retention and increase customer lifetime value to build a more resilient growth engine, while reducing dependence on continued bike-category momentum.


