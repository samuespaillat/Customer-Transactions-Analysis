# Customer-Transactions-Analysis
SQL data cleaning and business analysis with MySQL and Power BI, exploring customer transactions, spending patterns, and data quality.

# Customer & Transactions Analysis

## Project Overview

This project analyzes a fictional banking transaction dataset using **MySQL and Power BI**. The goal was to clean inconsistent data, investigate customer transactions, identify spending patterns, and present findings through an interactive dashboard.

The project simulates a practical data analyst workflow, from raw data preparation to business analysis and visualization.

## Tools Used

- **MySQL 8.0 / MySQL Workbench** - data cleaning, transformation, joins, and SQL analysis
- **Power BI** - data modeling, DAX measures, KPI cards, and interactive visualizations
- **CSV** - source data format

## Dataset

The project uses two fictional datasets:

- `customers_messy.csv` - customer information, including customer IDs, names, and states.
- `transactions_messy.csv` - transaction records, including transaction IDs, customer IDs, dates, categories, amounts, payment methods, and transaction statuses.

The original datasets contained duplicate records, missing values, inconsistent date formatting, and transactions that could not be matched to customer records.

## Data Cleaning & Preparation

SQL was used to prepare the datasets for analysis.

### Customers
- Removed 6 duplicate records.
- Reduced the dataset from 146 to 140 customer records.
- Prepared the customer data for joining with transaction records.

### Transactions
- Removed 20 duplicate records.
- Reduced the dataset from 820 to 800 transaction records.
- Standardized transaction dates.
- Identified missing payment-method values.
- Investigated customer IDs that could not be matched to the customer table.

### Data Quality Findings
- 38 transactions had missing payment methods.
- 17 transactions could not be matched to a customer record.
- The unmatched transactions were retained for further investigation rather than automatically assigned to customers.

## Analysis

SQL queries and Power BI visuals were used to explore:

- Transaction value by category.
- Transaction value by state.
- Highest-value customers.
- Transaction counts and total amounts over time.
- Monthly spending patterns.
- Customer and transaction data quality.

A Power BI measure was created to calculate transaction value excluding the category labeled `Payment`.

## Key Business Insights

- **Category spending:** Transportation had the highest total transaction amount among categories, excluding Payment.
- **Geographic differences:** Ohio had the highest transaction value at approximately $23,785.82, while New York had the lowest at $14,745.44.
- **Top customer:** Luis Patel recorded $1,614.53 across 12 transactions.
- **Monthly trends:** March 2025 had the highest monthly transaction count, with 59 transactions, and a transaction value of $10,049.51, excluding Payment.
- **Spending patterns:** In March 2025, groceries accounted for $3,172.42, transportation for $2,292.61, and dining for $2,186.19. Shopping had the lowest amount among these categories at $203.52.
- **Data quality:** 17 transactions could not be matched to customer records and require further investigation.

The analysis suggests a potential seasonal spending pattern worth testing through year-over-year comparisons.

## Dashboard

The Power BI dashboard summarizes transaction activity, category spending, geographic differences, monthly trends, and customer-level results.

A screenshot of the dashboard is included in the repository.

## Limitations & Next Steps

- Investigate unmatched customer IDs to determine why 17 transactions could not be linked to customer records.
- Compare monthly transaction counts and amounts across years to test for seasonality.
- Investigate whether monthly changes are driven by transaction volume, average transaction size, or particular categories.
- Clarify how transaction statuses, refunds, and negative amounts should be treated for different business metrics.

## Skills Demonstrated

- SQL data cleaning and transformation
- Duplicate detection and removal
- Data validation and quality investigation
- Joins and aggregations
- Business question development
- Time-based analysis
- Power BI dashboard development
- DAX measures
- Communicating findings through business insights

## Data Disclaimer

All data used in this project is fictional and intended for educational and portfolio purposes only.
