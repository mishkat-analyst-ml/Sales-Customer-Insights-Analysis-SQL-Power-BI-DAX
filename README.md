# Sales-Customer-Insights-Analysis-SQL-Power-BI-DAX
End-to-End Business Intelligence Project | SQL • Power BI • DAX

Transforming raw customer transaction data into actionable business insights through SQL analysis, interactive Power BI dashboards, and KPI-driven decision making.

# 📌  Project Overview

This project demonstrates a complete Business Intelligence (BI) workflow using MySQL, Power BI, and DAX. The objective was to analyze customer purchasing behavior, sales performance, revenue distribution, customer lifetime value, and churn indicators to help business stakeholders make data-driven decisions.

The dashboard provides executives with a single view of customer and sales performance by tracking KPIs, regional performance, purchasing patterns, seasonal trends, and customer preferences.

# 🎯 Business Problem

Retail businesses often struggle to answer questions such as:

Which regions generate the highest revenue?
Which product categories are purchased most frequently?
When do customers usually make purchases?
What is the average customer lifetime value?
How frequently do customers purchase?
Which customers are more likely to churn?
Are there seasonal trends affecting sales?

This dashboard answers these questions using interactive visualizations and SQL-driven analysis.

# 🛠 Tech Stack
Technology	Purpose
MySQL	Data Extraction & Business Queries
Power BI	Dashboard Development
DAX	KPI Measures & Calculations
Power Query	Data Cleaning & Transformation
Excel/CSV	Source Dataset
# 📂 Project Workflow
CSV Dataset
      │
      ▼
Data Cleaning
      │
      ▼
Import into MySQL
      │
      ▼
Business SQL Analysis
      │
      ▼
Power BI Data Model
      │
      ▼
DAX Measures
      │
      ▼
Interactive Dashboard
      │
      ▼
Business Insights
# 📊 Dashboard KPIs

The dashboard tracks four executive-level KPIs:

KPI	Value
Average Purchase Frequency	9.96
Average Customer Lifetime Value	5.03K
Total Revenue	1M
Total Customers	10K

These KPIs provide an instant overview of overall business performance.

# 🔍 SQL Business Analysis Performed
1️⃣ Revenue by Region
SELECT Region,
SUM(Average_Order_Value) AS TotalSales
FROM sales_and_customer_insights
GROUP BY Region;
Result
Region	Revenue
South America	278,749
Europe	277,476
Asia	272,449
North America	271,386
Business Insight
Revenue is distributed fairly evenly across all regions.
South America slightly outperforms the other markets.
No single region dominates sales, indicating a diversified customer base.
# 2️⃣ Most Purchased Product Categories
SELECT Most_Frequent_Category,
COUNT(*)
FROM sales_and_customer_insights
GROUP BY Most_Frequent_Category;
Result
Category	Customers
Electronics	2,567
Clothing	2,510
Home	2,476
Sports	2,447
Business Insight
Electronics is the highest-performing category.
Customer demand is balanced across all categories.
Product diversification appears healthy.
# 3️⃣ Preferred Purchase Time
SELECT Preferred_Purchase_Times,
COUNT(*)
FROM sales_and_customer_insights
GROUP BY Preferred_Purchase_Times;
Result
Time	Customers
Evening	3,433
Afternoon	3,354
Morning	3,213
Business Insight
Evening has the highest shopping activity.
Marketing campaigns should prioritize evening hours.
Promotional emails and notifications can be scheduled before peak shopping time.
# 4️⃣ Monthly Revenue Trend
SELECT MONTH(Peak_Sales_Date),
SUM(Average_Order_Value)
FROM sales_and_customer_insights
GROUP BY MONTH(Peak_Sales_Date);
Business Insight
Revenue remains relatively stable throughout the year.
January and May recorded the strongest sales.
February experienced the lowest monthly revenue.
No major seasonal fluctuations were observed.
# 5️⃣ Customer Lifetime Value
SELECT AVG(Lifetime_Value)
FROM sales_and_customer_insights;
Insight

Average customer lifetime value is approximately 5.03K, indicating consistent long-term customer contribution.

# 6️⃣ Purchase Frequency
SELECT AVG(Purchase_Frequency)
FROM sales_and_customer_insights;
Insight

Customers purchase nearly 10 times on average, demonstrating strong customer engagement.

# 7️⃣ Churn Analysis
SELECT AVG(Churn_Probability)
FROM sales_and_customer_insights;
Insight

Average churn probability helps identify customer retention risks and supports proactive loyalty strategies.

# 📈 Dashboard Features

✔ Executive KPI Cards

✔ Revenue Analysis

✔ Customer Segmentation

✔ Category Distribution

✔ Seasonal Sales Analysis

✔ Monthly Revenue Trend

✔ Customer Lifetime Value

✔ Churn Monitoring

✔ Interactive Filters

Region
Season
Product Category
# 💡 Key Business Insights
South America generates the highest revenue among all regions.
Electronics is the most purchased product category.
Customers are most active during the evening.
Customer purchasing behavior remains consistent throughout the year.
Average purchase frequency (~10 purchases) indicates strong customer loyalty.
Average customer lifetime value exceeds 5K, highlighting high long-term customer value.
Revenue distribution is balanced across regions, reducing dependency on a single market.
Churn analysis enables targeted customer retention strategies.
📊 Power BI Visualizations
KPI Cards
Revenue by Region (Column Chart)
Monthly Revenue Trend (Line Chart)
Revenue by Season (Column Chart)
Product Category Distribution (Donut Chart)
Lifetime Value vs Churn (Scatter Plot)
Interactive Slicers
Dynamic Filtering
Responsive Dashboard Layout
## 🚀 Skills Demonstrated
SQL
Aggregations
GROUP BY
Filtering
Date Functions
Business Query Writing
Customer Analysis
Power BI
Dashboard Design
Interactive Reports
Data Modeling
Drill Filtering
KPI Design
DAX
SUM
AVERAGE
COUNT
Calculated Measures
Business KPIs
Business Intelligence
Customer Analytics
Sales Analytics
Revenue Analysis
Customer Segmentation
Executive Dashboarding
KPI Reporting
Data Storytelling
📁 Repository Structure
Sales-Customer-Insights-Dashboard/
│
├── Dataset/
│   └── sales_and_customer_insights.csv
│
├── SQL/
│   └── Business_Queries.sql
│
├── PowerBI/
│   └── Sales_Customer_Insights.pbix
│
├── Dashboard/
│   └── Dashboard_Screenshot.png
│
├── README.md
│
└── LICENSE


