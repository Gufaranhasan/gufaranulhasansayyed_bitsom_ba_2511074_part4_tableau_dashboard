Executive Retail Dashboard – Tableau Project

1. Business Problem Summary
The leadership team requires an executive-level dashboard to monitor:
- Sales performance
- Profitability trends
- Customer segment behavior
- Category-level risks
- Shipping efficiency
- Discount impact on margins
- Return patterns

The goal is to enable **data-driven decision-making**, improve profitability, and proactively identify business risks.

---

2. Dataset Description

**File Name:** dashboard_sales_data.xlsx  

The dataset contains transactional retail order data with the following key fields:

Key Dimensions
- Order: order_id, order_date, ship_date
- Geography: region, state, city
- Customer: customer_id, customer_segment
- Product: category, sub_category, product_name
- Logistics: ship_mode, delivery_days
- Marketing: campaign_channel

Measures
- sales
- quantity
- profit
- discount
- customer_rating

Flags
- return_flag (0 = not returned, 1 = returned)

---

3. Data Preparation & Assumptions

- Excel serial dates converted to standard date format
- Each row treated as a single order (for aggregation purposes)
- Profit assumed as net profit
- Return flag represents full order return
- Delivery delay derived from delivery_days

---

4. Tableau Workbook

**File:** tableau/executive_dashboard.twbx

The workbook includes:
- 7 analytical views
- 1 executive dashboard
- Interactive filters and actions
- KPI summary section

---

## 5. Calculated Fields

The following calculated fields were created:

1. Profit Margin  
2. Cost  
3. Average Order Value  
4. Return Rate  
5. Shipping Delay Bucket  
6. Discount Band (additional)

Refer to business_insights.md for detailed formulas.

---

## 6. Dashboard Components

### KPI Cards
- Total Sales
- Total Profit
- Profit Margin
- Average Order Value
- Return Rate

### Visualizations
- Sales trend over time
- Regional performance analysis
- Category profitability breakdown
- Customer segment comparison
- Discount vs profit scatter analysis
- Shipping performance analysis
- Return pattern analysis

---

## 7. Filters & Interactions

### Filters Used
- Region
- Category
- Customer Segment
- Date Range
- Ship Mode
- Campaign Channel

### Interactions
- Clicking region/category filters all charts
- Cross-filtering across all views
- Drill-down capability in category hierarchy

---

## 8. Key Business Insights

- Revenue growth is inconsistent across time
- High discounts negatively impact profitability
- Certain categories are consistently loss-making
- Delayed shipments correlate with higher returns
- Customer segments have varying profitability
- Some regions show high revenue but low margin

(Refer to outputs/business_insights.md for full insights)

---

## 9. Dashboard Story Summary

The dashboard highlights that while the business is generating strong sales, profitability is under pressure due to:
- Discounting strategies
- Logistics inefficiencies
- Product-level losses

Strategic actions include:
- Discount optimization
- Supply chain improvements
- Product portfolio rationalization

(Refer to outputs/dashboard_story.md for full narrative)

---

## 10. Assumptions & Limitations

### Assumptions
- One row = one order
- Profit is accurately reported
- No partial returns

### Limitations
- No cost breakdown (logistics vs product)
- No customer lifetime value tracking
- No inventory data
- Limited time span for trend analysis

---

## 11. Screenshots Included

- full_dashboard.png
- sales_trend_view.png
- regional_performance_view.png
- category_profitability_view.png
- filter_interaction_view.png

---

## 12. Conclusion

This dashboard provides leadership with a **holistic view of performance, risks, and opportunities**, enabling better strategic decision-making.
