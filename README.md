# Sales-Sparta: End-to-End Sales Data Pipeline

**Sales-Sparta Ltd.** wants to build a scalable data pipeline that enables real-time visibility into sales performance, customer behavior, and brand performance. This solution is designed to serve a growing sales team with a simple, effective, and modular infrastructure that can evolve as the business scales.

## Project Overview

This project demonstrates how raw sales data can be collected, stored, transformed, and visualized to enable data-driven decision-making. The pipeline connects Salesforce (CRM data source), Snowflake (data warehouse), Airbyte (ETL/ELT ingestion), and Tableau (BI & dashboarding).

## Tools and Technologies

| Component      | Technology | Purpose |
|----------------|------------|---------|
| CRM            | Salesforce | Capture and manage customer/sales data |
| Data Warehouse | Snowflake  | Store and query transformed data |
| ETL Pipeline   | Airbyte    | Ingest and move data from source to warehouse |
| BI Tool        | Tableau    | Visualize metrics and generate insights |

## Data Pipeline Lifecycle

1. **Data Generation**  
   - Sales reps manually enter data into Salesforce.
   - Previously done via Excel sheets, which posed risks (e.g., data loss, low accuracy).

2. **Data Storage**  
   - Raw data is stored securely in Snowflake cloud data warehouse.
   - Staging and Production environments used for clean separation of raw vs. transformed data.

3. **Data Ingestion & Transformation**  
   - Airbyte handles batch ingestion from Salesforce into Snowflake.
   - Staging tables are transformed (null handling, column standardization) before promotion to production.

4. **Data Serving & Visualization**  
   - Transformed production tables are connected to Tableau.
   - Dashboards use Tableau Extracts for better performance.

## Key Business Insights

- **Total Orders**: 250  
- **Average Order Value**: $522  
- **Top Sales Months**: August 2022, September 2023  
- **High-Performing States**: California & Texas  
- **Top Brands**: Luxelife and Ecoera  
- **Profit**: Over $28,000 (consistently positive margins)

## Tableau Dashboard

Explore the live dashboard here:  
🔗 [View on Tableau Public](https://public.tableau.com/app/profile/santosh.govardhan.kyathsandra.badarinath/viz/Sales-spartametrics/Dashboard1)

## Challenges Faced

- **Data Quality**: Null values in CSVs required robust cleaning and validation.
- **Data Modeling**: Inconsistent dimension keys violated primary key constraints.
- **Transformation Logic**: Standardization and feature engineering in staging layer.

## Lessons Learned

- Importance of staging environments for safe experimentation.
- The trade-off between real-time vs. batch ingestion.
- Effective visualization depends on clean and well-joined data.


