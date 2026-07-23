![Data Pipeline Workflow](image.png)
# 🐍 Python Automation & Data Engineering Toolkit

Welcome to my personal collection of Python utility scripts, ETL helpers, and workflow shortcuts! 

This repository serves as a modular toolkit designed to automate repetitive data preparation tasks, eliminate manual data wrangling errors, and optimize day-to-day analytics workflows.

---

## 🛠️ Repository Contents & Shortcuts Index

| Category | Script / Notebook | Description | Key Tech / Modules |
| :--- | :--- | :--- | :--- |
| **ETL & File Prep** | `folder_to_single_file.py` | Automatically merges a folder of CSV/Excel files into a single master workbook; splits datasets exceeding Excel's 1.04M row limit. | `pandas`, `openpyxl`, `re`, `os` |
| **Database Pipelines** | `retrive_tables_to_mysql.py` | Automatically creates database schemas and streams multi-table Excel/CSV datasets directly into MySQL. | `sqlalchemy`, `pandas`, `mysql-connector` |
| **Data Ingestion** | `retrive_tables.py` | Ingests multi-sheet workbooks into native Jupyter DataFrames while bypassing corrupted `zipfile` CRC metadata errors. | `pandas`, `zipfile`, `globals()` |
| *(Future Tools)* | *Coming Soon* | *More daily automation scripts and helper functions will be continuously added here.* | `Python` |

---

## 🚀 Highlights & Problem Solving

### 1. Bypassing Excel's 1.04M Row Limit
* Large web analytics and POS transaction files frequently exceed Excel’s hard limit (`1,048,576` rows).
* The `folder_to_single_file` utility automatically detects file sizes and programmatically splits large datasets across structured chunk sheets (`_part1`, `_part2`) without data loss.

### 2. Automated MySQL Database Ingestion
* Programmatically handles connection setups, table creation, column name cleaning/sanitization, and direct SQL streaming for fast local analysis.

---

## 🧰 Prerequisites & Installation

To run any script in this collection, ensure you have Python 3.x installed along with the required libraries:

```bash
pip install pandas openpyxl sqlalchemy mysql-connector-python
