# AdventureWorks Azure Project

## AdventureWorks Azure Project: Medallion Architecture Data Engineering on Azure

### Overview

This project implements a complete medallion architecture using AdventureWorks data on the Microsoft Azure platform. The solution demonstrates how to ingest, transform, visualize, and model enterprise data at scale using **Azure Data Factory**, **Azure Data Lake Storage Gen2**, **Azure Databricks**, and **Azure Synapse Analytics**.

***

### 🏗️ Project Architecture

| Layer   | Technology                | Description                                                                                  |
|---------|---------------------------|----------------------------------------------------------------------------------------------|
| Bronze  | Azure Data Factory, ADLS Gen2 | Raw AdventureWorks data loaded from GitHub into Azure Data Lake Gen2 (Bronze container). |
| Silver  | Azure Databricks, ADLS Gen2   | Cleansing, transformation, and data visualization using Databricks; output to Silver container in ADLS Gen2. |
| Gold    | Azure Synapse Analytics, ADLS Gen2 | Synapse serverless SQL reads from ADLS Silver via views and external tables; final curated analytics datasets loaded to Gold container. |

***

### 🔄 Data Flow

- **Bronze Layer**:  
  - Azure Data Factory pipelines extract raw data available on GitHub.
  - Data is loaded into the Bronze container in Azure Data Lake Gen2 for persistent, scalable raw storage.

- **Silver Layer**:  
  - Azure Databricks notebooks process and transform the raw data from the Bronze container.
  - Data cleansing, enrichment, and visualization performed in Databricks.
  - Transformed data is saved to the Silver container in ADLS Gen2.

- **Gold Layer**:  
  - Azure Synapse Analytics (serverless SQL) creates views and external tables sourcing from the Silver container.
  - Final, curated tables are generated and exported to the Gold container in ADLS Gen2 for BI and advanced analytics.

***

### 📂 Repository Structure

- `/bronze`  
  Data Factory pipeline configs, dataset definitions, and integration runtime setup for raw data ingestion.
- `/silver`  
  Databricks notebooks/scripts for transformation and visualization, plus configs for output to Silver container.
- `/gold`  
  Synapse Analytics SQL scripts, view definitions, and external table creation logic, as well as instructions for exporting to the Gold container.

***

### 🦾 Key Technologies & Skills Demonstrated

- **Azure Data Factory:** Automated data orchestration and secure data movement from GitHub to Azure.
- **Azure Data Lake Storage Gen2:** Scalable, cost-effective data lake for multi-layer architecture.
- **Azure Databricks:** Distributed data processing, Spark-based transformation, and visualization of business datasets.
- **Azure Synapse Analytics (serverless SQL):** On-demand data modeling, virtualized views, and external table management for reporting and analytics.

***

### 📈 Business Value

- **Standardized Data Foundation:** Enables robust, scalable processing for business analytics.
- **Curated Analytical Data:** Multi-layer pipeline ensures clean, enriched, and insight-ready datasets at each stage.
- **Cloud-Native Flexibility:** Easily adapts to other enterprise datasets and business scenarios.


***
