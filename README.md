# Online Retail Sales Dataset  

## Overview

The data represents **transactional sales records** from an Indonesia-based online retail company that sells **unique all-occasion gifts**. Many of the company's customers are **wholesalers** who purchase products in bulk.

The dataset contains transactions between:

**2024 – 2025**

Students are required to perform an **ETL process (Extract, Transform, Load)** to integrate the data and build a **Data Warehouse for sales analysis**.

---

## Data Sources

The dataset originates from **two operational systems**.

### 1. Indonesia Sales System
- Format: **CSV**
- File provided in this repository

```
indonesia_sales.csv
```

This dataset contains **transactions from Indonesian customers**.

---

### 2. International Sales System
- Format: **MySQL Database**
- Provided through a **public database connection**

Students must connect to the MySQL database using **Python** to extract the international sales data.

---

## Dataset Structure

Each row represents **one product sold within an invoice transaction**.

| Column | Data Type | Description |
|------|------|------|
| InvoiceNo | String | Unique identifier of the invoice |
| StockCode | String | Unique product identifier |
| Description | String | Product name or description |
| Quantity | Integer | Number of items purchased |
| InvoiceDate | Datetime | Date and time when the transaction occurred |
| UnitPrice | Decimal | Price per unit of the product |
| CustomerID | Integer | Unique identifier of the customer |
| Country | String | Country where the customer is located |
| Region | String | Geographic region classification |
| Category | String | Product category classification |

---

## Column Descriptions

### InvoiceNo
Unique identifier assigned to each invoice.

Example:
```
536365
```

One invoice may contain **multiple products**, resulting in multiple rows with the same `InvoiceNo`.

---

### StockCode
Unique identifier assigned to each product.

Example:
```
85123A
```

---

### Description
Name or description of the product.

Example:
```
WHITE HANGING HEART T-LIGHT HOLDER
```

---

### Quantity
Number of units purchased in the transaction.

Example:
```
6
```

---

### InvoiceDate
Date and time when the transaction occurred.

Example:
```
2025-03-15 10:45:00
```

---

### UnitPrice
Price of a single unit of the product.

Example:
```
2.55
```

---

### CustomerID
Unique identifier assigned to each customer.

Example:
```
17850
```

---

### Country
Country where the customer is located.

Example:
```
Indonesia
```

---

### Region
Higher-level geographic classification.

Possible values include:

- Asia Pacific  
- Europe  
- North America  

Example:
```
Asia Pacific
```

---

### Category
Product category assigned to the item.

Example values:

- Home Decoration  
- Gift Items  
- Seasonal Products  
- Toys  

Example:
```
Home Decoration
```

---


---

## Fact Table Grain

The expected grain of the data warehouse fact table is:

> **One row represents one product sold in one transaction on a specific date.**

---

## Assignment Workflow

Students are expected to complete the following steps:

1. **Extract** data from CSV and MySQL sources  
2. **Transform** and clean the datasets  
3. **Integrate** both datasets into one unified dataset  
4. **Model** a star schema for the data warehouse  
5. **Load** the data into PostgreSQL (Supabase)  
6. **Analyze** the data using SQL queries  

---

## Repository Contents

```
indonesia_sales.csv
README.md
```

The **international sales dataset** will be accessed via **MySQL database connection** provided during the assignment.

---

## Notes

- Both sources share the **same schema structure**.
- Students must **integrate both datasets before loading them into the warehouse**.
- The final warehouse should support **analytical sales queries**.

---

## License

This dataset is provided **for educational purposes only** as part of the Data Warehousing course assignment.
