# Walmart Data Engineering Pipeline

An end-to-end data engineering project that demonstrates automated data ingestion, incremental processing, transformation, data quality, and workflow orchestration using **Apache Airflow, Databricks, dbt, PostgreSQL, and Amazon S3**.

## Project Overview

This project implements a data engineering pipeline for processing Walmart-related data through multiple stages of ingestion, storage, transformation, and modeling. The pipeline uses **Apache Airflow** to orchestrate workflows, **Amazon S3** for cloud data storage, **Databricks** for data processing, and **dbt** for transformation and data modeling.

The project follows modern data engineering practices including **incremental processing, metadata-driven pipelines, data quality testing, snapshots, Slowly Changing Dimensions (SCD), and Star Schema modeling**.

## Architecture

```text
PostgreSQL
    │
    ▼
Apache Airflow
    │
    ▼
Amazon S3
    │
    ▼
Databricks
    │
    ▼
dbt
    │
    ├── Staging Models
    │
    ├── Intermediate Models
    │
    └── Mart Models
            │
            ▼
    Analytics-Ready Data
```

## Technologies Used

- **Python** – Pipeline scripting and data processing
- **PostgreSQL** – Source database
- **Apache Airflow** – Workflow orchestration and scheduling
- **Amazon S3** – Cloud object storage and data lake layer
- **Databricks** – Data processing and transformation
- **PySpark** – Distributed data processing
- **dbt** – Data transformation, modeling, testing, and snapshots
- **Delta Lake** – Reliable data storage and processing
- **Git/GitHub** – Version control

## Key Features

- Extracted data from PostgreSQL as part of the data ingestion workflow.
- Stored source and processed data in Amazon S3.
- Built Airflow DAGs to automate and orchestrate data pipeline workflows.
- Implemented **incremental data processing** to avoid unnecessary reprocessing.
- Developed **metadata-driven pipeline workflows** for scalable data ingestion.
- Processed and transformed datasets using Databricks and PySpark.
- Developed modular dbt models for analytics-ready datasets.
- Implemented dbt **data quality tests and snapshots**.
- Applied **Slowly Changing Dimensions (SCD)** to maintain historical changes.
- Designed fact and dimension tables using **Star Schema** modeling.

## Data Pipeline

### 1. Data Ingestion

Data is extracted from the PostgreSQL source system and moved into the cloud storage layer for downstream processing.

### 2. Data Storage

Amazon S3 is used as the cloud storage layer for maintaining raw and processed datasets.

### 3. Data Processing

Databricks and PySpark are used to process and transform the data efficiently.

### 4. Data Transformation

dbt is used to build modular transformation models and prepare datasets for analytics.

### 5. Data Quality

dbt tests are implemented to validate data and identify potential data quality issues.

### 6. Historical Data Management

dbt snapshots and Slowly Changing Dimensions are used to track changes and maintain historical records.

### 7. Data Modeling

The final datasets are organized into fact and dimension tables using a Star Schema for analytical workloads.

## Project Objective

The objective of this project is to demonstrate a complete modern **data engineering workflow**, covering data ingestion, cloud storage, distributed processing, transformation, orchestration, data quality, historical data management, and dimensional modeling using AWS, Databricks, Airflow, and dbt.
