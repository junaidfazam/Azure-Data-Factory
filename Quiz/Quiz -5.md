<h1 align="center">Azure Data Factory (ADF) Quiz - 5</h1>

### 1. What is the primary function of pipelines in Azure Data Factory?  
Pipelines in Azure Data Factory are primarily used for orchestration and data movement. They define the flow of activities and control how data moves between different sources and destinations, but they do not transform the data itself.

### 2. What are mapping data flows used for in Azure Data Factory?  
Mapping data flows in Azure Data Factory are specifically designed for data transformations. They provide a visual environment to build ETL (Extract, Transform, Load) or ELT (Extract, Load, Transform) logic without writing code.

### 3. How can you load 100 tables from a source database to a target efficiently using Azure Data Factory?  
An efficient way to load 100 tables from a source database is to query the system information schema to get a list of all table names. This list can then be used in a ForEach activity within a pipeline to iteratively copy each table's data.

### 4. Which Azure Data Factory activity is used to retrieve a list of table names from a database's system information schema?  
The Lookup activity in Azure Data Factory can be used to execute a query against the system information schema of a database to retrieve a list of table names.

### 5. How can you handle duplicate rows within a mapping data flow?  
Duplicate rows within a mapping data flow can be handled using the Aggregate transformation. This allows you to group data based on specified columns and apply aggregation functions, effectively removing duplicates.

### 6. What is the purpose of the Conditional Split transformation in a mapping data flow?  
The Conditional Split transformation is used to divide incoming data into different streams based on specified conditions. This allows you to route data to different transformations or destinations based on data characteristics.

### 7. How can you handle bad records, such as incorrect date formats, in a specific column within a mapping data flow?  
Bad records with incorrect formats, like bad dates, can be handled using the Conditional Split transformation. You can define a condition using the expression builder to identify and route records that do not meet the expected format to a separate stream or destination.

### 8. What is the key difference between pipelines and data flows in terms of their functionality?  
The key difference is that pipelines orchestrate and move data, while data flows transform data. Data flows are typically called and executed within pipelines to perform the necessary data manipulations.

### 9. When building a pipeline, how would you incorporate a data transformation designed in a mapping data flow?  
You can incorporate a mapping data flow into a pipeline by using the Data Flow activity. You add the Data Flow activity to your pipeline and then configure it to reference the specific mapping data flow you want to execute.

## 10. What do the integration runtime, compute type, and core count settings in a data flow activity configuration relate to?  
These settings relate to the underlying compute resources used to execute the mapping data flow. They are similar to configuring a cluster, determining the size and scale of the virtual machines used for the data transformation process.

