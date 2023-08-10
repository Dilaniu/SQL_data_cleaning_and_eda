# SQL_data_cleaning_and_eda
Certainly! Here's a README template for the SQL queries:

---

# Project SQL Analysis

This repository contains a collection of SQL queries that provide insights and aggregations on the `calls` dataset for our project. It involves creating, updating, and querying the data for various analytical insights.

## Table Structure

Initially, a database `project` and table `calls` is created with the following structure:

```sql
CREATE TABLE calls (
	ID CHAR(50),
	cust_name CHAR (50),
	sentiment CHAR (20),
	csat_score CHAR(5),
	call_timestamp CHAR (10),
	reason CHAR (20),
	city CHAR (20),
	state CHAR (20),
	channel CHAR (20),
	response_time CHAR (20),
	call_duration_minutes INT,
	call_center CHAR (20)
);
```

## Data Cleanup

Before diving deep into analysis, the data needs some cleaning and transformation:

- Convert `call_timestamp` from string to date format.
- Setting `csat_score` values to NULL where they are 0.
- Alter the data type of `csat_score` to INT.

## Exploratory Data Analysis (EDA)

After cleaning, the EDA begins with:

1. Checking the number of rows and columns.
2. Reviewing distinct values in key columns.
3. Computing percentages for distinct values.
4. Grouping data by days of the week.
5. Various aggregation methods to get insights.

## Advanced Aggregations

Advanced querying techniques like window functions are used to uncover deeper insights:

- Identifying maximum call duration partitioned by `call_timestamp`.

## Usage

You can run these queries on your MySQL server instance after setting up the appropriate data.

## Contribution

Feel free to raise issues or PRs if you find something amiss or wish to contribute new queries or improvements to existing ones!
---
