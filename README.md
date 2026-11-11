
# CARESYNC – End-to-End Data Engineering Project

## Project Overview
CARESYNC is an end-to-end Data Engineering project built using Azure Data Factory, Azure Databricks, PySpark, and Azure SQL Database.

The project focuses on data ingestion, transformation, data quality, audit logging, pipeline orchestration, and business analytics using the Medallion Architecture.

## Technology Stack
- Azure Data Factory (ADF)
- Azure Databricks
- PySpark and Apache Spark
- Azure Data Lake Storage (ADLS)
- Azure SQL Database
- PostgreSQL
- Azure Logic Apps
- SQL
- Power BI

## Data Architecture

The project follows the Medallion Architecture:

### 1. Bronze Layer
- Ingest raw data from source systems.
- Store raw data in the Bronze layer.
- Support incremental and batch data loading.

### 2. Silver Layer
- Transform and cleanse source data.
- Apply data validation and transformation logic.
- Prepare structured data for downstream processing.

### 3. Gold Layer
- Generate business-ready analytical datasets.
- Build hospital, patient, and laboratory analytics.
- Support reporting and dashboard development.

## Azure Data Factory
- Orchestrate data ingestion and transformation pipelines.
- Execute child pipelines for ADLS CSV and PostgreSQL sources.
- Monitor pipeline execution status.
- Maintain pipeline execution audit logs.

## Audit Logging and Monitoring
Azure SQL Database is used to maintain pipeline execution details, including:
- ADF Run ID
- Table ID
- Execution stage
- Execution status
- Records written
- Start and end timestamps

## Automated Email Notifications
Integrated Azure Data Factory with Azure Logic Apps using an HTTP trigger.

Key features:
- Automated SUCCESS and FAILED notifications.
- Dynamic pipeline execution details.
- Table-level execution status reporting.
- HTML-formatted email reports.
- Outlook email notification integration.

## Databricks Gold Insights Dashboard
The CARESYNC Gold Insights dashboard includes:
- Executive Overview
- Patient Demographics & Risk
- Hospital Operations
- Lab Test Trends

## Repository Structure

```text
caresync-adb-repo/
│
├── Gold/
│   ├── NB_hospital_daily_summary.ipynb
│   ├── NB_lab_test_trends.ipynb
│   ├── NB_patient_360.ipynb
│   └── sttm_silver_to_gold.xlsx
│
├── Landing_to_Bronze.ipynb
├── Bronze_to_Silver.ipynb
├── Prepare calendar table.ipynb
└── README.md
```

## Project Objective
To build a scalable data engineering solution that integrates data ingestion, transformation, orchestration, monitoring, automated notifications, and business intelligence reporting.

---

**Project:** CARESYNC  
**Focus:** End-to-End Data Engineering  
**Architecture:** Medallion Architecture (Bronze, Silver, Gold)
