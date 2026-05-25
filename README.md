# Retail Brand Performance Analytics Dashboard using Azure SQL & Power BI

## Overview
This project is an end-to-end Retail Brand Performance Analytics Dashboard developed using Azure SQL Database and Power BI. The project focuses on analyzing retail brand performance, discounts, profitability, and sales trends using cloud-based analytics and interactive dashboards.

The project demonstrates practical implementation of:
- Azure SQL Database
- SQL Data Cleaning
- Power BI Dashboard Development
- DAX Calculations
- Cloud Data Integration
- Business Analytics

---

# Tools & Technologies Used
- Microsoft Azure
- Azure SQL Database
- SQL
- Power BI
- DAX
- Power BI Service

---

# Project Workflow

## 1. Azure SQL Database Setup
- Created Azure SQL Database
- Uploaded retail dataset into Azure SQL
- Managed cloud-based data storage

## 2. SQL Data Cleaning
Performed data cleaning in Azure SQL Database using SQL queries:
- Removed unwanted symbols from price columns
- Standardized data formats
- Improved data consistency

## 3. Power BI Integration
Connected Power BI with Azure SQL Database using:
- Database authentication
- Microsoft account authentication

## 4. Data Transformation
Performed additional data transformation and formatting in Power BI Power Query.

## 5. DAX Calculations
Created calculated columns and measures including:
- Discount %
- Profit %
- Cost Price

## 6. Dashboard Development
Built interactive dashboards to analyze:
- Brand performance
- Discount trends
- Profitability
- Product variety
- Sales price comparison

## 7. Power BI Service Publishing
Published reports to Power BI Service for cloud-based sharing and accessibility.

---

# SQL Queries Used

## Cleaning Original Price Column
```sql
SELECT TOP (1000) *
FROM [dbo].[Men+Tshirt (1)]

UPDATE [dbo].[Men+Tshirt (1)]
SET original_price =
TRIM(REPLACE(CAST(original_price AS VARCHAR(MAX)), '?', ''))
WHERE original_price LIKE '%?%'
