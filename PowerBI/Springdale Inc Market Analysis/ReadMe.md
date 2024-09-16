# Marketing Campaign Performance Dataset
## Overview
This dataset simulates a year of marketing activities and customer interactions for a fictional company called Springdale Inc. The company operates in multiple cities across the United States and offers a wide range of products, from electronics to beauty products.Springdale uses various marketing channels to promote its products, track customer behavior, and assess the effectiveness of its campaigns. This dataset aims to analyze customer purchasing behavior, campaign effectiveness, customer segmentation, and revenue generation over the period from April 1, 2023, to March 31, 2024.
This dataset can be used for Market Analysis, Customer Segmentation, Campaign Effectiveness Studies, and Lifetime Value Prediction.

## Project Story
The marketing department of TechWave launched a year-long initiative to optimize marketing spend and drive revenue. The initiative was designed to:
1. Understand customer behavior and lifetime value.
2. Optimize marketing channels for each product category.
3. Improve customer retention through targeted campaigns.
The marketing team tracked purchases, feedback, and engagement across different campaigns and seasons. This dataset captures the transactional data and feedback throughout this period, offering insights into the efficacy of different campaign strategies and the factors influencing customer retention and satisfaction.

## Dataset Structure
The dataset consists of multiple tables, and each table captures specific information related to customers, campaigns, locations, and seasonal events.

### 1. Main Table: Customer Transactions & Campaign Responses
  1. Customer ID: Unique identifier for each customer.
  2. Age:	Age of the customer (18 to 71).
  3. Gender:	Gender of the customer (Male or Female).
  4. City:	City where the customer resides.
  5. State:	State corresponding to the customer’s city.
  6. Income (USD):	Annual income of the customer.
  7. Purchase Date:	Date when the customer made a purchase.
  8. Product Category:	Category of the product purchased (e.g., Electronics, Clothing, Beauty).
  9. Revenue (USD):	Revenue generated from the purchase in USD.
  10. Campaign Source:	Marketing channel through which the customer was reached (e.g., Google Ads, Social Media).
  11. Campaign Type:	Type of marketing campaign (Retargeting, Brand Awareness, etc.).
  12. Customer Lifetime Value (USD):	Estimated lifetime value of the customer.
  13. Acquisition Cost (USD):	Cost incurred to acquire the customer.
  14. Customer Segment:	Type of buyer (Frequent Buyer or Occasional Buyer).
  15. Competitor Influence	Whether the customer has been influenced by competitors (Yes or No).
  16. Retention Rate	Whether the customer has been retained over time (Yes or No).
  17. Feedback Rating	Feedback score given by the customer on a scale from 1.0 to 5.0.
  18. Satisfaction Score (0-100)	Customer satisfaction score, ranging from 60 to 100.
  19. Discount Offered (USD)	Discount offered to the customer at the time of purchase.
  20. Response to Campaign	Whether the customer responded to the campaign (Yes or No).

### 2. Location Mapping Table
  1. City:	City name.
  2. State:	State corresponding to the city.

### 3. Seasonal Events Table
  1. Event:	Name of the seasonal event (e.g., Thanksgiving, Christmas).
  2. Date:	Date of the event.

## Technical Notes
The dataset was generated using Python, with pandas, random, and datetime libraries.
An IPYNB file is provided with the code used to create and manipulate the dataset.
The dashboard accompanying this dataset was created in Power BI to visualize KPIs such as revenue, customer retention, and campaign performance.

## KPI
Total Revenue: Sum of Revenue (USD) over time.
Customer Lifetime Value (CLV): Track CLV across different customer segments.
Customer Retention Rate: Percentage of retained customers (Retention Rate).
Campaign Effectiveness: Measure the response rate by comparing the number of Response to Campaign "Yes" vs. "No".
Satisfaction Score Distribution: Distribution of Satisfaction Score (0-100) across customers.
Revenue by Product Category: Bar chart showing revenue contributions from different Product Category.
Revenue by Campaign Source: Pie chart of revenue contribution by different Campaign Source.
Customer Feedback: Average Feedback Rating across different campaigns or customer segments.
