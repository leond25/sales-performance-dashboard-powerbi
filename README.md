# Sales Performance Dashboard (MySQL + Power BI)

## 📌 Project Overview
This project analyzes a simulated retail company's sales data to understand the root causes of a revenue decline in Q4 2025.  
I built an executive-facing dashboard in Power BI connected to a MySQL database to identify product, channel, and customer drivers behind the decline and propose data-backed recommendations.

## 🎯 Business Question
Why did revenue decline in Nov–Dec 2025, and what actions should the business take to recover?

## 🧱 Data Model
Relational schema designed in MySQL:
- customers (customer_id, name, signup_date, country)
- products (product_id, product_name, category, price)
- orders (order_id, customer_id, order_date, channel)
- order_items (order_item_id, order_id, product_id, quantity, unit_price, discount_pct)

Star schema with a Date dimension in Power BI for time intelligence.

## 📊 Dashboard Pages

### Page 1 – Executive Summary
- KPI Cards: Total Revenue, Total Orders, AOV  
- Monthly Revenue Trend  
- Revenue by Product  
- Interactive slicers (Channel, Category, Date)

### Page 2 – Product Deep Dive
- Product revenue trends over time  
- % revenue contribution by product  
- Identifies declining performance of top revenue driver (Pro Subscription)

### Page 3 – Customer & Channel Analysis
- Repeat customers table  
- Revenue by sales channel  
- Isolates channel-level drivers of revenue decline

## 🔍 Key Insights
- Revenue declined significantly in Nov–Dec 2025.
- Pro Subscription drives the majority of revenue and experienced a sharp MoM decline.
- The Online channel contributed most to the revenue drop.
- Discount usage increased in late Q4, compressing revenue.

## 💡 Recommendations
- Launch retention campaigns for Pro Subscription customers.
- Bundle Analytics Add-on with Pro Subscription to increase AOV.
- Reduce discount reliance and test value-based pricing.
- Improve onboarding to reduce early churn among new customers.

## 🛠 Tools & Skills
- SQL (MySQL): data modeling, aggregations
- Power BI: dashboard design, DAX measures, data modeling
- DAX: Total Revenue, AOV, MoM % change
- Business Analysis: KPI design, root-cause analysis, executive storytelling

## 📂 Files
- `/sql/schema.txt` – database schema
- `/sql/sample_data.txt` – sample data
- `/dax/measures.txt` – DAX measures used
- `/screenshots/` – dashboard visuals

## 📎 How to Reproduce
1. Create the MySQL schema using sql commands in `schema.txt`
2. Load sample data from `sample_data.txt`
3. Connect Power BI to MySQL
4. Build visuals using the measures in `/dax/measures.txt`
