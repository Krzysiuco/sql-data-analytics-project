---

# Customer & Product Analytics Reports (SQL Server)

This repository contains advanced SQL Server reporting views designed for customer and product analytics.
The project demonstrates data aggregation, KPI calculations, customer segmentation, and product performance analysis using transactional sales data.

## Overview

The solution consists of two analytical SQL views:

* `gold.report_customers`
* `gold.report_products`

Both reports are built using Common Table Expressions (CTEs), aggregations, business logic, and KPI calculations to support business intelligence and reporting workflows.

---

# Customer Report

The `gold.report_customers` view provides a complete customer-level analytical summary.

## Features

### Customer Information

* Full customer name
* Age calculation
* Age group segmentation

### Customer Segmentation

Customers are classified into:

* **VIP**
* **Regular**
* **New**

based on:

* account lifespan
* total revenue generated

### Customer KPIs

The report calculates:

* Total orders
* Total sales
* Total quantity purchased
* Number of unique products purchased
* Latest order date
* Customer lifespan (months)
* Recency (months since last order)
* Average order value
* Average monthly spend

## Techniques Used

* CTEs (`WITH`)
* Aggregations
* `CASE WHEN`
* `DATEDIFF`
* `COUNT(DISTINCT)`
* Defensive division using `NULLIF`
* SQL Server Views

---

# Product Report

The `gold.report_products` view delivers product-level sales and performance analytics.

## Features

### Product Information

* Product name
* Category
* Subcategory
* Product cost

### Product Segmentation

Products are categorized as:

* **High-Performer**
* **Mid-Range**
* **Low Performer**

based on total generated revenue.

### Product KPIs

The report calculates:

* Total sales
* Total quantity sold
* Total orders
* Total customers
* Product lifespan
* Most recent sale
* Recency in months
* Average order revenue
* Average monthly revenue

## Techniques Used

* Multi-table joins
* CTEs
* KPI calculations
* Revenue segmentation
* Time-based analytics
* SQL Server Views

---

# Technologies

* Microsoft SQL Server
* T-SQL

---

# Skills Demonstrated

* Data Analytics
* SQL Reporting
* Business Intelligence
* Data Aggregation
* KPI Design
* Customer Segmentation
* Product Performance Analysis
* Query Optimization Principles

---

# Example Use Cases

These reports can be used for:

* Executive dashboards
* Customer behavior analysis
* Product performance monitoring
* Sales analytics
* Business intelligence solutions
* Power BI / Tableau integrations

---

# Database Structure

The reports use the following tables:

## Fact Table

* `gold.fact_sales`

## Dimension Tables

* `gold.dim_customers`
* `gold.dim_products`

---
