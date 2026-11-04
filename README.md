# Sql_project_retail-sales-dataset
# 🛍️ SQL Retail Sales Analysis Project

## 📌 Project Overview

This project focuses on analyzing retail sales data using **SQL (PostgreSQL)** to uncover meaningful business insights and understand customer purchasing behavior.

The project involves database creation, data cleaning, exploratory data analysis (EDA), and solving real-world business questions using SQL queries.

The main goal is to analyze sales performance, customer demographics, product categories, monthly sales trends, and customer purchasing patterns to support data-driven business decisions.

## 🎯 Project Objectives

- Create and manage a retail sales database.
- Clean the dataset by identifying and removing missing values.
- Perform Exploratory Data Analysis (EDA).
- Analyze sales performance across different product categories.
- Understand customer demographics and purchasing behavior.
- Identify the best-selling month in each year.
- Find top customers based on total sales.
- Analyze sales patterns across different time shifts.

## 🛠️ Tools & Technologies

- **Database:** PostgreSQL
- **Language:** SQL
- **Concepts:** Data Cleaning, EDA, Aggregate Functions, Window Functions, CTEs, CASE Statements, GROUP BY, ORDER BY, Filtering.

## 📂 Project Structure

```text
SQL_Retail_Sales_Analysis/
│
├── README.md
├── sql_query_project.sql
└── SQL - Retail Sales Analysis_utf.csv
```

## 🗄️ Database Schema

Database Name: `sql_project1`

Table Name: `retail_sales`

| Column Name | Data Type | Description |
|---|---|---|
| transactions_id | INT | Unique transaction ID |
| sale_date | DATE | Date of sale |
| sale_time | TIME | Time of sale |
| customer_id | INT | Customer ID |
| gender | VARCHAR(20) | Customer gender |
| age | INT | Customer age |
| category | VARCHAR(20) | Product category |
| quantiy | INT | Quantity purchased |
| price_per_unit | FLOAT | Price per unit |
| cogs | FLOAT | Cost of goods sold |
| total_sale | FLOAT | Total transaction amount |

## 🧹 Data Cleaning

The following data cleaning operations were performed:

- Checked the dataset for missing (NULL) values.
- Identified NULL values across important columns.
- Removed records containing missing values.
- Verified the dataset after cleaning.

## 📊 Exploratory Data Analysis (EDA)

Performed initial analysis to understand the dataset:

- Retrieved sample records.
- Counted total sales transactions.
- Identified unique customers.
- Identified unique product categories.
- Explored the available customer and sales information.

## 🔍 Business Questions & SQL Analysis

The project addresses the following 10 business questions:

**Q1. Retrieve all columns for sales made on November 5, 2022.**

- Used `WHERE` to filter transactions by a specific date.

**Q2. Retrieve all transactions where the category is Clothing and the quantity sold is more than 4 in November 2022.**

- Used `WHERE`, `AND`, and date formatting with `TO_CHAR()`.

**Q3. Calculate the total sales for each product category.**

- Used `SUM()`, `COUNT()`, and `GROUP BY`.

**Q4. Find the average age of customers who purchased items from the Beauty category.**

- Used `AVG()` and `ROUND()`.

**Q5. Find all transactions where the total sale is greater than 1000.**

- Used conditional filtering with `WHERE`.

**Q6. Find the total number of transactions made by each gender in each product category.**

- Used `COUNT()`, `GROUP BY`, and `ORDER BY`.

**Q7. Calculate the average sale for each month and identify the best-selling month in each year.**

- Used `EXTRACT()`, `AVG()`, `RANK()`, `OVER()`, and `PARTITION BY`.
- Applied Window Functions to rank monthly sales separately for each year.

**Q8. Find the top 5 customers based on the highest total sales.**

- Used `SUM()`, `GROUP BY`, `ORDER BY DESC`, and `LIMIT`.

**Q9. Find the number of unique customers who purchased items from each category.**

- Used `COUNT(DISTINCT customer_id)` and `GROUP BY`.

**Q10. Categorize sales into different shifts and calculate the number of orders in each shift.**

- Used a Common Table Expression (CTE), `WITH`, `CASE WHEN`, `EXTRACT()`, and `COUNT()`.

## 📚 SQL Concepts Practiced

Through this project, I practiced the following SQL concepts:

- Database and Table Creation
- SELECT and WHERE Statements
- AND / OR Operators
- NULL Value Handling
- DELETE Statement
- DISTINCT
- Aggregate Functions (SUM, AVG, COUNT)
- GROUP BY and ORDER BY
- LIMIT
- Date and Time Functions
- EXTRACT() and TO_CHAR()
- Window Functions (RANK, OVER, PARTITION BY)
- Common Table Expressions (CTE)
- CASE WHEN Statements

## 💡 Key Learning Outcomes

- Gained practical experience in SQL-based data analysis.
- Improved understanding of data cleaning techniques.
- Learned how to solve business-related problems using SQL.
- Practiced aggregate and window functions for sales analysis.
- Developed an understanding of customer purchasing behavior and sales trends.

## 🚀 How to Run This Project

1. Clone the repository:

```bash
git clone YOUR_REPOSITORY_URL
```

2. Open PostgreSQL using pgAdmin or your preferred SQL editor.

3. Create the database:

```sql
CREATE DATABASE sql_project1;
```

4. Import the provided CSV dataset into the `retail_sales` table using the appropriate column mapping.

5. Open `sql_query_project.sql`.

6. Execute the SQL queries to perform data cleaning, exploratory analysis, and business analysis.

## 👩‍💻 Author

**Afsana Sadia Borni**

Computer Science & Engineering Student

Interested in Data Analytics, Machine Learning, and Database Management.

---

⭐ If you find this project useful, feel free to explore the SQL queries and share your feedback!
