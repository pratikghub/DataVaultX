 
## Project Type : Advanced Sales & Marketing Data Warehousing with Azure

### Author : Pratik Ganguli 


## Overview
This project focuses on designing and implementing a **sales and marketing data warehouse** for Adventure Works Cycles, utilizing **Azure Data Factory (ADF) for ETL workflows**, **Azure Data Studio for querying OLTP and OLAP databases**, and **Azure SQL Database for structured data storage**. The primary goal is to facilitate advanced **business intelligence analytics** to enhance decision-making in sales optimization, customer segmentation, discount impact analysis, and demand forecasting.

This implementation follows a **star-schema architecture**, ensuring high-performance queries and efficient data retrieval. The **ETL pipeline** automates the transformation from a **normalized OLTP database** to a **denormalized OLAP structure**, enabling more effective data aggregation, trend analysis, and reporting.

## Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Project Objectives](#project-objectives)
- [Methodology](#methodology)
- [Key Findings](#key-findings)
- [Data Warehouse Architecture](#data-warehouse-architecture)
- [ETL Workflow and Transformations](#etl-workflow-and-transformations)
- [Technology Stack](#technology-stack)
- [Usage](#usage)
- [Results](#results)
- [Business Applications](#business-applications)
- [Visualizations and Interpretations](#visualizations-and-interpretations)
- [Conclusion](#conclusion)
- [License](#license)
- [Acknowledgments](#acknowledgments)

## Dataset
The dataset consists of historical sales transactions, customer demographics, product details, and time-series data. The **OLTP database** was transformed into an **OLAP format** to facilitate structured analysis. 

### Key Data Elements:
- **Customer Data**: Customer type (Individual vs. Store), geographic segmentation, and purchase behavior.
- **Product Data**: Product categories, subcategories, and pricing.
- **Sales Transactions**: Order details, discounting effects, and revenue.
- **Time-Series Data**: Seasonal sales patterns and quarterly trends.

## Project Objectives
The primary objectives of this project include:
1. **Building an optimized data warehouse** using Azure SQL Database with a **star-schema design**.
2. **Automating ETL pipelines** using Azure Data Factory to transform normalized OLTP data into a structured OLAP model.
3. **Analyzing customer segmentation** to understand the revenue and profit contributions of different customer groups.
4. **Evaluating the impact of discounting strategies** on sales volume and profitability.
5. **Identifying seasonal trends** in sales to enhance demand forecasting and inventory planning.

## Methodology
### 1. Data Preprocessing & Extraction
- Extracted transactional data from the **OLTP database** using **Azure Data Studio**.
- Cleaned and formatted raw data to maintain consistency and remove duplicates.

### 2. Data Transformation using Azure Data Factory
- **Schema Transformation**: Converted **normalized (OLTP)** data into **denormalized (OLAP)** format.
- **Derived Columns**: Created new attributes for customer segmentation and product hierarchies.
- **Union Transformations**: Merged datasets from different sources.
- **SQL-Based Aggregations**: Computed key business metrics (profit, sales trends, and seasonal patterns).

### 3. Data Loading into Data Warehouse
- Designed and implemented a **star-schema warehouse** in **Azure SQL Database**.
- Loaded transformed data into **Fact and Dimension tables** for optimized querying.

## Key Findings
- **Stores generate higher revenue but operate at a loss**, whereas individual customers yield higher profit margins.
- **Bikes are the most profitable category**, requiring minimal discounting.
- **Seasonality significantly impacts sales**, with strong revenue peaks in certain quarters.
- **Discounting strategies must be optimized** to prevent profit erosion while driving sales.

## Data Warehouse Architecture
The **star schema** comprises the following tables:
- **FactSale**: Centralized sales transaction table storing order details, revenue, and profit margins.
- **DimCustomer**: Customer attributes (type, region, and segmentation).
- **DimProduct**: Product attributes (category, subcategory, pricing, and discount details).
- **DimDate**: Time-based attributes (year, quarter, month, week) for trend analysis.

Each **dimension table** connects to **FactSale**, ensuring structured analytics and optimized query performance.

## ETL Workflow and Transformations
### 1. Customer Dimension Transformation
- Combined **individual and store customer datasets**.
- Created **customer segmentation attributes** using derived columns.
- Standardized customer data before loading into **DimCustomer**.

### 2. Product Dimension Transformation
- Extracted **product, subcategory, and category data** from the source database.
- Performed **hierarchical joins** to create a structured product dataset.
- Mapped product attributes before loading into **DimProduct**.

### 3. Date Dimension Transformation
- Generated **date-based attributes** (Year, Quarter, Month, Week).
- Integrated transformed data into **DimDate**.

### 4. Fact Sale Table Transformation
- Aggregated **order quantity, discount values, sales revenue, and gross profit**.
- Joined transaction data with **DimCustomer, DimProduct, and DimDate**.
- Loaded cleaned data into **FactSale**.

## Technology Stack
- **Azure Data Factory**: Automated ETL workflows and schema transformations.
- **Azure Data Studio**: Connected to OLTP and OLAP databases for SQL-based analysis.
- **Azure SQL Database**: Hosted the data warehouse using a star-schema design.
- **SQL Queries**: Used for data aggregation, customer segmentation, and profitability analysis.

## Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/AdventureWorksDataWarehouse.git
   cd AdventureWorksDataWarehouse
   ```
2. Connect to the OLTP database using **Azure Data Studio**.
3. Execute **ETL pipelines** in **Azure Data Factory**.
4. Query the **Adventure Works Data Warehouse** using SQL for analysis.

## Results
- **Profitability Analysis**: Identified high-revenue but low-profit segments.
- **Seasonality Trends**: Determined demand fluctuations to improve forecasting.
- **Discount Impact Analysis**: Measured how price reductions affect profit margins.

## Business Applications
- **Pricing Optimization**: Adjust bulk pricing for store customers to prevent revenue loss.
- **Personalized Marketing Campaigns**: Use customer segmentation insights.
- **Inventory Planning**: Stock products based on seasonal demand patterns.

## Visualizations and Interpretations
### 1. Entity-Relationship Diagram (ERD)
- The **star schema ERD** visualizes relationships between **FactSale** and **Dimension tables**, ensuring efficient analytical performance.

### 2. Customer Segmentation Analysis
- **Interpretation**: Individual customers contribute lower revenue but significantly higher profits.

### 3. Seasonal Sales Trends
- **Key Insight**: Revenue peaks in specific quarters indicate demand shifts requiring adaptive inventory strategies.

### 4. Discounting Impact on Profitability
- **Business Impact**: Excessive discounts increase sales volume but lower overall profit margins.

## Conclusion
This project demonstrates the effectiveness of **data warehousing using Azure technologies**. By leveraging **Azure Data Factory for ETL automation** and **Azure Data Studio for SQL-based analysis**, businesses can optimize sales strategies and improve profitability through **structured, data-driven decision-making**.

## License
This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

## Acknowledgments
Special thanks to [Microsoft Azure](https://azure.microsoft.com/) for cloud-based data management solutions and OpenAI's ChatGPT for documentation assistance.



