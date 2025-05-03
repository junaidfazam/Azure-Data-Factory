<h1 align="center">Azure Data Factory (ADF) Quiz - 6</h1>

## 1. How can you read the contents of a file in Azure Data Factory?  
To read the contents of a file, you can use the Web activity to get the file's URL from the storage account. The output response from the Web activity, which contains the text of the file, can then be passed to a Set Variable activity.

### 2. What two activities should come to mind when asked about reading a file and displaying its contents in Azure Data Factory?  
The two activities that should come to mind are the Web activity and the Set Variable activity.

### 3. What is the purpose of the Web activity when reading a file in ADF?  
The Web activity is used to provide the URL of the file located in the storage account. It retrieves the content of the file as a response.

### 4. How do you get the actual content of the file after using the Web activity?  
The output of the Web activity will have a response that contains the text of the file. This response, specifically `output.response`, can be passed to a Set Variable activity to get the contents.

### 5. How do you delete files from Blob Storage or ADLS Gen2 using Azure Data Factory?  
To delete files, you can use the Delete activity in the pipeline. You provide the configurations for the specific files or multiple files you want to delete within the Delete activity.

### 6. Can you delete multiple files using the Delete activity?  
Yes, the Delete activity allows you to provide configurations to delete multiple files.

### 7. How can you trigger the deletion of a file as soon as it arrives in storage?  
You can set up an event-based trigger on the pipeline that contains the Delete activity. This trigger will initiate the pipeline execution when a new file arrives.

### 8. How can you ensure a pipeline continues execution even if an activity within it fails?  
To ensure continued execution despite an activity failure, you should link the activities using the "on completion" option instead of "on success."

### 9. Explain the difference between linking activities "on success" versus "on completion".  
Linking activities "on success" means the next activity will only execute if the preceding activity completes successfully. Linking activities "on completion" means the next activity will execute regardless of whether the preceding activity succeeded or failed.

### 10. In the context of activity linking, when would you typically use the "on success" option?  
You would typically use the "on success" option when the subsequent activity is dependent on the successful completion of the preceding activity.
