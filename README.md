# Pharmaceutical Sales Company Analysis


This data analysis project provides a comprehensive examination of raw sales data from `Datamatrix-ml Pharmaceuticals`, a leading global pharmaceutical manufacturer. The goal is to extract meaningful insights and present them through a series of interactive Power BI dashboards. The analysis covers overall company performance, distributor and customer metrics, and sales team effectiveness.


## Table of Contents

  - [Project Objective](https://www.google.com/search?q=%23project-objective)
  - [Tools Used](https://www.google.com/search?q=%23tools-used)
  - [Solution Approach](https://www.google.com/search?q=%23solution-approach)
  - [Data Model](https://www.google.com/search?q=%23data-model)
  - [Dashboard Overviews and Key Insights](https://www.google.com/search?q=%23dashboard-overviews-and-key-insights)
      - [Executive Summary](https://www.google.com/search?q=%231-executive-summary)
      - [Distributor & Customer Analysis](https://www.google.com/search?q=%232-distributor--customer-analysis)
      - [Sales Team Performance](https://www.google.com/search?q=%233-sales-team-performance)
 

## Project Objective

The primary objective is to analyze the company's sales data for the German and Poland markets to provide actionable insights for different stakeholders within the organization. The requirements were divided based on the target audience:

|Requirement ID|Audience|Requirement Description|
|:---|:---|:---|
|DM-DA01-REQ-1|Executive Committee|Provide a high-level overview of the company’s sales performance by year, month, customer city, and channel/sub-channel. Highlight top-performing drug classes, specific drugs, and customer cities.|
|DM-DA01-REQ-2|Sales Manager/Sales Rep|Deliver a detailed breakdown of sales by distributor and product, identify top customers and cities, and show sales splits by various channels.|
|DM-DA01-REQ-3|Head of Sales|Create a comprehensive report on sales team performance, detailing sales by team for each product and product class. Identify top-performing managers and reps, and allow for data filtering by year and month.|

## Tools Used

  * **Power BI Desktop**: For data modeling, analysis, and report creation.
  * **Power Query Editor**: For data cleaning, transformation, and preparation.
  * **Python (pandas)**: Used for initial Exploratory Data Analysis (EDA) to check data quality, handle missing values, and understand data distributions.

## Solution Approach

1.  **Data Exploration (EDA)**: The raw `.csv` dataset was initially inspected using the pandas library in Python to identify and handle any inconsistencies, missing values, or outliers.
2.  **Data Cleaning and Transformation**: In Power Query Editor, column headers and data types were corrected to ensure data integrity before modeling.
3.  **Data Modeling**: A star schema data model was built in Power BI to optimize performance and usability. The initial single-table dataset was split into dimension and fact tables.
4.  **Report & Dashboard Creation**: Three interactive, multi-page reports were developed in Power BI to address the specific requirements of the executive team, sales managers, and the head of sales.

## Data Model

To facilitate efficient analysis, the data was modeled into a **star schema**. This structure separates the quantitative sales data (facts) from the descriptive, categorical data (dimensions). This model improves query performance and simplifies the creation of complex analytics.

The model consists of one central `FACT-sales` table connected to nine dimension tables:

  * **Fact Table**: `FACT-sales` (contains metrics like Price, Quantity, Sales)
  * **Dimension Tables**: `DIM-channel`, `DIM-subchannel`, `DIM-country`, `DIM-city`, `DIM-distributor`, `DIM-customer`, `DIM-month`, `DIM-product`, `DIM-sales-rep`, and `DIM-sales-team`.

![image](https://github.com/user-attachments/assets/31d9c5ad-ceef-4022-9b43-2b52a5a78b1e)


## Dashboard Overviews and Key Insights

Three distinct dashboards were created to cater to the needs of different stakeholders.

### 1\. Executive Summary

This dashboard provides a high-level, at-a-glance view of the overall business performance.

![image](https://github.com/user-attachments/assets/3febf60b-6dc8-465f-b54c-f0bd1d351127)



**Key Insights:**

  * **Total Sales**: The company achieved total sales of **$11.80 billion**.
  * **Top Performers**:
      * **Top Product Class**: `Analgesics` is the highest-grossing category with over **$2.37 billion** in sales.
      * **Top Product**: `Ionclotide` stands out as the top-selling individual product, generating **$169.08 million**.
      * **Top City**: `Butzbach` is the most profitable city with sales of **$93.56 million**.
  * **Sales Trend**: The "Sales by Year" chart indicates a declining trend in sales, which requires further investigation.
  * **Geographic Distribution**: The "Sales by Top Cities" map visualizes the key revenue-generating locations across Europe.

### 2\. Distributor & Customer Analysis

This report offers a more granular view, focusing on the performance of distribution partners and key customers.

![image](https://github.com/user-attachments/assets/0751ca3b-569b-4355-bab0-a44d51216241)


**Key Insights:**

  * **Top Distributor**: `Gerlach LLC` is the leading distributor, responsible for **$3.50 billion** in sales. `Koss` follows with **$3.11 billion**.
  * **Top Customer**: `Mraz-Kutch Pha...` is the largest customer, with purchases totaling **$94 million**.
  * **Sales Channels**:
      * `Pharmacy` and `Hospital` are the two primary sales channels.
      * Within sub-channels, sales are diversified across `Private`, `Retail`, `Institution`, and `Government` sectors.
  * **Product-Level Analysis**: The matrix visual allows for a drill-down into sales by each distributor for specific products. For instance, `Gerlach LLC`'s sales of `Antiseptics` alone amounted to **$688.5 million**.

### 3\. Sales Team Performance

This dashboard is designed for the Head of Sales to monitor and analyze the performance of the sales teams and individual representatives.

![image](https://github.com/user-attachments/assets/5cac7e41-8409-4c1d-954d-008babeb0bc5)


**Key Insights:**

  * **Top Sales Managers**:
      * `Tracy Banks`'s team (Bravo) generated **$698.09 million** in sales.
      * `Britanny Bold`'s team (Delta) achieved **$584.00 million** in sales.
  * **Top Sales Representatives**:
      * `Mary Gerrard` (Team Delta) is the top-performing rep with sales of **$256.80 million**.
      * `Anne Wu` (Team Delta) follows with **$240.19 million**.
  * **Performance Breakdown**: The dashboard provides detailed matrices showing sales contributions by each team (`Alfa`, `Bravo`, `Charlie`, `Delta`) for different product classes and individual products.
  * **Interactive Filtering**: Slicers for `Year` and `Month` allow for dynamic filtering to analyze performance over specific time periods. For example, in `2017`, Team Delta was the top performer for `Mood Stabilizers` with sales of **$186.57 million**.

