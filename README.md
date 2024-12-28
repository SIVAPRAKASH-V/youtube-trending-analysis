# YouTube Trending Data Archiving and Purging Pipeline

## Project Overview

This project automates the ingestion, filtration, archiving, and analysis of YouTube trending video data using Azure tools. It leverages the **"YouTube Trending Video Dataset"** from Kaggle (updated daily) to derive actionable insights on video engagement metrics and trends. The solution includes a scalable and automated data management pipeline with seamless integration of Azure tools for advanced analytics.

### Key Features:
- Scalable and automated data management.
- Advanced data filtration and routing.
- Comprehensive analytics and visualization using Azure Databricks.

## Solution Architecture

![image](https://github.com/user-attachments/assets/17ff8d86-18a6-413f-9f8e-57f403464a51)


### 1. Data Ingestion:
The YouTube Trending Video dataset is ingested into **Azure Data Lake Storage Gen2 (Bronze Layer)** via **Azure Data Factory (ADF)**.

### 2. Data Filtration:
Three filtration criteria are applied to the data:
- Videos with views > 378,000.
- Videos that trended within 3 days.
- Videos with a like-to-dislike ratio > 0.04129.

### 3. Data Routing:
- **Compliant Data**: Moved to the Archive Container in the **Gold Layer** for analysis.
- **Non-compliant Data**: Moved to the Purging Container for deletion or further analysis.

### 4. Data Analysis and Visualization:
Compliant data from the Archive Container is analyzed in **Azure Databricks**, enabling advanced visualization and insights on:
- Engagement metrics like views, likes, and comments.
- Trends in video categories.
- Regional audience preferences.

## Tools and Requirements

### Azure Data Factory (ADF):
- Automates data movement and transformation via pipelines.

### Azure Databricks:
- Cloud-based analytics platform for processing large datasets and running machine learning models.
- Transforms and analyzes data stored in Azure Data Lake for efficient insight generation.

### Azure Data Lake Storage:
- Scalable repository for raw and processed data.
- Stores ingested data and supports Databricks processing for analysis.

### Azure Blob Storage:
- Scalable, cloud-based object storage solution for storing unstructured data such as text or binary files.

## Workflow Summary

1. **Ingest Data**: Use ADF to load the YouTube Trending Video dataset into Azure Data Lake (Bronze Layer).
2. **Filter Data**: Apply filtration criteria to segment data into compliant and non-compliant categories.
3. **Route Data**: Move compliant data to the Archive Container (Gold Layer) and non-compliant data to the Purging Container.
4. **Analyze Data**: Use Azure Databricks to analyze archived data and generate insights on video trends and engagement metrics.


## Insights and Visualization
- Analyze trends in video categories.
- Understand audience preferences by region.
- Evaluate engagement metrics such as views, likes, and comments.

## Sample output
Total Views per category
![image](https://github.com/user-attachments/assets/d41e832c-c401-4d4a-8ff5-a1f6aded4c77)


---

### How to Use
1. Clone the repository.
2. Set up Azure resources (Data Factory, Databricks, Data Lake, Blob Storage).
3. Configure the pipeline and run it to ingest and process the dataset.
4. Analyze archived data using Databricks notebooks.



---

<p>For detailed instructions and troubleshooting, please comment or contact the author.</p>
<p>Give Credits to the author</p>
<p>If you like this project give stars.</p>

### Thank you

# **Author**: _Sivaprakash V_
