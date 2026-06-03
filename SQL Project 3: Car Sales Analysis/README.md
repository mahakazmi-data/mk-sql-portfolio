# Maha B. Kazmi - SQL Portfolio

I am a data-driven professional with experience in Marketing, Communications, and Data Analytics. This portfolio showcases SQL projects focused on business insights and data storytelling.

## Project Index
- 1. Global Marketing Campaign Analysis
- 2. Customer Segmentation Project
- 3. Car Sales Performance & Revenue Trends Analysis <- You are here

## Skills
- SQL (Joins, Aggregations)
- Data Analysis
- Marketing Analytics

## Tools Used
- SQLite / DB Browser
- SQL
- GitHub
- Kaggle Dataset

--- 

## Which months had the highest sales?

SQL Query: 
```sql
SELECT 
    substr(Date, 1, 7) AS month,
    SUM("Sale Price") AS total_sales
FROM car_sales_data
GROUP BY month
ORDER BY total_sales DESC;
```
![Monthly Car Sales](Monthly_Sales.png)

A: The top 3 months with the highest sales were December 2022, October 2022, and August 2022. 


---


## Are there seasonal spikes?

SQL Query: 
```sql
SELECT
  strftime('%Y-%m', Date) AS month,
  COUNT(*) AS total_sales
FROM car_sales_data
GROUP BY strftime('%Y-%m', Date)
ORDER BY month;
```
![Spikes in sales](Spikes_in_sales.png)

A: Based on this, we can tell that baseline demands are very stable. However, there is a prominent dip in June 2023 when sales decrease by 97% at 6,839 sales that month. In terms of seasonal spikes, there are no true seasonal spikes but there are mild end-of-quarter / year-end uplifts.

----

##  Which car make generates the most revenue?

SQL Query: 
```sql
SELECT
  "Car Make",
  Sum ("Sale Price") AS total_revenue
FROM car_sales_data
GROUP BY "Car Make"
ORDER BY total_revenue DESC;
```

![Car make revenue](Car_make_revenue.png)

A: Here, we can identify Honda as the car brand generating the most revenue.
