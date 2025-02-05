# Tokyo-Olympics-Azure-ETL

## Architecture Diagram
![alt text](https://github.com/Nasr-Syed/Tokyo-Olympics-Azure-ETL/blob/2408c63da6de87edc469dedbc5aca4f5b44f160d/images/Architecture%20Diagram.png)

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