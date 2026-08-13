# Assignment Overview

Module: OLTP Database (MySQL)

Overview
This module focuses on designing and populating an OLTP transactional schema for sales data and automating basic maintenance tasks.

Objectives
- Design a transactional table to store sales (columns: rowid, product_id, customer_id, price, quantity, timestamp).
- Load provided CSV data into MySQL and validate the import.
- Create appropriate indexes (e.g., on `timestamp`) and verify index metadata.
- Automate export/dump tasks with shell scripts.

Files
- `oltpdata.csv` — raw transactional data sample
- `sales_data.sql` — MySQL dump / create-table + data
- `datadump.sh` — mysqldump helper
- `sql_commands.txt` — example SQL commands used during the assignment

Deliverables
- Created and populated `sales_data` table in a `sales` database.
- Index on `timestamp` and verification query output.
- A shell script to export/dump table data (`datadump.sh`).

