# Online Shop 2024 — Sales & Commercial Performance Analysis

## Project Overview

This project analyzes an online retail dataset to understand sales performance, product and category contribution, customer activity, supplier concentration, discounting, freight, and shipment performance.

The project was built in **Excel 2016** using **Power Query, Power Pivot, DAX, PivotTables, PivotCharts, and interactive dashboards**.

The goal was to turn raw transactional data into a structured analytical model and use it to produce practical commercial and operational insights.

---

## Business Questions

- How did sales change over time?
- Which categories and products generated the most sales?
- How concentrated were sales across suppliers?
- How much revenue was reduced through discounts?
- How did freight move relative to sales?
- What was the shipment status distribution?
- What did customer ratings and product review activity indicate?

---

## Dataset & Data Model

The dataset contains eight source tables:

- Orders
- Order Details
- Customers
- Products
- Suppliers
- Reviews
- Payments
- Shipments

A dedicated **Calendar** table was also created for time-based analysis.

The tables were connected in Power Pivot using relationships between customers, orders, products, suppliers, reviews, payments, shipments, and the calendar.

Because the transaction tables operate at different levels of detail, the model was treated as a relational analytical model rather than a single flat dataset.

---

## Data Preparation

Power Query was used to:

- Clean and structure the source tables
- Assign appropriate data types
- Prepare the tables for the Data Model
- Create the Calendar table
- Add date attributes such as Year, Quarter, Month and Year-Month
- Create delivery-day calculations

The prepared data was then loaded into Power Pivot for modelling and analysis.

---

## Analytical Model

DAX measures were created for key metrics including:

- Total Sales
- Gross Sales
- Discount Amount
- Discount Rate
- Sales Retention Rate
- Total Orders
- Total Customers
- Total Units Sold
- Average Order Value
- Total Freight
- Freight % of Sales
- Average Delivery Days
- YoY Sales Growth
- YTD Sales
- Orders by Category

**Metric definitions:**

- **Gross Sales** = sales value before discounts
- **Discount Amount** = value deducted through discounts
- **Total Sales** = Gross Sales minus Discount Amount
- **Discount Rate** = Discount Amount ÷ Gross Sales
- **Sales Retention Rate** = Total Sales ÷ Gross Sales

Unless otherwise stated, **sales in this analysis refers to Total Sales after discounts**.

---

# Key Findings

## Strong Overall Sales Performance

The dataset recorded **$1.27M in Total Sales after discounts across 830 orders and 91 customers**.

Average order value was **$1,525.05**.

**Year-over-year sales growth was 53.4%**, comparing sales with the corresponding previous-year period.

---

## Sales Varied Significantly by Year

| Year | Total Sales | Share of Total |
|---|---:|---:|
| 2013 | $208,083.97 | 16.4% |
| 2014 | $617,085.20 | 48.7% |
| 2015 | $440,623.87 | 34.8% |

2014 was the strongest year, generating **$617,085.20**, or 48.7% of total sales.

Compared with 2013, **2014 sales increased by approximately 196.6%**.

Sales then declined by approximately **28.6% in 2015 compared with 2014**.

This shows that sales growth was concentrated around 2014 rather than increasing consistently across every year.

---

## Electronics Dominated Sales

Electronics generated **$571,680.12**, representing approximately **45.2% of Total Sales**.

The remaining categories contributed:

- Home & Kitchen — 24.4%
- Accessories — 16.7%
- Furniture — 13.8%

Electronics therefore accounted for almost half of the sales value and was the largest contributor by a significant margin.

---

## A Small Group of Products Generated Significant Sales

The **Wireless Charger** was the highest-selling product at **$141,396.74**, representing approximately **11.2% of Total Sales**.

Other high-selling products included Storage Containers, Computer Speakers, Gaming Keyboard, and Rice Cooker.

The concentration of sales among leading products makes product-level performance an important area for monitoring.

---

## Discounting Reduced Gross Sales by 6.55%

**Gross Sales before discounts were $1,354,458.59.**

Discounts amounted to **$88,665.55**, resulting in **$1,265,793.04 in Total Sales after discounts**.

The overall discount rate was **6.55%**, meaning approximately **93.45% of Gross Sales was retained after discounts**.

Accessories had the highest discount rate at **7.14%**, while Electronics had the lowest at **5.98%**.

The **Wireless Charger** had the largest discount amount among individual products at **$8,587.47**.

This analysis measures discount intensity and revenue retention; it does not establish that higher discounts caused higher sales.

