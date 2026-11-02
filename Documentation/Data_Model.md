# Data Model Documentation
## Retail Sales Analytics Dashboard

### 1. Overview

The Retail Sales Analytics Dashboard uses a relational data model built with two Excel tables.

The model connects transaction-level sales data with product master information to support sales, cost and profitability analysis.

### 2. Data Sources

| Table | Description | Data Granularity |
|---|---|---|
| InputData | Contains individual sales transactions | One row per transaction |
| MasterData | Contains product details and pricing | One row per product |

### 3. Table Structure

#### InputData — Transaction Table

This table contains sales transaction information.

Fields identified in the source workbook include:

- DATE
- Day
- DISCOUNT %
- Quantity and other transaction attributes

The table is used to analyse sales performance over time and across sales dimensions.

#### MasterData — Product Master Table

This table contains product-level information.

Fields identified in the source workbook include:

- PRODUCT ID
- PRODUCT
- CATEGORY
- BUYING PRIZE
- SELLING PRICE
- UOM

It provides product attributes and pricing information for sales and cost calculations.

### 4. Relationship Design

The current Power BI model contains a one-to-many relationship:

**MasterData (1) → InputData (*)**

- MasterData represents the product lookup side.
- InputData represents the transaction side.
- PRODUCT ID is the expected relationship key; confirm the exact configured columns in Power BI Desktop.
- Product information can be used to analyse transaction-level sales.

### 5. Data Model Diagram

```text
       MasterData
       -----------
       PRODUCT ID
       PRODUCT
       CATEGORY
       BUYING PRIZE
       SELLING PRICE
       UOM
            |
            | 1 : *
            |
       InputData
       ----------
       DATE
       Day
       PRODUCT ID
       QUANTITY
       DISCOUNT %
       Other transaction fields
```

*The diagram is a logical representation. Confirm the actual relationship columns and filter direction in Power BI Desktop.*

### 6. Data Modelling Approach

The existing two-table model is retained for this portfolio project.

The model supports:
- Product-level sales analysis.
- Category-level performance analysis.
- Transaction-level calculations.
- Sales and cost calculations using product pricing attributes.
- Time-based sales analysis.

### 7. Data Quality Considerations

The source workbook was inspected for:
- Missing values.
- Duplicate transaction records.
- Hidden worksheets.
- External workbook links.

The original workbook also contains volatile discount formulas. The public dataset should use fixed discount values to ensure reproducible reporting.

### 8. Power BI Implementation

The model is used with Power BI measures and report visuals to calculate and display business KPIs.

The following areas should be validated before publication:
- Relationship key and cardinality.
- Cross-filter direction.
- Data types.
- DAX measure calculations.
- Refresh behaviour.

### 9. Future Improvements

Possible enhancements include:
- Dedicated Date dimension.
- Additional customer or store dimensions, if relevant data becomes available.
- Improved data validation.
- Performance optimisation for larger datasets.

These are potential future enhancements, not changes made to the current model.

### 10. Summary

The current model connects product master data with sales transactions through a one-to-many relationship. It provides the foundation for interactive retail sales and profitability reporting in Power BI.
