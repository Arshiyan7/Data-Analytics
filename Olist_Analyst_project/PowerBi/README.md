# Power BI — Interactive Dashboard

This folder contains the final Power BI dashboard built on the five cleaned Olist CSV files. The dashboard is the visual payoff of the entire pipeline — data cleaned in Python, analyzed in SQL, pivoted in Excel, and now presented as a fully interactive report in Power BI.

---

## File

| File | Description |
|---|---|
| olist_dashboard.pbix | Power BI dashboard file with all measures, relationships and visuals |
| olist_dashboard.png | Static screenshot of the final dashboard |

---

## Data Model

All five cleaned CSV files were imported into Power BI. Relationships were built in the Model view with orders_cleaned as the central bridge table connecting all other tables.

| Table | Join Column | Related Table | Join Column |
|---|---|---|---|
| orders_cleaned | customer_id | customers_cleaned | customer_id |
| orders_cleaned | order_id | items_cleaned | order_id |
| orders_cleaned | order_id | payments_cleaned | order_id |
| orders_cleaned | order_id | reviews_cleaned | order_id |

---

## DAX Measures and Calculated Columns

### Measures

| Measure | Formula | Table |
|---|---|---|
| Total Revenue | SUM(items_cleaned[price]) | items_cleaned |
| Total Orders | DISTINCTCOUNT(orders_cleaned[order_id]) | orders_cleaned |
| Avg Review Score | ROUND(AVERAGE(reviews_cleaned[review_score]), 2) | reviews_cleaned |
| Avg Delivery Days | ROUND(AVERAGE(orders_cleaned[Delivery Days]), 1) | orders_cleaned |
| Late Delivery % | DIVIDE(COUNTROWS(FILTER(...Late)), COUNTROWS(FILTER(...delivered)), 0) * 100 | orders_cleaned |

### Calculated Columns

| Column | Formula | Table |
|---|---|---|
| Delivery Days | DATEDIFF(order_purchase_timestamp, order_delivered_customer_date, DAY) | orders_cleaned |
| Late Order | IF(order_delivered_customer_date > order_estimated_delivery_date, "Late", "On Time") | orders_cleaned |

---

## Dashboard Visuals

| Visual | Type | Fields Used |
|---|---|---|
| Total Revenue | KPI Card | Total Revenue measure |
| Total Orders | KPI Card | Total Orders measure |
| Avg Review Score | KPI Card | Avg Review Score measure |
| Avg Delivery Days | KPI Card | Avg Delivery Days measure |
| Late Delivery % | KPI Card | Late Delivery % measure |
| Revenue by State | Bar Chart | customer_state, Total Revenue |
| Revenue by Month | Line Chart | order_purchase_timestamp, Total Revenue |
| Revenue by Payment Type | Donut Chart | payment_type, Total Revenue |
| Avg Review Score by State | Bar Chart | customer_state, Avg Review Score |
| Orders by State | Filled Map | customer_state, Total Orders |

---

## Slicers

| Slicer | Field | Purpose |
|---|---|---|
| Year | order_purchase_timestamp | Filter all visuals by year |
| Order Status | order_status | Filter all visuals by delivery status |

---

## Key Insights

**Revenue Concentration** — Sao Paulo generates R$ 5.2 million in revenue, more than double Rio de Janeiro at R$ 1.8 million, indicating heavy geographic concentration in the southeast region.

**Late Delivery Rate** — 8.11% of all orders were delivered late. States like AL and MA show late delivery rates above 20% which directly correlates with their below average review scores.

**Payment Dominance** — Credit card accounts for nearly 78% of total payment value at R$ 12.5 million, with boleto as a distant second at R$ 2.9 million reflecting Brazilian payment preferences.

**Revenue Growth** — Revenue grew consistently throughout 2017 peaking at R$ 1 million in November driven by Black Friday. Revenue stabilized between R$ 850k and R$ 983k per month throughout 2018 indicating a maturing business.

**Customer Satisfaction** — The overall average review score is 4.09 out of 5. Rio de Janeiro, despite being the second highest revenue state, has a below average score of 3.87 highlighting a satisfaction gap in high volume regions.

---

## Dashboard Preview

![Olist Power BI Dashboard](olist_dashboard.png)

---

## Author

Arshiyan Mairaj
[LinkedIn](https://linkedin.com/in/arshiyanmairaj/) | [GitHub](https://github.com/Arshiyan7)