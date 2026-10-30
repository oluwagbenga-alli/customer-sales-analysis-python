# Project 2: Customer Sales Analysis with Python

## 1. Project Overview

This beginner project uses Python to analyse online retail transactions. It explores total sales, monthly sales trends, top-selling products, and sales by country.

## 2. Business Question

**What can sales transaction data tell us about revenue, popular products, and sales performance?**

The analysis focuses on:

- What were the total sales?
- How did sales change by month?
- Which five products generated the most sales?
- Which countries contributed the most sales?

## 3. Dataset

- **Dataset:** Online Retail Dataset
- **Source:** UCI Machine Learning Repository
- **Dataset link:** [UCI Online Retail Dataset](https://archive.ics.uci.edu/dataset/352/online+retail)
- **File used:** `Online Retail.xlsx`

The dataset contains transactions from a UK-based online retailer between December 2010 and December 2011. Each row represents a product line within an invoice.

## 4. Tools and Technologies

- **Python** for the analysis
- **Pandas** for loading, cleaning, and summarising data
- **Matplotlib** for charts
- **Jupyter Notebook** for writing and running the code

## 5. Methodology

The project was completed in four stages.

### Stage 1: Load and Understand the Data

**Objective:** Review the dataset’s structure and check its quality.

**Activities:**

- Loaded the Excel file with Pandas `read_excel()`.
- Previewed records with `head()`.
- Checked the number of rows and columns with `shape`.
- Reviewed column names and data types with `info()`.
- Summarised numeric columns with `describe()`.
- Checked missing values with `isna().sum()`.
- Checked for exact duplicate records.

**Initial dataset size:** 541,909 rows and 8 columns.

### Stage 2: Basic Data Cleaning

**Objective:** Prepare the transactions for a basic sales analysis.

**Activities:**

- Removed exact duplicate records using `drop_duplicates()`.
- Removed cancellation transactions, identified by invoice numbers beginning with `C`.
- Removed rows with zero or negative quantities.
- Removed rows with zero or negative unit prices.
- Checked missing values after cleaning.

**Rows remaining after cleaning:** 524,878.

There were 132,186 missing `CustomerID` values after cleaning. They were left in the dataset because the project analyses sales by product, month, and country rather than individual customers.

### Stage 3: Basic Sales Analysis

**Objective:** Summarise sales performance using the cleaned data.

**Activities:**

- Calculated sales for each transaction line by multiplying quantity by unit price.
- Added transaction line sales to find total sales.
- Grouped sales by month.
- Grouped sales by product and sorted the results to identify the top five.
- Grouped sales by country and sorted the results.

### Stage 4: Visualisation and Findings

**Objective:** Present the results clearly and summarise what they show.

**Activities:**

- Created a bar chart of sales by month.
- Created a bar chart of the top five products by sales.
- Used the summary tables and charts to write business findings.

## 6. Analysis Results

- **Total sales:** approximately **£10,642,110.80**.
- **Highest sales month:** November 2011, with approximately **£1,503,866.78**.
- **Top product by sales:** DOTCOM POSTAGE, with **£206,248.77**.
- **Highest sales country:** United Kingdom, with approximately **£9,001,744.09**.

## 7. Key Findings

1. Total sales across the cleaned transactions were approximately **£10.64 million**.
2. Monthly sales were highest in **November 2011**. Sales rose from September through November, then fell in December.
3. The **United Kingdom** contributed the most sales. Among products, **DOTCOM POSTAGE** ranked first by sales.

## 8. Business Recommendations

- Monitor stock availability for products that generate the most sales.
- Use the monthly sales pattern to inform inventory and promotion planning, especially ahead of high-sales months.
- Review sales by country when considering where to focus marketing or business development.

## 9. Project Status

The four project stages are complete: data exploration, basic cleaning, sales analysis, and visualisation with findings.
