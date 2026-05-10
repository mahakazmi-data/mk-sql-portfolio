# Maha Kazmi - SQL Portfolio

I am a data-driven marketing professional with experience in communications and analytics. This portfolio showcases SQL projects focused on business insights and data storytelling.

## Projects
- Marketing Campaign Analysis
- Sales Performance Dashboard (coming soon)

## Skills
- SQL (Joins, Aggregations, CTEs, Window Functions)
- Data Analysis
- Marketing Analytics
-- Calculate ROI by campaign type
SELECT 
  campaign_type,
  SUM(revenue) - SUM(ad_spend) AS ROI
FROM Campaigns
GROUP BY campaign_type
ORDER BY ROI DESC;
