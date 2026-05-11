# Maha B. Kazmi - SQL Portfolio

I am a data-driven professional with experience in Marketing, Communications, and Data Analytics. This portfolio showcases SQL projects focused on business insights and data storytelling.

## Project Index
- 1. Global Marketing Campaign Analysis
- 2. Comming Soon
- 3. Comming Soon

## Skills
- SQL (Joins, Aggregations)
- Data Analysis
- Marketing Analytics

## Global Marketing Campaign Analysis

Situation: Soothe, a hand lotion company, has data on its marketing stats. They want to determine the most valuable use of their Ad Budget based on previous performance on various platforms and campaigns. They want answers to the following to determine this: 

- 1. Which campaign has the highest ROI?
- 2. Which platform performs best?
- 3. Which campaign should we invest more in?

Q1: Which campaign has the highest ROI?
-- Objective: Identify which campaign type generates the highest ROI

SQL Query: 
```sql
SELECT 
  campaign_type, 
  (SUM(revenue) - SUM(ad_spend) )/ SUM(ad_spend) AS ROI
FROM global_ads_performance_dataset 
GROUP BY campaign_type 
ORDER BY ROI DESC;
```
### 📊 Results

| Campaign | ROI |
|---|---|
| Search | 4.30% |
| Display | 3.83% |
| Video | 3.77% |
| Shopping | 3.58% |

-- Calculate ROI by advertising platform

![Campaign ROI Results](campaign_roi_results.png)

SELECT 
  platform,
  (SUM(revenue) - SUM(ad_spend)) * 1.0 / SUM(ad_spend) AS ROI
FROM global_ads_performance_dataset
GROUP BY platform
ORDER BY ROI DESC;

### 📊 Results

| Platform | ROI |
|---|---|
| Tik Tok Ads | 6.62% |
| Meta Ads | 4.66% |
| Google Ads | 2.47% |

![Platform ROI Results](platform_roi_results.png)

-- Calculate which campaign we should invest more in based on ROI, Revenue, and Ad Spend.

SELECT 
  campaign_type, 
  (SUM(revenue) - SUM(ad_spend) ) *1.0 / SUM(ad_spend) AS ROI,
  SUM (revenue) AS total_revenue,
  SUM (ad_spend) AS total_ad_spend
FROM global_ads_performance_dataset 
GROUP  BY campaign_type 
ORDER  BY ROI DESC;

### 📊 Results

| Campaign | ROI | Revenue | Ad Spend| 
|---|---|---|---|
| Search | 4.30% |15218470.85 | 2868006.85 |
| Display | 3.83% |12798903.17 | 2644735.12 |
| Video | 3.77% |13341261.19 | 2796458.48 |
| Shopping | 3.58% |12824695.6 |2799548.64 |

![Campaign to Invest in More Results](ROI_Revenue_Spend.png)
