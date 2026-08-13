# Assignment Overview

Module: Data Warehouse (PostgreSQL)

Overview
This module covers the design and population of a star schema data warehouse for e-commerce sales and construction of reporting artifacts.

Objectives
- Design a star schema (dimensions: `DimDate`, `DimCategory`, `DimCountry`; fact: `FactSales`).
- Implement the schema in PostgreSQL (DDL available in `CREATE-SCRIPT.sql`).
- Load provided CSV datasets into the corresponding dimension and fact tables.
- Build reporting SQL examples: grouping sets, ROLLUP, CUBE, and a materialized view for total sales per country.

Files
- `CREATE-SCRIPT.sql` — DDL for `DimDate`, `DimCategory`, `DimCountry`, `FactSales`
- `DimDate.csv`, `DimCategory.csv`, `DimCountry.csv`, `FactSales.csv` — sample data to load

Deliverables
- A working `softcart`/`staging` schema with populated dimensions and fact table.
- Sample reporting queries demonstrating grouping sets, ROLLUP, and CUBE.
- An MQT (materialized view) or equivalent summarization named `Total_sales_per_country`.