---

## Supplier Sales Were Concentrated

The top 10 suppliers generated **$858,856.07**, representing approximately **67.9% of Total Sales**.

The largest supplier by sales was **Premier Logistics Inc.**, with **$172,765.83** in Total Sales.

This concentration makes the performance and continuity of major supplier relationships important to overall sales.

The dataset does not contain procurement costs, supplier lead times, or alternative-supplier information, so the analysis does not attempt to quantify supplier risk.

---

## Freight Followed the Broad Sales Pattern

Total freight was **$64,942.69**, equivalent to approximately **5.13% of Total Sales**.

Monthly analysis showed freight broadly moving with sales activity. Both measures peaked in April, declined sharply in May, reached their lowest point around June, and generally increased toward the end of the year.

The analysis identifies the pattern but does not establish a causal relationship between sales and freight.

---

## Shipment Status

The shipment data contained **15,000 records**.

- Delivered — 35.8%
- Shipped — 35.6%
- Pending — 23.7%
- Cancelled — 4.9%

Pending shipments represented nearly one-quarter of the shipment records, making shipment status an important operational metric to monitor.

The percentages are presented descriptively rather than being labelled as good or bad because the dataset does not provide operational benchmarks.

---

## Customer Ratings

The rating distribution contained **1,106 reviews**.

The most common rating was **1 star, with 280 reviews**, while 4-star reviews were the least common at 168.

This distribution provides an important customer-feedback signal and highlights the need to investigate the reasons behind the relatively high volume of low ratings.

---

# Dashboards

### Executive Overview

The first dashboard provides a high-level view of:

- Total Sales
- Total Orders
- Total Customers
- Average Order Value
- Monthly Sales Trend
- Sales by Category
- Top 10 Products
- Customer Rating Distribution

Interactive slicers allow users to filter the analysis by Year, Month, Category, Rating, and Shipment Status.

### Commercial & Operations

The second dashboard focuses on:

- Total Sales
- YoY Growth
- Total Orders
- Freight % of Sales
- Sales and Discount by Category
- Top 10 Discounted Products
- Top 10 Suppliers by Sales
- Sales and Freight Trend
- Payment Status

---

# Business Recommendations

### 1. Monitor Electronics closely

Electronics contributes 45.2% of Total Sales, making it the largest driver of revenue. Its product mix and sales performance should therefore receive close attention.

### 2. Monitor high-contributing products

Products responsible for a large share of Total Sales should be monitored closely for availability and changes in sales performance.

### 3. Review discount levels by category

Discount intensity differs across categories, with Accessories recording the highest discount rate. Discount decisions should therefore be evaluated by category rather than applying a uniform approach.

### 4. Monitor major supplier relationships

With the top 10 suppliers contributing 67.9% of Total Sales, changes in the performance of key suppliers could have a noticeable effect on overall sales.

### 5. Monitor pending shipments

Pending shipments account for 23.7% of shipment records. Tracking this measure over time can help identify periods where shipment activity requires further investigation.

### 6. Investigate customer feedback

The high number of 1-star reviews makes customer feedback an important area for further investigation, particularly around the products receiving the highest volume of negative ratings.

---

# Limitations

- The dataset does not provide business context for major changes in annual sales.
- Supplier analysis measures sales concentration rather than procurement or supplier risk.
- Discount analysis does not establish whether discounts caused higher sales.
- Shipment status percentages cannot be judged against an operational target because no benchmark is provided.
- Customer ratings and reviews are descriptive and may not represent all customers.
- The dataset contains unusually high recorded quantities for some orders, so unit-based metrics should be interpreted with caution.
- The analysis reflects the available dataset and should not be treated as a complete representation of real-world business performance.

---

# Tools & Skills

**Tools:**  
Microsoft Excel 2016 · Power Query · Power Pivot · DAX · PivotTables · PivotCharts · Excel Slicers

**Skills demonstrated:**  
Data cleaning · Data transformation · Data modelling · Table relationships · DAX measures · Time intelligence · Sales analysis · Product analysis · Category analysis · Supplier analysis · Discount analysis · Operational analysis · Dashboard development

---

## Project Outcome

The project transformed multiple retail tables into a connected analytical model and two interactive dashboards.

The resulting analysis provides a consolidated view of **sales performance, product and category contribution, supplier concentration, discounting, freight, shipments, and customer feedback**, demonstrating how Excel can be used for structured business analysis beyond basic spreadsheet reporting.
