# Azure Data Factory COVID-19 Data Integration Pipeline Documentation

    ## 1. Introduction

    This project demonstrates an end-to-end **data pipeline** built using **Azure Data Factory (ADF)** to ingest, transform, and store COVID-19-related datasets for **Business Intelligence (BI)** and **Machine Learning (ML)**. The pipeline pulls data from multiple sources, processes it, and stores it in **Azure SQL Database** and **Azure Data Lake Storage Gen2**.

    ---

    ## 2. Data Sources

    ### GitHub Repositories
    - `cases_deaths.csv`: Contains data about COVID-19 cases and deaths by country.
    - `country_response.csv`: Government response data by country.
    - `hospital_admissions.csv`: Weekly hospital admissions due to COVID-19.
    - `testing.csv`: Testing rates and outcomes.

    ### Azure Blob Storage
    - `population_data.csv`: Contains demographic data at the country level.

    ---

    ## 3. Data Ingestion & Transformation

    ### Data Flow
    - **ADF Pipelines**:
      - Ingest data from GitHub and Azure Blob Storage.
      - Trigger **Data Flows** to clean and structure the data.
      - **Transformation Logic**:
        - `cases_deaths`: Cleaned data ready for BI reporting.
        - `hospital_admissions`: Aggregated and cleaned data (weekly and daily).

    ### Databricks
    - **Population Data**: Advanced processing on population demographics.
    - **Testing Data**: Enriched with testing metrics and positivity rates.

    ---

    ## 4. Data Storage

    - **Azure Data Lake Gen2**: Raw and processed data, ready for **AI/ML**.
    - **Azure SQL Database**: Cleaned data for **BI reporting** (e.g., Power BI).

    ---

    ## 5. Triggers and Automation

    - **Ingestion Trigger**: Automatically triggers the ingestion pipeline when file is available.
    - **Transformation Trigger**: Starts the data transformation flows based on previous triggers.
    - **Schedule Trigger**: Runs pipelines on a scheduled basis (e.g., daily, weekly).

    ---

    ## 6. Tools & Technologies

    - **Azure Data Factory (ADF)**: Orchestrates the pipeline and triggers.
    - **Azure Databricks**: For complex data transformations.
    - **Azure Blob Storage**: For dataset storage.
    - **Azure Data Lake Gen2**: For processed data storage.
    - **Azure SQL Database**: For BI reporting tables.
    - **GitHub**: Data source repository.

    ---

    ## 7. Future Enhancements

    - Add automated alerts to monitor pipeline failures.
    - Implement data validation post-ingestion and transformation.
    - Integrate CI/CD pipelines to deploy and manage ADF pipelines.
    