<h1 align="center">Azure Data Factory (ADF) Quiz - 4</h1>

## 1. What is incremental data in the context of data loading?  
Incremental data refers to the change data, meaning only the new or modified records that have appeared since the last data load.

### 2. How can a watermark column in a source table help handle incremental data?  
A watermark column (like a date or version number) indicates when a row was inserted or last updated. By tracking the highest watermark value loaded previously, you can identify and load only rows with a higher watermark value.

### 3. Explain the role of a lookup activity in handling incremental data using a watermark column.  
A lookup activity is used to retrieve the last watermark value that was successfully processed. This value is then used to filter the source data and extract only the incremental records.

### 4. What is the purpose of a stored procedure activity after loading incremental data using a watermark column?  
After loading the incremental data, a stored procedure activity can be used to update the reference table that stores the last processed watermark value with the new highest watermark value from the current load.

### 5. Besides a watermark column, what other database technology can be used to handle incremental data from a SQL database?  
The default change tracking technology provided by the database itself (like system changed versions in SQL DB) can be used to track and identify incremental changes.

### 6. How does the "last modified date" feature in Azure Data Factory assist with incremental data loading from Data Lake Gen2?  
Azure Data Factory's "last modified date" filter in the Copy Data activity allows you to specify a time window and load only those files in Data Lake Gen2 that have been modified within that period.

### 7. Describe the file loading behavior known as "time partition" and how it facilitates incremental data loading.  
"Time partition" file loading behavior assumes that files are organized or named with date/time information. ADF can use this structure to identify and load the latest files based on their timestamps in the folder structure or file name.

### 8. What is a potential drawback of using the "time partition" file loading behavior?  
A potential drawback is that ADF might need to scan through a large number of files to identify the latest ones based on their time partitions, which can be time-consuming, especially with a large number of files.

### 9. When a watermark column or time-partitioned files are not available, what alternative mechanism can be used for capturing incremental data?  
Change Data Capture (CDC) tools, such as Qlik Replicate, are external mechanisms that can capture only the incremental changes from a source and load them into a destination like ADLS Gen2.

### 10. What is the primary goal when implementing any of the described methods for handling incremental data?  
The primary goal is to efficiently load only the new or changed data into the destination, avoiding the need to re-process the entire dataset each time and reducing processing time and resources.
