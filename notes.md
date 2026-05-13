# Project notes

This file contains notes, assumptions and learning progress related to the project.

## Initial data inspection

Dataset: Online Retail — UCI Machine Learning Repository

Initial columns:

- InvoiceNo
- StockCode
- Description
- Quantity
- InvoiceDate
- UnitPrice
- CustomerID
- Country

Initial observations:

- The dataset contains transactional sales data.
- Each row represents one product line within an invoice.
- Revenue is not provided directly and needs to be calculated.
- Some rows may contain cancelled orders, missing CustomerID values or negative quantities.

## Initial data quality checks

The initial inspection focuses on identifying potential data quality issues before building the dashboard.

Checked metrics:

- total number of rows
- missing CustomerID values
- missing product descriptions
- cancelled invoices
- negative quantities
- zero or negative unit prices
- number of countries

These checks will help define the data cleaning rules for the analysis.

## Initial inspection results

The dataset contains 541,909 transaction rows.

Initial data quality findings:

- 135,080 rows have missing CustomerID values.
- 1,454 rows have missing product descriptions.
- 9,288 rows are cancelled invoices.
- 10,624 rows have negative quantity values.
- 2,517 rows have zero or negative unit prices.
- The dataset contains transactions from 38 countries.

These findings indicate that the dataset requires cleaning before building the final dashboard.

## Data cleaning rules

For the main sales analysis, only valid sales rows will be used.

A row is considered valid for sales analysis if:

- the invoice is not cancelled,
- quantity is greater than 0,
- unit price is greater than 0,
- product description is not missing.

CustomerID is not required for the main sales analysis because sales, products, countries and monthly revenue can still be analyzed without customer-level identification.

For customer analysis, only rows with available CustomerID will be used.

## Clean dataset summary

- Valid sales rows: 530,104
- Rows available for customer analysis: 397,884
- Total revenue from valid sales rows: 10,666,684.54
