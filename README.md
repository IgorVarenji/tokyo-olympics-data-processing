Tokyo Olympics Data Pipeline
This project demonstrates a complete data processing pipeline for analyzing Tokyo Olympic data using various Azure services, including Azure Data Factory, Azure Databricks, and Azure Synapse Analytics.

Project Overview
The goal of this project is to ingest, process, and analyze data related to the Tokyo Olympics. The data pipeline involves three major steps: data ingestion, data transformation, and data analysis.

**Architecture**


Azure Data Factory:
Purpose: Data ingestion.
Process: We created a pipeline that ingests raw data from various sources and stores it in Azure Data Lake Gen 2. The data is organized into different folders based on its type (e.g., athletes, coaches, entries by gender, medals, teams).


Azure Databricks:
Purpose: Data transformation and processing.
Process: We mounted the Azure Data Lake Gen 2 storage in Databricks using OAuth credentials. The raw data was then loaded into Spark DataFrames where we performed schema inference and necessary transformations. Specifically:
Data Transformations: Cast data types, calculated average entries by gender, and aggregated medal counts.
Output: The transformed data was saved back to Azure Data Lake Gen 2 in a structured format.


Azure Synapse Analytics:
Purpose: Data analysis and querying.
Process: Using Synapse SQL, we analyzed the transformed data to gain insights, such as:
Total number of athletes by country.
Total gold, silver, and bronze medals by country.
Average number of male and female participants per discipline.

Project Outcome
This pipeline allows for efficient data processing and analysis, leveraging the power of Azure cloud services to handle large datasets related to the Tokyo Olympics.
