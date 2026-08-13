# Assignment Overview

Module: ETL & Data Pipelines

Overview
This module automates syncing transactional data from a MySQL OLTP database into a PostgreSQL staging warehouse using shell scripts and scheduled jobs.

Objectives
- Extract incremental transactional data from MySQL (recent rows based on timestamp).
- Load extracted data into Postgres staging tables (`sales_data`).
- Transform staging data to populate `DimDate` and `FactSales`.
- Export transformed tables as CSVs for production loading.
- Schedule the ETL with a cron job for regular automation.

Files
- `setupmysqldb.sh` — creates MySQL `sales` DB and loads `sales_olddata.csv` and `sales_newdata.csv`.
- `setuppostgresqldb.sh` — creates Postgres `sales_new` DB and staging tables.
- `ETL.sh` — ETL template for incremental extract, transform, and export.
- `sales_olddata.csv`, `sales_newdata.csv` — sample incremental datasets

Deliverables
- Working shell-based ETL that extracts recent rows, loads into Postgres, runs transforms, and exports CSVs.
- A cron entry example to schedule regular runs.

