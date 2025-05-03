

#### Required Services
 - Azure Data Factory
 - Azure Storage
 - Azure SQL Database & Server
- Azure Databricks

#### Storage Required
 - Azure Gen 2 Storage
   - raw
   - lookup
   - processed

 - Azure Blob Storage
   - population
   - config

#### Ingestion Requirement

  - Population Data
    - format
      - Input  : zip
      - Output : tsv
    - location
      - Input location    : blob/population
      - Output location   : raw/population
    - Ingestion Condition: Only if file has 100 rows
    - Ingestion Frequency        : As soon as file arrives
    - Post-process      : Delete the file after ingestion

  - Covid-19 Data
    - format
      - Input  : csv
      - Output : csv
    - location
      - Input location    : raw/ecdc
      - Output location   : raw/ecdc
    -  Ingestion Condition: Read the config/list to get the file to be ingested
    - Schedule          : Daily at midnight

  - Json File configuration
    - Config Location   : blob config
    - JSON Config File contains:
     - Base URL
     - Relative URL
     - File name

#### Transformation Requirement

#### SQL BI Requirements
- Schema: covid_reporting
- Tables:
   - cases_and_deaths
   - hospital_admissions_daily
   - testing


