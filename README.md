# SQL-Aggregations-and-basic-visualisation for marketing campaign data 

### Objective
Answer five business questions on the cleaned data with SQL, run from Python on a local SQLite database.

### Item	Description
Input	data/marketing_campaign_clean.csv	Output of notebook 01
Created	analysis.db	Local SQLite database with one table, sales (one row per customer)
Output	5 DataFrames (q1 to q5)	Query results used in notebook 03

### The five queries

1	Which education level responds best to the last campaign?	GROUP BY, SUM, AVG	:  The result is PhD

2	Do high-income customers spend and respond more?	CTE, NTILE(4), NULLIF	: The result shows that the categories of customers with big min_income and max_income spend have a big avg_total_spent and response_rate_pct

3	Which product categories generate most spending?	UNION ALL, SUM() OVER ()	: The result is "Wine"

4 Does household profile change the purchase channel?	CASE WHEN, GROUP BY 
     Business interpretation
Households with young children: price-sensitive customers who compare products online without completing a purchase. This suggests an issue with conversion on the website (pricing, delivery, or the purchasing journey) and indicates that these customers are responsive to promotional offers.
Households without children and teenagers: higher-volume customer segments, suitable for upselling and premium offers. The product catalog remains relevant for households without children.
Concrete action: reserve promotions and bundle offers for households with young children, and optimize the website for this segment (e.g., making offers more visible, providing promo codes, and simplifying the checkout process).

Which campaign performed best?	UNION ALL, rate computation	: The last campaign 
