# AWS_Glue_End_to_End_Project

## Project Workflow:

**1. Data Ingestion:**

Raw data in CSV format is uploaded to an Amazon S3 bucket, serving as the initial data source.
AWS Glue Crawler is configured to automatically discover and catalog metadata about the newly uploaded CSV files, making them accessible for further processing.
Screenshots/buckets.JPG

**2. Data Cataloging:**

Catalog tables are created in the AWS Glue Data Catalog, enabling structured access to the ingested data.
These cataloged tables provide a clear schema for the data, making it easier to work with during transformations.

**3. Data Transformation:**

An AWS Glue Job is designed to perform data transformations based on specific requirements.
The Glue Job uses the source data, selects relevant fields, and filters data based on countries, focusing on records from Pakistan and Australia.

**4. Data Loading:**

The transformed data is loaded into a target S3 bucket, creating a refined dataset that is ready for further analysis or consumption.


**5. Automation and Orchestration:**

AWS Lambda is employed to automate and orchestrate the entire data transformation process.
Lambda functions trigger the Glue Job, ensuring that data processing occurs promptly after new uploads.
This automated workflow optimizes efficiency and minimizes manual intervention.
