# Shop Database ETL Pipeline

This project is a complete end-to-end ETL (Extract, Transform, Load) pipeline for a retail shop database. It demonstrates how raw business data can be collected from multiple sources, cleaned, standardized, and prepared for analysis or storage in a relational database.

The dataset includes customer, product, order, and payment information, with several realistic data quality issues such as invalid emails, missing values, wrong dates, and inconsistent product fields. The project focuses on handling these issues and transforming the raw files into clean, usable data.

## Project Overview

The goal of this project is to:

- Extract data from CSV and Excel files
- Clean and standardize inconsistent records
- Transform data into a structured format suitable for database use
- Validate key fields like emails, dates, prices, and stock quantities
- Prepare the final data for reporting and analysis

## Business Use Case

This pipeline simulates a small e-commerce or retail environment where a business needs to manage:

- Customer profiles
- Product catalog data
- Order details
- Payment records

By cleaning and organizing this information, the business can improve data consistency, reduce errors, and support downstream reporting and analysis.

## Data Sources

The repository contains the following datasets:

- `users_data.csv` - customer information
- `products_data.csv` - product catalog and inventory details
- `orders_data.csv` - order records and amounts
- `payments_data.xlsx` - payment information in Excel format

## ETL Workflow

The pipeline follows a standard ETL process:

1. Extract
   - Read data from CSV and Excel files
   - Load raw datasets into Python using pandas

2. Transform
   - Clean invalid or missing values
   - Standardize column names and formatting
   - Handle invalid dates and email formats
   - Convert text-based numeric fields into proper data types
   - Fill or remove incomplete records as required

3. Load
   - Prepare cleaned tables for SQL database storage or analysis
   - Structure the output into normalized, query-friendly records

4. Validate
   - Check for quality issues in the transformed data
   - Ensure the final dataset is consistent and ready for business use

## Tech Stack

- Python
- Pandas
- Jupyter Notebook
- Excel file handling (`openpyxl` / Excel input)
- SQL / database concepts

## Project Structure

```text
Shop-Database-ETL-Pipeline/
├── README.md
├── ETL Pipleline project end to end.ipynb
├── users_data.csv
├── products_data.csv
├── orders_data.csv
├── payments_data.xlsx
└── .ipynb_checkpoints/   (if generated locally)
```

## Example Data Quality Issues Handled

This project includes imperfect real-world data, such as:

- Invalid or missing email addresses
- Blank or null values in critical columns
- Incorrect date strings
- Non-numeric values in numeric fields like price or stock quantity
- Missing product descriptions and category values

These issues are common in real business datasets and are part of why ETL projects are important.

## How to Run

1. Open the Jupyter notebook:
   `ETL Pipleline project end to end.ipynb`
2. Install the required packages:

```bash
pip install pandas openpyxl jupyter
```

3. Run the notebook cells in order to:
   - load the data
   - clean the records
   - transform the fields
   - prepare the final dataset

## Use Cases

This project can be extended for:

- Sales reporting
- Customer segmentation
- Inventory analysis
- Revenue tracking
- Database migration workflows
- Data quality monitoring

## Summary

This repository showcases a practical ETL pipeline for a shop database using realistic data challenges. It is useful for learning how raw business data is cleaned, transformed, and organized before being used in reporting or database systems.

## Future Improvements

- Add SQL database creation and table loading scripts
- Automate ETL with a Python script instead of notebook execution
- Add logging and error tracking
- Include dashboards for sales and inventory analysis
- Create reusable transformation functions for larger datasets
