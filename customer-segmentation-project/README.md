# Maha B. Kazmi - SQL Portfolio

I am a data-driven professional with experience in Marketing, Communications, and Data Analytics. This portfolio showcases SQL projects focused on business insights and data storytelling.

## Project Index
- 1. Global Marketing Campaign Analysis
- 2. Customer Segmentation Project
- 3. Coming Soon

## Skills
- SQL (Joins, Aggregations)
- Data Analysis
- Marketing Analytics

## Tools Used
- SQLite / DB Browser
- SQL
- GitHub
- Kaggle

# Dataset Customer Segmentation Analysis

## Goal
Analyze customer spending behavior and identify high-value customer groups.

## Questions Answered
- Which age group spends the most?
- Which region performs best?
- Which product category generates the most revenue?

---

## Q1: Which age group spends the most?

-- Objective: Identify which age range has the most disposable income.

SQL Query: 

```sql
SELECT  Age, 
AVG ( "Purchase Amount (USD)") AS avg_purchase 
FROM shopping_trends
GROUP BY Age
ORDER BY Avg_purchase DESC;
```
![Spending by age](Age_Spending.png)

## Insights
- Customers aged 53 had the highest average purchase amount
- Customers between the ages of 49 and 54 consistently showed strong spending behavior
- Younger age groups generally spent less on average

A: Customers aged 53 had the highest average purchase amount

---


