<h1 align="center">Azure Data Factory (ADF) Quiz</h1>

### 1. What is Azure Data Factory (ADF)?  
ADF is a cloud-based ETL (Extract, Transform, Load) or ELT (Extract, Load, Transform) service managed by Azure. It is serverless and helps with data integration, orchestration, and transformation.

### 2. What is the purpose of a Linked Service in ADF?  
A Linked Service defines the connection information needed to connect ADF to an external data source or sink. It contains configurations or connection details, like connection strings or credentials.

### 3. What is a Data Set in ADF?  
A Data Set is a pointer to the specific data within a linked service. It defines the structure, location, and format of the data you want to use as input or output in a pipeline activity.

### 4. Explain the relationship between a Linked Service and a Data Set.  
A Linked Service establishes the connection to a data store, while a Data Set defines the specific data (e.g., a table, file, or folder) within that connected data store. You must have a Linked Service before you can define a Data Set pointing to data within it.

### 5. What is an Integration Runtime (IR) in ADF?  
An Integration Runtime is the compute environment that ADF uses to execute activities. It acts as a bridge between activities and linked services, providing the resources needed for data movement or transformation.

### 6. Name the three main types of Integration Runtimes discussed.  
The three main types are Azure Integration Runtime (often referred to as Auto-Resolve IR), Self-Hosted Integration Runtime, and Azure SSIS Integration Runtime.

### 7. When would you use a Self-Hosted Integration Runtime?  
You would use a Self-Hosted Integration Runtime when you need to connect Azure Data Factory to on-premises data sources or destinations.

### 8. When would you use an Azure SSIS Integration Runtime?  
An Azure SSIS Integration Runtime is used to lift and shift or execute SQL Server Integration Services (SSIS) packages within Azure Data Factory.

### 9. What is the purpose of Triggers in ADF?  
Triggers are used to execute ADF pipelines automatically based on a defined schedule, event, or tumbling window. They eliminate the need for manual pipeline execution.

### 10. Name the three types of Triggers discussed.  
The three types of triggers are Event Trigger, Tumbling Window Trigger, and Schedule Trigger.
