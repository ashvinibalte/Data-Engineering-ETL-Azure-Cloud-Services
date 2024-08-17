# Data Engineering ETL Azure Cloud Services

## Financial Data Processing Using Azure Databricks, Azure Data Factory, and Azure Blob Storage

## Project Overview

This project sets up a comprehensive ETL (Extract, Transform, Load) pipeline for processing financial data. The goal is to automate the ingestion, processing, and storage of financial data using Azure cloud services. The processed data is stored securely and is ready for further analysis and reporting.

## Objectives

- Automate the ingestion of financial data from Yahoo Finance API.
- Process the data using Azure Databricks for transformations.
- Store the raw and processed data in Azure Blob Storage.
- Use Azure Data Factory to orchestrate the entire ETL process.

## Architecture

### 1. Data Ingestion

- **Source:** The project fetches historical financial data for a selected stock (e.g., Apple Inc.) from the Yahoo Finance API.
- **Storage:** The raw data is stored as CSV files in **Azure Blob Storage**, providing a scalable and secure storage solution.

### 2. Data Processing

- **Tool:** Data processing is carried out using **Azure Databricks**, an Apache Spark-based analytics platform.
- **Cluster Setup:** A Databricks cluster is configured to handle data processing tasks. VM size restrictions in the `eastus` region were managed by selecting alternative VM sizes or regions.
- **Processing:** The data undergoes various transformations, such as year-wise aggregation and calculation of average closing prices, within Databricks notebooks.

### 3. ETL Pipeline

- **Orchestration:** **Azure Data Factory** is used to automate the ETL process, linking Azure Blob Storage and Databricks.
- **Data Movement:** The pipeline facilitates data movement from Blob Storage to Databricks and back, ensuring the processed data is securely stored.
- **Automation:** The pipeline is scheduled to run at regular intervals, ensuring timely updates and processing.

### 4. Monitoring and Optimization

- **Monitoring:** Azure Monitor and Databricks' built-in tools are used to track the performance of the pipeline and the Databricks cluster.
- **Optimization:** Regular reviews of cluster configuration and pipeline settings are conducted to ensure optimal performance and cost-efficiency.

## Challenges

- **VM Size Availability:** Challenges were encountered with VM size availability in the `eastus` region, necessitating the selection of alternative VM sizes or regions.
- **Data Management:** The project required careful management of data within Azure Blob Storage, including access controls and lifecycle policies.

## Tools & Technologies

- **Azure Blob Storage**: For storing raw and processed data securely.
- **Azure Databricks**: For processing large volumes of financial data.
- **Azure Data Factory**: For automating and orchestrating the ETL pipeline.
- **Python**: For scripting and performing data transformations.

## Outcomes

The project successfully established a scalable ETL pipeline capable of processing large volumes of financial data. The processed data is securely stored in Azure Blob Storage, ready for advanced analytics and business intelligence applications.




