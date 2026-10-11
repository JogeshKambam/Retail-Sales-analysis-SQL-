# 🛍️ Retail Sales Analysis Using SQL

## 📌 Project Overview

This project focuses on analyzing retail sales transaction data using SQL and MySQL Workbench. The objective is to explore sales performance, understand customer purchasing behavior, identify product category trends, and answer business-related questions using SQL queries.

The project demonstrates practical SQL skills used in data analysis, including data exploration, data quality checks, aggregation, filtering, grouping, and business insight generation.

## 🎯 Project Objectives

* Analyze overall retail sales performance.
* Understand customer purchasing behavior.
* Identify popular product categories.
* Analyze sales quantities and transaction values.
* Explore customer demographics, including age and gender.
* Examine sales trends based on transaction dates and times.
* Classify transactions into different shifts.
* Answer business questions using SQL queries.

## 🛠️ Tools and Technologies

* **Database:** MySQL
* **SQL Environment:** MySQL Workbench
* **Language:** SQL
* **Dataset:** Retail sales transaction data
* **Version Control:** Git and GitHub (for project sharing)

## 📂 Dataset Description

The dataset contains retail transaction records with information about sales, customers, product categories, and transaction dates and times.

### Key Columns

| Column           | Description                            |
| ---------------- | -------------------------------------- |
| `transaction_id` | Unique identifier for each transaction |
| `sale_date`      | Date of the transaction                |
| `sale_time`      | Time of the transaction                |
| `customer_id`    | Identifier of the customer             |
| `gender`         | Gender recorded for the customer       |
| `age`            | Customer's age                         |
| `category`       | Product category                       |
| `quantity`       | Number of units purchased              |
| `price_per_unit` | Price per unit                         |
| `cogs`           | Cost of goods sold                     |
| `total_sale`     | Total sales value of the transaction   |

## 🔍 Project Workflow

### 1. Database Setup

* Created a database in MySQL.
* Created the retail sales table.
* Imported the dataset into MySQL Workbench.

### 2. Data Exploration

* Retrieved sample records.
* Checked the total number of transactions.
* Examined distinct product categories.
* Reviewed the table structure and column data types.

### 3. Data Quality Checks

* Checked for NULL values.
* Examined date and time columns.
* Verified quantity and sales values.
* Investigated data quality issues where necessary.

### 4. SQL Analysis

Used SQL queries to answer business questions through:

* `SELECT` and `WHERE`
* Aggregate functions such as `COUNT()`, `SUM()`, `AVG()`, `MIN()`, and `MAX()`
* `GROUP BY` and `HAVING`
* `CASE` statements
* Date and time functions
* Subqueries and Common Table Expressions (CTEs)

### 5. Business Insights

Analyzed sales transactions to understand customer behavior, product category performance, and transaction patterns across different time periods.

## 💼 Business Questions Answered

The project explores questions such as:

1. What is the total number of transactions?
2. Which Clothing transactions occurred in November 2022 with a quantity greater than four?
3. What are the total sales and transaction counts for different product categories?
4. What is the average age of customers purchasing from specific categories?
5. How do sales vary by customer gender?
6. Which transactions have high sales values?
7. How does sales performance vary across different months?
8. Which customers or transactions contribute to sales performance?
9. What are the key characteristics of retail transactions?
10. How many transactions occurred during the Morning, Afternoon, and Evening shifts?

*Note: The final business questions should match the actual SQL scripts included in the repository.*

## 🧠 SQL Concepts Demonstrated

| SQL Concept            | Application                                            |
| ---------------------- | ------------------------------------------------------ |
| Filtering with `WHERE` | Retrieving transactions that match specific conditions |
| Aggregate functions    | Calculating sales totals, averages, and counts         |
| `GROUP BY`             | Summarizing sales by category or shift                 |
| `HAVING`               | Filtering aggregated results                           |
| `CASE` statements      | Classifying transactions into shifts                   |
| Date functions         | Filtering transactions by month                        |
| Subqueries             | Performing analysis using intermediate results         |
| CTEs                   | Organizing complex queries into readable steps         |
| NULL checks            | Identifying missing values                             |

## 📊 Example SQL Query: Sales by Category

```sql
SELECT
    category,
    SUM(total_sale) AS total_sales,
    COUNT(*) AS total_transactions
FROM retail_sales
GROUP BY category
ORDER BY total_sales DESC;
```

This query calculates total sales and transaction counts for each product category.

## ⏰ Example SQL Query: Transactions by Shift

```sql
SELECT
    CASE
        WHEN HOUR(sale_time) < 12 THEN 'Morning'
        WHEN HOUR(sale_time) BETWEEN 12 AND 17 THEN 'Afternoon'
        ELSE 'Evening'
    END AS shift,
    COUNT(*) AS total_orders
FROM retail_sales
GROUP BY shift;
```

This query classifies transactions into Morning, Afternoon, and Evening shifts and counts the transactions in each group.

## 📈 Expected Outcomes

The analysis helps demonstrate how SQL can be used to:

* Summarize retail sales data.
* Identify differences in sales across product categories.
* Examine customer purchasing patterns.
* Analyze transactions by date and time.
* Check data quality before analysis.
* Convert raw transaction records into useful business information.

Actual findings and numerical results should be added after running and validating the queries.



*Keep the dataset and SQL file in the repository only if you have permission to share them.*

## 🚀 How to Run the Project

1. Install MySQL Server and MySQL Workbench.
2. Download or obtain the retail sales dataset.
3. Create a database in MySQL.
4. Create the retail sales table using the appropriate column definitions.
5. Import the dataset into the table.
6. Open the SQL script in MySQL Workbench.
7. Execute the queries one by one.
8. Review the results and document the business insights.

## 👨‍💻 Skills Demonstrated

* SQL querying and data manipulation
* Data exploration and quality checks
* Sales analysis
* Customer behavior analysis
* Date and time-based analysis
* Aggregation and grouping
* Business problem-solving
* Translating business questions into SQL queries

## 🏁 Conclusion

This project demonstrates the use of SQL to explore and analyze retail transaction data. It provides practical experience in data quality checks, aggregation, filtering, and business-oriented analysis.

The project also builds a foundation for more advanced analytics using Python, visualization tools, and business intelligence platforms.

---

**Project:** Retail Sales Analysis Using SQL
**Database:** MySQL
**Tool:** MySQL Workbench
**Author:** Jogesh
