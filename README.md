# Project Requirement: Azure Data Factory Pipeline for COVID-19 Analytics

## Objective
Design and implement a scalable data pipeline using Azure Data Factory to ingest, transform, and store COVID-19-related data to support BI reporting and AI/ML analytics.

---

## 1. Ingestion Sources

### From GitHub
- `cases_deaths.csv`
- `country_response.csv`
- `hospital_admissions.csv`
- `testing.csv`

### From Azure Blob Storage
- `population_data.csv`

> All ingested data is stored in **Azure Data Lake Storage Gen2 (Raw Layer)**.

---

## 2. Transformation Process

### A. Azure Data Factory – Data Flow Outputs
- `cases_deaths` – Cleaned and structured
- `hospital_admissions_weekly` – Aggregated weekly data
- `hospital_admissions_daily` – Cleaned daily-level data

### B. Azure Databricks – Notebook Outputs
- `population_data` – Transformed demographic and regional insights
- `testing_data` – Enriched metrics including positivity rates and capacity

---

## 3. Storage Targets

- **Azure SQL Database**
  - For BI dashboards and reporting (e.g., Power BI)
  
- **Azure Data Lake Storage Gen2 (Processed Layer)**
  - For AI/ML modeling and analytics

---

## 4. Tools and Services

- Azure Data Factory (Pipelines, Data Flows)
- Azure Databricks (Notebook-based transformations)
- Azure Data Lake Storage Gen2
- Azure SQL Database
- GitHub (as source)
- Azure Blob Storage (as source)

---

## Architecture Flow

```text
Ingestion:
  GitHub / Blob Storage
         ↓
Azure Data Factory Pipelines
         ↓
    ADLS Gen2 (Raw)

Transformation:
  - ADF Data Flows: cases, hospital admissions
  - Databricks: population, testing
         ↓

Storage:
  - ADLS Gen2 (Processed) → AI/ML
  - Azure SQL Database → BI/Reporting
