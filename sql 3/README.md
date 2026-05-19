# Maha B. Kazmi - SQL Portfolio

I am a data-driven professional with experience in Marketing, Communications, and Data Analytics. This portfolio showcases SQL projects focused on business insights and data storytelling.

## Project Index
- 1. Global Marketing Campaign Analysis
- 2. Customer Segmentation Project
- 3. Car Sales Performance & Revenue Trends Analysis

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

## Which month had the highest sales?

SQL Query: 
```sql
SELECT 
  campaign_type, 
  (SUM(revenue) - SUM(ad_spend) )/ SUM(ad_spend) AS ROI
FROM global_ads_performance_dataset 
GROUP BY campaign_type 
ORDER BY ROI DESC;
```
