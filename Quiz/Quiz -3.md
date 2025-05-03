<h1 align="center">Azure Data Factory (ADF) Quiz - 3</h1>

## 1. What is the primary function of the Copy Data activity in Azure Data Factory?  
The Copy Data activity is used to simply copy data from a source location to a target location.

### 2. Explain the purpose of the ForEach activity.  
The ForEach activity is used to iterate over a collection and execute a set of activities for each item in the collection, effectively looping through actions.

### 3. What kind of information can you obtain using the Get Metadata activity? Name at least three types.  
The Get Metadata activity can provide information about a data set such as item names, item type (file or folder), last modified date, size, and existence.

### 4. When would you use the Set Variable activity?  
The Set Variable activity is used to define a variable within a pipeline and assign a value to that variable.

### 5. How does the Wait activity function?  
The Wait activity pauses the execution of a pipeline for a specified duration, measured in seconds.

### 6. What is the main use case for the Validation activity?  
The Validation activity is used to check for the presence of a file or folder at a specified location before proceeding with subsequent activities.

### 7. Which activity is typically used to trigger HTTP requests?  
The Web activity and Webhook activity are typically used to trigger HTTP requests from within an Azure Data Factory pipeline.

### 8. If you need to execute a query and retrieve its output within a pipeline, which activity should you use?  
The Lookup activity is used to execute a query against a data source and retrieve the output of that query.

### 9. How can you pass parameters to a Databricks notebook when executing it from Azure Data Factory?  
Parameters can be passed to a Databricks notebook in the Execute Notebook activity through the "Base Parameters" option.

### 10. What happens if you execute a notebook with the Execute Notebook activity but don't specify parameters, and the notebook expects them?  
If parameters are not specified in the Execute Notebook activity but the notebook expects them, the default parameters defined within the notebook itself will be used.
