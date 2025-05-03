<h1 align="center">Azure Data Factory (ADF) Quiz - 2</h1>

### 1. What are the three different ways to execute pipelines in Azure Data Factory?  
There are three main ways to execute pipelines: Debug mode, manual triggering, and triggering through defined triggers (like blob events). These methods allow for different testing and automated execution scenarios.

### 2. What are ARM templates in the context of Azure Data Factory, and what format do they use?  
ARM templates (Azure Resource Manager templates) in ADF are essentially JSON files that represent the code and configuration of data factory components like pipelines, datasets, and linked services. While ADF uses a visual drag-and-drop interface, this interface generates the underlying JSON code.

### 3. Why are ARM templates important for deploying Data Factory code to higher environments?  
ARM templates allow for the automated deployment of data factory configurations to different environments (like UAT or Production) without manually recreating everything. They enable CI/CD pipelines for consistent and efficient code migration.

### 4. How is a code repository typically integrated with Azure Data Factory for deployment?  
Azure Data Factory can be linked to a code repository (like Azure DevOps). Changes are made in feature branches, merged into development branches, and then published. The publishing process generates the ARM templates in the repository, which can then be used for deployment.

### 5. Describe the process of using feature branches and pull requests for managing Data Factory code deployments.  
Developers work on their code in isolated feature branches. Once changes are complete, they create a pull request to merge their code into a more stable branch (like the development branch). This allows for code review and integration before publishing.

### 6. What is the purpose of the "Publish all" option in Azure Data Factory when a code repository is configured?  
When a code repository is linked and code is merged to the designated branch, clicking "Publish all" generates the ARM templates representing the current state of the data factory in the linked repository. These generated templates are crucial for subsequent deployments.

### 7. What is a common difficulty encountered when copying data from an on-premise source to a cloud destination using Data Factory?  
A common difficulty is the slow throughput and speed of data transfer from on-premise systems to cloud storage due to factors like network latency and bandwidth.

### 8. How can enabling staging help improve the performance of data copy activities from on-premise sources?  
Enabling staging uses a temporary storage account to compress the data before transferring it from on-premise. The data is then decompressed on the cloud side before being loaded into the final destination. This compression significantly improves transfer speed.

### 9. Explain the concept of "Degree of copy parallelism" in the context of Data Factory copy activities.  
Degree of copy parallelism refers to the number of threads used concurrently during a copy activity. Increasing this value can improve performance by allowing more data to be transferred simultaneously, although the optimal value may require testing.

### 10. While Data Integration Units (DIUs) are mentioned as a performance tuning option, why are they generally considered less impactful than other methods like staging or copy parallelism?  
The source material suggests that while DIUs (representing CPU power) might help in some cases, they do not typically provide as significant a performance improvement for copy activities as enabling staging with compression and adjusting the degree of copy parallelism.
