# Business Requirements Document
## Retail Sales Analytics Dashboard

### 1. Project Overview

The Retail Sales Analytics Dashboard is a Power BI reporting solution designed to analyse retail sales performance, product performance, profitability and sales trends.

The project uses a practice retail sales dataset containing transaction-level sales information and product master data.

The objective is to transform raw sales data into meaningful business insights through interactive Power BI visualisations.

### 2. Business Problem

Retail businesses need to monitor sales performance, understand customer purchasing patterns and identify profitable products.

Analysing sales data manually can make it difficult to:
- Monitor overall sales and profit.
- Identify top-performing products and categories.
- Compare monthly and daily sales trends.
- Understand payment mode distribution.
- Evaluate performance across different sales types.

This dashboard addresses these requirements through a centralised reporting solution.

### 3. Business Objectives

1. Monitor total sales and overall profitability.
2. Analyse sales and profit trends over time.
3. Identify high-performing products.
4. Compare sales across product categories.
5. Analyse sales by payment mode.
6. Compare performance across sales types.
7. Provide interactive filtering for business analysis.

### 4. Key Performance Indicators (KPIs)

| KPI | Business Definition |
|---|---|
| Total Sales | Net sales value after applicable discounts |
| Total Quantity | Total units sold |
| Total Cost | Total purchase cost of sold products |
| Total Profit | Net sales minus total cost |
| Profit Margin % | Total profit divided by net sales |

*Final KPI calculations must be validated against the Power BI measures before publication.*

### 5. Dashboard Requirements

The dashboard should provide the following analytical views:

| Visual | Business Requirement |
|---|---|
| KPI Cards | Display key sales and profitability indicators |
| Monthly Sales & Profit | Analyse monthly performance trends |
| Sales by Payment Mode | Compare payment method contribution |
| Sales by Product | Identify product-level performance |
| Daily Sales | Understand daily sales patterns |
| Sales by Type | Compare different sales channels/types |
| Sales by Category | Analyse category-level performance |

### 6. Interactive Filters

The report includes the following filters:

- Year
- Month Name
- Sale Type
- Payment Mode

Users should be able to apply filters and analyse the relevant business performance dynamically.

### 7. Data Sources

The project uses two Excel worksheets:

- **Input Data:** Transaction-level sales information.
- **Master Data:** Product-level information, including category and pricing attributes.

The data is used to build the Power BI data model and calculate business KPIs.

### 8. Expected Business Benefits

- Improved visibility into sales performance.
- Better understanding of product and category performance.
- Easier identification of sales trends.
- Improved profitability monitoring.
- Faster and more informed business decisions.

### 9. Tools and Technologies

- Microsoft Power BI Desktop
- Power Query
- DAX
- Microsoft Excel
- Data Modelling
- GitHub for project documentation and version control

### 10. Project Scope

This is a practice portfolio project developed to demonstrate Power BI development, data modelling, DAX calculations, dashboard design and business analysis skills.

The dataset does not represent verified live business performance.
