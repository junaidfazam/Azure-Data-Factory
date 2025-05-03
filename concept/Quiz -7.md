<h1 align="center">Azure Data Factory (ADF) Quiz - 7</h1>

### 1. Describe two ways to send email notifications on Azure Data Factory pipeline failures.  
Two ways to send email notifications on Azure Data Factory pipeline failures are using Alerts and Metrics directly within ADF and integrating with Azure Logic Apps via Web or Webhook activities.

### 2. What is the primary benefit of using Azure Logic Apps with a Webhook activity for sending email notifications on ADF failures compared to alerts and metrics?  
Using Azure Logic Apps with a Webhook activity provides more flexibility and customization options for email content and integration with other services compared to the more basic notifications offered by Alerts and Metrics.

### 3. When describing your ADF project experience, what is the most common type of activity you should emphasize ADF is typically used for?  
When describing your ADF project experience, you should typically emphasize the use of Copy Activities as this is a very common and core functionality of ADF.

### 4. Why is it generally not recommended to describe highly complex data transformations built solely within Azure Data Factory in an interview setting?  
It is generally not recommended to describe highly complex data transformations built solely within Azure Data Factory because for large volumes of data and intricate logic, services like Databricks are often a more feasible and performant solution.

### 5. How do you typically test your Azure Data Factory pipelines when working in a feature branch connected to a code repository?  
You typically test your Azure Data Factory pipelines when working in a feature branch by using the Debug mode within the ADF portal.

### 6. What ADF activity is recommended for logging pipeline execution details to a database?  
The Stored Procedure activity is recommended for logging pipeline execution details to a database in Azure Data Factory.

### 7. How can you pass system-defined parameters (like pipeline run ID) to a Stored Procedure activity in Azure Data Factory?  
You can pass system-defined parameters to a Stored Procedure activity in Azure Data Factory by using the dynamic content option and selecting the desired system variables.

### 8. What is the purpose of the Get Metadata activity in Azure Data Factory?  
The purpose of the Get Metadata activity in Azure Data Factory is to retrieve metadata about data objects such as files, folders, and tables.

### 9. What information does the "Child Items" property of the Get Metadata activity provide when the linked dataset points to a folder?  
When the linked dataset points to a folder, the "Child Items" property of the Get Metadata activity provides a list of the items (files and subfolders) contained within that folder.

### 10. Provide a practical use case for the "Child Items" property of the Get Metadata activity.  
A practical use case for the "Child Items" property is to get the count of files present in a folder, which can then be used to control the pipeline flow based on the number of files.
