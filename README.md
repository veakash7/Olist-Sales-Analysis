# Olist-Sales-Analysis

[View the Interactive Dashboard Here](https://app.powerbi.com/groups/me/reports/be7fe99f-d220-4e1b-b3ed-ee0e44023daa/9ab8acd6320c1425dc20?experience=power-bi)

### 1. Problem Statement

This project analyzes the Olist e-commerce dataset, which contains data on 113,000 orders from a Brazilian marketplace. The goal was to develop a comprehensive Power BI dashboard to identify key drivers of revenue, understand customer behavior, and uncover actionable insights to improve sales performance.

### 2. My 6-Step Process

I followed a structured data analysis process from end-to-end:

**1. Data Sourcing:**
Downloaded the 8 raw CSV files from the public [Olist E-Commerce Dataset on Kaggle](https*://www.kaggle.com/datasets/olistbr/brazilian-ecommerce).

**2. Data Cleaning & Transformation (Python):**
Used the **Pandas** library in Python to pre-process and clean the data.
* Merged 8 separate CSVs into a cohesive dataset.
* Handled missing values: Imputed numerical nulls (e.g., `payment_value`) with the median `(fillna())`.
* Standardized data formats: Converted datetime columns from `object` to `datetime` using `pd.to_datetime`.
* Exported the cleaned data and loaded into Power BI.

**3. Data Modeling (Power BI):**
Engineered a robust **star-schema** in the Power BI model view.
* Established one-to-many, single-direction relationships from dimension tables (e.g., `dim_Customers`, `dim_Products`, `dim_Date`) to the central `fct_Orders` table.
* This model optimizes query performance and ensures accurate, non-ambiguous analysis.

**4. DAX Measures:**
Authored custom **DAX** measures to calculate key business metrics, including:
* Total Revenue
* Average Order Value (AOV)
* Total Customers
* Average Review Score

**5. Data Visualization:**
Designed an interactive 3-page report in Power BI, with each page serving a specific analytical purpose:
* **Sales Analysis:** An executive overview of KPIs, revenue trends, and geographic performance.
* **Order & Payments:** A deep dive into payment methods, installment plans, and order fulfillment status.
* **Product & Reviews:** An analysis of top-performing categories, AOV, and the correlation between review scores and sales.

**6. Insights & Recommendations:**
Insight 1: Strong Core Performance The business is robust, with $15.84M in revenue generated from 113K orders across 74 product categories. The customer experience is generally positive, with a high average review score of 4.09 out of 5.

Insight 2: Geographic Concentration The state of São Paulo (SP) is the undisputed core of the business, accounting for 42K orders (37% of the total). The city of sao paulo alone generated $3.18M in revenue, representing over 20% of all company revenue.
Recommendation: Focus marketing and logistics efforts in this key region. Explore targeted campaigns to expand in the next largest markets, Rio de Janeiro (12K orders) and MG (12K orders).

Insight 3: Customer Payment Preferences Credit cards are the dominant payment method, accounting for 78.34% ($12.54M) of all sales value.
Recommendation: Ensure the credit card payment process is seamless. Since Boleto (17.92%) is still a significant secondary option, this service must be maintained and reliable. The popularity of 1-installment payments ($5.91M) suggests customers prefer to pay upfront.

Insight 4: High Fulfillment Success The logistics operation is highly effective, with 96.48K orders (over 85%) successfully delivered. This high success rate builds customer trust and authenticity.

Insight 5: Correlation Between Reviews & Sales The Average review_score by Month chart shows significant dips below 4.0 in February (3.87), March (3.84), and November (3.91). These dips, especially in March and November, correlate with dips in the Total Revenue by Month chart.
Recommendation: Investigate the root cause of poor reviews in these specific months (e.t., seasonal shipping delays, product stock issues) as improving customer satisfaction appears directly linked to increasing revenue.

Insight 6: High-Value vs. High-Volume Products There is a clear distinction between top-performing categories:
High Revenue: health_beauty generates the most total revenue ($1.44M).
High Value: computers has the highest Average Order Value ($1147) by a large margin (2x the next category).
Recommendation: This means that while health_beauty drives a high volume of sales, computers brings in the highest-value customers. Marketing strategies should be tailored for both: a volume-based strategy for health_beauty and a high-touch, value-focused strategy for computers.

### 3. Tools Used
* **Python:** (Pandas) for data cleaning and transformation.
* **Power BI:** (Power Query, DAX, Data Modeling) for analysis and visualization.
