

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

 -Population Data
  - Input format      : [Specify format]
  - Input location    : [Specify location]
  - Output format     : [Specify format]
  - Output location   : [Specify location]
  - Ingestion Condition: Only if file has 100 rows
  - Ingestion         : As soon as file arrives
  - Trigger           : [Specify if using ADF trigger]
  - Post-process      : Delete the file after ingestion

    - Covid-19 Data
    - Config Location   : blob config
    - JSON Config File contains:
      - Base URL
       - Relative URL
       - File name
    - Schedule          : Daily at midnight
    - Output format     : [Specify format]

#### Transformation Requirement

#### SQL BI Requirements
- Schema: covid_reporting
- Tables:
   - cases_and_deaths
   - hospital_admissions_daily
   - testing
- Trigger: [Specify trigger mechanism]

