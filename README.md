# Tokyo-Olympics-Azure-ETL

## Architecture Diagram
![alt text](https://github.com/Nasr-Syed/Tokyo-Olympics-Azure-ETL/blob/2408c63da6de87edc469dedbc5aca4f5b44f160d/images/Architecture%20Diagram.png)

In this Data Engineering ETL project, a multiple array of products all part of the Microsoft Azure suite were used to conduct a complete ETL workflow. Data was ingested from multiple sources, integrated into the Azure Data Lake Storage (Gen 2) using Azure Data Factory. Data was then transformed in DataBricks using Pyspark, multiple transformations were conducted on dataframes, and transformed data was loaded back into Azure Data Lake storage for analysis. I then integrated Azure Synapse Analytics as part of the ETL pipeline, in order to gather insights from the data using Synapse SQL. 

## Azure Data Factory
Azure Data Factory was utilized as part of the ETL pipeline and E2E flow. Raw data was copied from HTTP file links stored on GitHub.

![alt text](https://github.com/Nasr-Syed/Tokyo-Olympics-Azure-ETL/blob/b3e5aa3c66c8aeeafb5d44a7f9c0c460ff0859d5/images/ADF%20Flow.png)

The Azure Data Factory copy pipeline loaded data from various source systems (in this case multiple .csv files stored on GitHub) from HTTP, and copied successfully onto Azure Data Lake storage.

![alt text](https://github.com/Nasr-Syed/Tokyo-Olympics-Azure-ETL/blob/b19c817b393805cd020a5850879346703e061d75/images/ADF%20Details.png)

Details for one example of a copy block in ADF can be found below in the figure. As seen, HTTP configuration is loaded to pull .csv data from GitHub repository, comma delimited.

![alt text](https://github.com/Nasr-Syed/Tokyo-Olympics-Azure-ETL/blob/b19c817b393805cd020a5850879346703e061d75/images/Example%20of%20one%20copy%20block.png)



## Azure Data Lake Storage 
### Data Lake Gen 2
![alt text](https://github.com/Nasr-Syed/Tokyo-Olympics-Azure-ETL/blob/2408c63da6de87edc469dedbc5aca4f5b44f160d/images/Architecture%20Diagram.png)

## Azure DataBricks
### Data Lake Gen 2 - Transformed files
After data was transformed via Pyspark functions in DataBricks notebooks, files were then written back onto Azure Data Lake Storage (Gen 2) in a "transformed" folder. Files were stored as "Block blob" storage.

![alt text](https://github.com/Nasr-Syed/Tokyo-Olympics-Azure-ETL/blob/2aed8c17ea2b24f07352ef2c0303772768ba8a64/images/Azure%20Data%20Lake%20Storage_transformed.png)

## Azure Synapse Analytics
Azure Synapse Analytics was integrated into this ETL end-to-end workflow, in order to explore the capabilities of data warehousing, using SQL. Tables were integrated from Azure Data Lake, queries were performed on the transformed data sets using Synapse SQL, and resultant queries were exported and stored as .csv files. 

![alt text](https://github.com/Nasr-Syed/Tokyo-Olympics-Azure-ETL/blob/2aed8c17ea2b24f07352ef2c0303772768ba8a64/images/synapse%20database%20tables%20.png)
SQL queries performed in Synapse Analytics below:

![alt text](https://github.com/Nasr-Syed/Tokyo-Olympics-Azure-ETL/blob/2aed8c17ea2b24f07352ef2c0303772768ba8a64/images/azure%20synapse%20queries.png)
