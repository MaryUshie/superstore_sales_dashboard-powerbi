# Superstore Sales Dashboard (Power BI)

An interactive Power BI report built on the Superstore sales dataset. It covers sales performance by segment, category, city and customer, plus time intelligence (MTD, YTD and year-over-year growth) using DAX and a dedicated Date table.

## Tools used
- Power BI Desktop
- DAX (measures and time intelligence)
- Data modelling (Date table, one-to-many relationships)

## Report pages

### Page 1: Sales Overview
KPI cards for order count and total sales, sales by customer segment, and orders by ship mode.

![Page 1](Screenshot%202026-10-20%20131102.png)

### Page 2: Sales Trends
Sales by category, Sales MTD, Sales YTD and monthly sales growth %.

![Page 2](Screenshot%202026-10-20%20131307.png)

### Page 3: Top Cities and Customers
Top 10 cities ranked by sales and top 10 customers by sales.

![Page 3](Screenshot%202026-10-20%20131344.png)

## Key DAX measures

Sales MTD = TOTALMTD(SUM(SUPERSTORE[Sales]), DateTable[Date])
Sales YTD = TOTALYTD(SUM(SUPERSTORE[Sales]), DateTable[Date])
Sales PY = CALCULATE(SUM(SUPERSTORE[Sales]), SAMEPERIODLASTYEAR(DateTable[Date]))
Sales Growth % = DIVIDE(SUM(SUPERSTORE[Sales]) - [Sales PY], [Sales PY])
Sales Rank by City = RANKX(ALL(SUPERSTORE[City]), [Total sales])


## How to open the report
1. Download project _v2.pbix from this repository.
2. Open it in Power BI Desktop (Windows).
3. Click on any chart element to see the other visuals filter.

## What I learned
- Building a Date table and marking it as the date table
- Writing time-intelligence measures in DAX
- Designing a multi-page report with consistent layout
# Superstore Sales Dashboard (Power BI)

An interactive Power BI report built on the Superstore sales dataset. It covers sales performance by segment, category, city and customer, plus time intelligence (MTD, YTD and year-over-year growth) using DAX and a dedicated Date table.

## Tools used
- Power BI Desktop
- DAX (measures and time intelligence)
- Data modelling (Date table, one-to-many relationships)

## Report pages

### Page 1: Sales Overview
KPI cards for order count and total sales, sales by customer segment, and orders by ship mode.

![Page 1](Screenshot%202026-10-20%20131102.png)

### Page 2: Sales Trends
Sales by category, Sales MTD, Sales YTD and monthly sales growth %.

![Page 2](Screenshot%202026-10-20%20131307.png)

### Page 3: Top Cities and Customers
Top 10 cities ranked by sales and top 10 customers by sales.

![Page 3](Screenshot%202026-10-20%20131344.png)

## Key DAX measures

Sales MTD = TOTALMTD(SUM(SUPERSTORE[Sales]), DateTable[Date])
Sales YTD = TOTALYTD(SUM(SUPERSTORE[Sales]), DateTable[Date])
Sales PY = CALCULATE(SUM(SUPERSTORE[Sales]), SAMEPERIODLASTYEAR(DateTable[Date]))
Sales Growth % = DIVIDE(SUM(SUPERSTORE[Sales]) - [Sales PY], [Sales PY])
Sales Rank by City = RANKX(ALL(SUPERSTORE[City]), [Total sales])


## How to open the report
1. Download project _v2.pbix from this repository.
2. Open it in Power BI Desktop (Windows).
3. Click on any chart element to see the other visuals filter.

## What I learned
- Building a Date table and marking it as the date table
- Writing time-intelligence measures in DAX
- Designing a multi-page report with consistent layout
