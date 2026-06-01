# Store Sales Analysis

## Project Overview
**Project Title**: Retail Sales Analysis
**Level**: Beginner
**Database**: p1_retail_db

## Objectives
1. Built and Managed Retail Sales Database
2. Cleaned and Transformed Raw Data
3. Conducted Exploratory Data Analysis
4. Generated Business Insights and Recommendations

This project showcases SQL techniques for data cleaning, exploratory analysis, and business reporting using store sales data. It 
demonstrates how SQL can be used to transform raw data into actionable business insights.

## Project Workflow
### 1. Database Setup

```
CREATE DATABASE st_project_tb;

CREATE TABLE retail_st (
    transactions_id INT PRIMARY KEY,
    sale_date DATE,
    sale_time TIME,
    customer_id INT,
    gender VARCHAR(15),
    age INT,
    category VARCHAR(15),
    quantity INT,
    price_per_unit FLOAT,
    cogs FLOAT,
    total_sale FLOAT
);

SELECT * FROM retail_st;
```

### 2. Data Cleaning and Preparation

```
SELECT COUNT(*) FROM retail_st;
SELECT COUNT(*) as total_sale FROM retail_st; 
SELECT COUNT(DISTINCT customer_id) as total_sale FROM retail_st;
SELECT COUNT(DISTINCT category) as total_sale FROM retail_st;

-- Data Cleaning
SELECT * FROM retail_st
WHERE
    transactions_id IS NULL
    OR
    sale_date IS NULL
    OR
    sale_time IS NULL
    OR
    customer_id IS NULL
    OR
    gender IS NULL
    OR
    age IS NULL
    OR
    category IS NULL
    OR
    quantity IS NULL
    OR
    price_per_unit IS NULL
    OR
    cogs IS NULL
    OR
    total_sale IS NULL


DELETE FROM retail_st
WHERE
    transactions_id IS NULL
    OR
    sale_date IS NULL
    OR
    sale_time IS NULL
    OR
    customer_id IS NULL
    OR
    gender IS NULL
    OR
    age IS NULL
    OR
    category IS NULL
    OR
    quantity IS NULL
    OR
    price_per_unit IS NULL
    OR
    cogs IS NULL
    OR
    total_sale IS NULL
```

### 3. Data Analysis & Findings
The following SQL queries address key business problems and generate actionable insights for decision-making.
