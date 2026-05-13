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
