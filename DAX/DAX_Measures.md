# DAX Measures Documentation
## Retail Sales Analytics Dashboard

### 1. Overview

DAX (Data Analysis Expressions) is used in Power BI to calculate business KPIs and perform dynamic sales analysis.

This document describes the proposed core measures for the Retail Sales Analytics Dashboard.

**Note:** These formulas are proposed definitions and must be compared with the actual measures in the PBIX before being described as implemented.

### 2. Total Sales

**Business Definition:** Net sales value after applying discounts.

```dax
Total Sales =
SUMX(
    InputData,
    InputData[QUANTITY] *
    RELATED(MasterData[SELLING PRICE]) *
    (1 - InputData[DISCOUNT %])
)
```

### 3. Total Quantity

**Business Definition:** Total quantity of products sold.

```dax
Total Quantity =
SUM(InputData[QUANTITY])
```

### 4. Total Cost

**Business Definition:** Total purchase cost of the products sold.

```dax
Total Cost =
SUMX(
    InputData,
    InputData[QUANTITY] *
    RELATED(MasterData[BUYING PRIZE])
)
```

### 5. Total Profit

**Business Definition:** Difference between net sales and total product cost.

```dax
Total Profit =
[Total Sales] - [Total Cost]
```

### 6. Profit Margin %

**Business Definition:** Profit as a percentage of net sales.

```dax
Profit Margin % =
DIVIDE(
    [Total Profit],
    [Total Sales],
    0
)
```

### 7. DAX Functions Used

| Function | Purpose |
|---|---|
| SUM | Calculates total quantity |
| SUMX | Performs row-by-row calculations |
| RELATED | Retrieves related product pricing |
| DIVIDE | Handles division safely |

### 8. Filter Context

The measures respond dynamically to report filters such as:
- Year
- Month Name
- Sale Type
- Payment Mode

### 9. Validation Checklist

Before publication, verify:
- Actual column names and data types.
- Discount values are stored as decimal percentages.
- Relationship between InputData and MasterData.
- Sales calculation and discount treatment.
- Cost and profit calculation.
- Profit margin definition.
- Results against Power BI Desktop visuals.

### 10. Summary

These measures provide the foundation for sales, quantity, cost and profitability analysis. Final implementation details should match the validated Power BI report.
