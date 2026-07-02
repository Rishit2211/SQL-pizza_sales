# SQL Pizza Sales Analysis

## Overview

This project focuses on analyzing pizza sales data using SQL to identify sales trends, customer preferences, product performance, and revenue generation. The project demonstrates practical SQL skills for business intelligence and data analytics.

## Objectives

* Analyze overall sales performance
* Identify best-selling pizzas
* Evaluate revenue by pizza category and size
* Discover customer ordering trends
* Generate business insights for decision-making

## Dataset

The dataset includes:

* Orders
* Order Details
* Pizzas
* Pizza Types
* Categories
* Sizes
* Prices
* Order Dates and Times

## Technologies Used

* SQL
* MySQL / PostgreSQL
* Joins
* Aggregate Functions
* Common Table Expressions (CTEs)
* Window Functions

## Key Analysis Performed

### Revenue Analysis

* Total Revenue Generated
* Average Order Value
* Revenue by Pizza Category
* Revenue by Pizza Size

### Product Analysis

* Top-Selling Pizzas
* Least-Selling Pizzas
* Category-Wise Sales Performance

### Order Analysis

* Total Number of Orders
* Peak Ordering Hours
* Daily and Monthly Order Trends

### Customer Insights

* Popular Pizza Preferences
* High-Demand Categories
* Sales Distribution Patterns

## Sample SQL Queries

### Total Revenue

```sql
SELECT ROUND(SUM(quantity * price), 2) AS total_revenue
FROM order_details od
JOIN pizzas p
ON od.pizza_id = p.pizza_id;
```

### Top 5 Best-Selling Pizzas

```sql
SELECT pizza_name,
       SUM(quantity) AS total_sold
FROM pizza_sales
GROUP BY pizza_name
ORDER BY total_sold DESC
LIMIT 5;
```

### Revenue by Category

```sql
SELECT category,
       ROUND(SUM(quantity * price), 2) AS revenue
FROM pizza_sales
GROUP BY category
ORDER BY revenue DESC;
```

## Insights

* Identified the most popular pizza varieties
* Determined peak sales periods
* Evaluated revenue contribution by category and size
* Generated recommendations to improve sales performance

## Project Structure

```text
SQL-Pizza-Sales-Analysis/
│
├── dataset/
│   └── pizza_sales.csv
│
├── sql_queries/
│   └── pizza_sales_analysis.sql
│
├── screenshots/
│
└── README.md
```

## Learning Outcomes

* SQL for Data Analytics
* Business Performance Analysis
* Revenue Trend Analysis
* Data-Driven Decision Making
* Advanced Query Writing

## License

This project is intended for educational and portfolio use.
