# Dataset Dictionary

## Retail Sales Analytics – Dataset Documentation

### 1. Dataset Overview

The dataset contains retail sales transaction records and product master information used to build the Power BI dashboard.

### 2. Source Tables

| Table Name | Description | Data Granularity |
|---|---|---|
| InputData | Sales transaction records | One row per transaction |
| MasterData | Product details and pricing information | One row per product |

### 3. InputData – Transaction Table

This table stores sales transaction details.

Fields identified in the source workbook include:

- Date
- Day
- Product ID
- Quantity
- Discount Percentage
- Sale Type
- Payment Mode

### 4. MasterData – Product Table

This table stores product-level information.

Fields identified in the source workbook include:

- Product ID
- Product Name
- Category
- Buying Price
- Selling Price
- Unit of Measurement (UOM)

### 5. Data Relationship

The model connects InputData and MasterData through Product ID.

- MasterData: One side
- InputData: Many side
- Relationship: One-to-many

### 6. Data Preparation

The source data is prepared for reporting and analysis using Power BI.

Data preparation includes reviewing data types, checking product identifiers, and validating the relationship between transaction and product information.

### 7. Usage

The dataset supports sales, quantity, cost, profit, product, category, payment mode and time-based analysis.

### 8. Data Privacy

This portfolio should contain only sample or authorised data. No confidential business, customer or personal information should be published.
