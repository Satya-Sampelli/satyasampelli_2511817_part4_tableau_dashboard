# Part 4 – Tableau Executive Dashboard & Data Storytelling

**Student:** Satya Sampelli
**Student ID:** 211817

---

# Business Problem Summary

The objective of this project is to build an interactive Tableau dashboard that helps retail management monitor business performance across different areas. The dashboard brings together sales, profit, customer segments, regional performance, category profitability, shipping performance, discount impact and return analysis so that decision-makers can quickly identify trends, opportunities and potential business risks.

---

# Dataset Description

**Dataset:** `dashboard_sales_data.xlsx`

The dataset contains retail order information from **January 2024 to December 2025**. It includes information related to sales, profit, customers, regions, product categories, shipping details, discounts and product returns.

Some of the important fields used in the dashboard include:

* Order Date
* Region
* Category
* Sub-Category
* Customer Segment
* Sales
* Profit
* Discount
* Ship Mode
* Delivery Days
* Return Flag

The data was connected directly to Tableau and used to create multiple visualisations and calculated fields.

---

# Tableau Workbook Description

The Tableau workbook (`executive_dashboard.twbx`) contains:

* 7 analytical worksheets
* 3 KPI worksheets
* 1 Executive Dashboard
* Multiple calculated fields
* Interactive filters
* Dashboard filter actions

The workbook has been saved as a packaged workbook (.twbx), allowing it to be opened without requiring any external data connection.

---

# Calculated Fields Created

The following calculated fields were created in Tableau:

| Calculated Field      | Purpose                                                    |
| --------------------- | ---------------------------------------------------------- |
| Profit Margin         | Calculates the percentage of sales converted into profit   |
| Cost                  | Calculates total cost by subtracting profit from sales     |
| Average Order Value   | Calculates average sales per order                         |
| Return Rate           | Calculates the percentage of returned orders               |
| Shipping Delay Bucket | Groups delivery days into Fast, Normal and Slow deliveries |

These calculated fields help provide additional business insights that are not directly available in the original dataset.

---

# Dashboard Components

The Executive Dashboard includes the following visualisations:

* KPI Sales
* KPI Profit
* KPI Profit Margin
* Monthly Sales Trend by Category
* Sales and Profit by Region
* Profitability by Category and Sub-Category
* Sales and Profit by Customer Segment
* Return Rate by Category and Segment

Together these views provide management with a complete overview of business performance.

---

# Filters and Interactions

The dashboard includes three interactive filters that apply across all visualisations:

* Region
* Category
* Customer Segment

Users can also interact with the charts to explore specific business areas. Selecting a region updates the other charts, making it easier to analyse regional performance in greater detail.

---

# Key Business Insights

Some important insights from the dashboard include:

* Technology generates the highest sales and profit among all product categories.
* The South region performs best in both sales and profit.
* Copiers, Accessories and Phones are the most profitable sub-categories.
* Furniture contributes noticeably lower profits than Technology.
* The Home Office segment generates the highest sales among customer segments.
* Profit changes considerably across categories, showing that not all sales contribute equally to profitability.
* Regional performance differs significantly, suggesting opportunities to improve lower-performing regions.
* The interactive filters allow management to quickly compare performance across different regions, categories and customer segments.

---

# Dashboard Story Summary

The dashboard provides management with a single view of overall business performance. It highlights where sales and profits are strongest, identifies the best-performing regions and product categories, and allows leadership to compare customer segments using interactive filters.

Rather than focusing on one metric, the dashboard combines multiple business perspectives to support faster and better decision-making.

---

# Assumptions and Limitations

## Assumptions

* Sales and profit values in the dataset are accurate.
* Return Flag correctly identifies returned orders.
* Delivery Days correctly represent shipping duration.
* The calculated fields accurately reflect business performance.

## Limitations

* The dashboard covers only the available two-year period.
* External factors such as economic conditions or competitor activity are not included.
* The analysis is based only on the variables available in the dataset.

---

# Screenshots Included

The repository includes the following screenshots:

* `full_dashboard.png`
* `sales_trend_view.png`
* `regional_performance_view.png`
* `category_profitability_view.png`
* `filter_interaction_view.png`

These screenshots provide evidence of the completed Tableau dashboard and its interactive functionality.
