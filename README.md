# Mobile-sales-analysis
Data analysis project exploring mobile sales trends, customer behaviour, and revenue insights
---
## Table of Contents
- Project Overview
- Tools Used
- Data Source
- Key Insights
- Visualization
- SQL Queries
- Author
---
## Project Overview
_This project focuses on analyzing mobile sales performance across various dimensions, including revenue, units sold, customer gender, payment methods, monthly trends, and geographical locations. The aim of the analysis is to uncover sales patterns, customer behaviors, and revenue distribution in order to support data-driven decision-making and business growth strategies._
---
## Tools Used
- Excel / Power Query - Data cleaning and Pivot Table
- Power BI – Visualization, and Dashboard
- SQL - Data Extraction and Queries
- Github - Portfolio and Project presentation
---
## Data Source
- Source: www.kaggle.com
---
## Key Insights
This dashboard analyzes ₦40.22M in mobile sales across gender, payment methods, months, and locations.
- Revenue: ₦40.22M with 50,074 units sold.
- Top Payment Method: Credit Card (28%).
- Customer Gender: Female customers slightly lead in purchases.
- Monthly Trend: Highest sales recorded in January.
- Location: Lake Amanda generated the most revenue.
---
## Table overlay
| TransactionID                          | Date       | MobileModel | Brand            | Price   | UnitsSold | TotalRevenue | CustomerAge | CustomerGender | Location      | PaymentMethod |
|----------------------------------------|------------|-------------|------------------|---------|-----------|--------------|-------------|----------------|---------------|---------------|
| 79397f68-61ed-4ea8-bcb2-f918d4e6c05b   | 01/06/2024 | direction   | Green Inc        | 1196.95 | 85        | 28002.8      | 32          | Female         | Port Erik     | Online |
| 4f87d114-f522-4ead-93e3-f336402df6aa   | 04/05/2024 | right       | Thomas-Thompson  | 1010.34 | 64        | 2378.82      | 55          | Female         | East Linda    | Credit Card |
| 6750b7d6-dcc5-48c5-a76a-b6fc9d540fe1   | 02/13/2024 | summer      | Sanchez-Williams | 400.8   | 95        | 31322.56     | 57          | Male           | East Angelic  | Online |

## Visualization
### Pivot Table


<img width="964" height="435" alt="pivot table mobile sales" src="https://github.com/user-attachments/assets/8eb3fefb-3eee-49c4-bb79-3f83f8c777db" />

---

### Dashboard

<img width="891" height="495" alt="MOBILE DATASET" src="https://github.com/user-attachments/assets/bc75140b-6181-4eb8-b25e-6bf34be722b4" />

## Query Language (SQL)

```SQL
SELECT * FROM dbo.mobile_sales;
---Categorize the price into Gold,Silver AND ---
SELECT * FROM dbo.mobile_sales SELECT price,
 CASE
  WHEN price < 500 THEN 'gold'
  WHEN price BETWEEN 500 AND 999 THEN 'diamond'
  WHEN price >= 1000 THEN 'silver'
END AS category
FROM dbo.mobile_sales;

```
