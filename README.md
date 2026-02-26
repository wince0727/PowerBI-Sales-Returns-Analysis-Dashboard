# Power BI Sales & Returns Analysis Dashboard

## Project Overview
This project is a multi-page **Power BI dashboard** built to analyze **sales performance, customer behavior, returns impact, profitability, and regional trends** using interactive visuals and slicers.

The dashboard was developed as per a given requirements document and follows best practices in data modeling and DAX.


## Tools & Technologies
- Power BI Desktop
- DAX (Data Analysis Expressions)
- CSV Dataset
- GitHub

## Dataset
- **Project_2_Data.csv**
- Tables used:
  - Sales
  - Returns
  - People


## Data Modeling
- Sales connected with People using Region
- Sales connected with Returns using Order ID
- Proper cardinality and single-direction relationships applied


## Dashboard Pages

### Report 1: Sales Overview
**Features:**
- KPI Cards: Total Sales, Total Profit, Quantity, Orders
- Sales by Manager (Pie & Bar Charts)
- Category-wise Sales (Waterfall)
- Interactive slicers

## Screenshot:
![Sales Overview](https://github.com/wince0727/PowerBI-Sales-Returns-Analysis-Dashboard/blob/main/ScreenShorts/Report%20p1.png)


### Report 2: Customer & Sales Analysis
**Features:**
- Top 5 Customers Matrix
- Positive Sales by Manager
- Top 5 States by Sales & Profit
- KPI Cards & slicers

## Screenshot:
![Customer Analysis](https://github.com/wince0727/PowerBI-Sales-Returns-Analysis-Dashboard/blob/main/ScreenShorts/Report%20p2.png)


### Report 3: Time & Regional Analysis
**Features:**
- Monthly Profit Trend
- Weekly Sales Trend
- Category-wise Sales (Ribbon Chart)
- Sales vs Profit by City (Scatter)
- Loss-making Sub-Categories (Tree Map)
- Quantity Sold by City (Map)

## Screenshot:
![Time & Regional Analysis](https://github.com/wince0727/PowerBI-Sales-Returns-Analysis-Dashboard/blob/main/ScreenShorts/Report%20p3.png)


### Report 4: Returns Analysis
**Features:**
- Total Orders, Returned Orders, Return Rate
- Returned Orders by Region
- Sales vs Profit (Returned Orders Only)
- Filters for date, category, region, city

## Screenshot:
![Returns Analysis](https://github.com/wince0727/PowerBI-Sales-Returns-Analysis-Dashboard/blob/main/ScreenShorts/Report%20p4.png)


## Key DAX Measures Used
```DAX
Total Sales = SUM(Sales[Sales])

Total Profit = SUM(Sales[Profit])

Total Orders = DISTINCTCOUNT(Sales[Order ID])

Returned Orders = DISTINCTCOUNT(Returns[Order ID])

Return Rate % = DIVIDE([Returned Orders], [Total Orders], 0)
