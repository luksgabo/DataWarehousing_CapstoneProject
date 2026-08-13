# Capstone Project — Data Engineering

This repository contains a capstone project completed for a Data Engineering course. It demonstrates designing an OLTP schema, building a data warehouse, performing analytics, and creating an ETL pipeline to move transactional data into a staging warehouse.

## Project structure
- Module1_OLTP_Database: OLTP design and MySQL dataset and utilities.
	- `sales_data.sql`, `oltpdata.csv`, `datadump.sh`, `sql_commands.txt`
- Module2_DataWarehouse: Star schema design and CSVs for dimensions and fact table.
	- `CREATE-SCRIPT.sql`, `DimDate.csv`, `DimCategory.csv`, `DimCountry.csv`, `FactSales.csv`
- Module3_DataAnalytics: Analytics tasks and sample ecommerce dataset.
	- `ecommerce.csv`
- Module4_ETL-DataPipelines: ETL scripts and setup for moving data from MySQL to PostgreSQL.
	- `ETL.sh`, `setupmysqldb.sh`, `setuppostgresqldb.sh`, `sales_olddata.csv`, `sales_newdata.csv`, `FormattingFunctions-in-PostgreSQL.md`

## Summary of work
- Module 1 — OLTP: designed a transactional `sales_data` table (product_id, customer_id, price, quantity, timestamp), loaded ~2605 rows, created an index on `timestamp`, and provided dump/export scripts.
- Module 2 — Data Warehouse: designed a star schema with `DimDate`, `DimCategory`, `DimCountry`, and `FactSales` tables and provided CSV data and `CREATE-SCRIPT.sql` to create the tables in PostgreSQL.
- Module 3 — Data Analytics: provided a sample `ecommerce.csv` and followed instructions for creating dashboards and visualizations on IBM Cognos and example queries to explore category and time-based aggregates.
- Module 4 — ETL Data Pipelines: implemented shell scripts to bootstrap MySQL/Postgres databases, extract incremental transactional data, transform into `DimDate` and `FactSales`, and export CSVs for production warehousing. Includes a template `ETL.sh` that selects records newer than a time window.
