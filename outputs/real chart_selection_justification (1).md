# Chart Selection Justification
## Part 4 — Tableau Executive Dashboard
**Student:** Satya | **ID:** 211817

---

## Chart 1 — Monthly Sales Trend by Category (Line Chart)

**Question answered:** How are sales changing over time, and which categories are driving growth or decline?

**Why this chart type:** A line chart is the most appropriate choice for showing change over time. Lines clearly communicate the direction and rate of change month by month, making it easy to spot peaks, troughs and trends. A bar chart for time series would be harder to read at this scale (24+ months of data).

**Fields used:**
- X axis: Order Date (aggregated by Month)
- Y axis: SUM(Sales)
- Color: Category (Furniture, Office Supplies, Technology — each a separate line)

**Design principle applied:** Used distinct colors for each category line so they can be differentiated at a glance. Kept the chart title simple and descriptive.

**Mistake avoided:** Did not use a stacked area chart, which would have made it hard to read individual category trends. Separate lines make each category's performance independently readable.

---

## Chart 2 — Sales and Profit by Region (Bar Chart)

**Question answered:** Which region generates the most sales and profit, and how do regions compare to each other?

**Why this chart type:** A horizontal bar chart is ideal for comparing values across a small number of discrete categories (4 regions). Bars make magnitude comparisons easy and intuitive. A map would also work but would require geographic coordinates and would not show profit as clearly.

**Fields used:**
- Rows: Region
- Columns: SUM(Sales) and SUM(Profit) as dual bars
- Color: Profit Margin (to show efficiency alongside volume)

**Design principle applied:** Sorted by Sales descending so the highest-performing region appears at the top. Added value labels to each bar so the exact figure is readable without needing to estimate from the axis.

**Mistake avoided:** Did not use a pie chart, which would have made the regional split hard to compare and would not show both Sales and Profit simultaneously.

---

## Chart 3 — Profitability by Category and Sub-Category (Bar Chart)

**Question answered:** Which categories and sub-categories are the most and least profitable?

**Why this chart type:** A horizontal bar chart with category grouping (using rows for both Category and Sub Category) provides a clear hierarchical breakdown. Each bar's length immediately shows the relative profit contribution, and the grouping makes it easy to compare sub-categories within each category.

**Fields used:**
- Rows: Category, Sub Category (nested)
- Columns: SUM(Profit)
- Color: SUM(Profit) — green for high profit, red for low/negative profit

**Design principle applied:** Used a diverging color scheme (green to red) so that loss-making sub-categories immediately stand out in red, drawing leadership attention to areas of concern without needing to read every value.

**Mistake avoided:** Did not use a treemap, which would have made sub-category comparison within categories harder. The bar chart keeps all values on a common axis scale, making magnitude comparisons accurate.

---

## Chart 4 — Sales and Profit by Customer Segment (Bar Chart)

**Question answered:** How do the three customer segments compare in terms of sales revenue and profitability?

**Why this chart type:** A grouped bar chart with Sales and Profit as separate bars per segment makes it easy to compare both metrics simultaneously across the three segments. The side-by-side layout is clearer than a stacked bar for this comparison.

**Fields used:**
- Columns: SUM(Sales) and SUM(Profit)
- Rows: Customer Segment
- Color: Customer Segment (distinct color per segment)

**Design principle applied:** Used consistent colors for each segment throughout the dashboard — the same color for Home Office, Consumer and Corporate appears in the segment chart, filters and legend. This consistency helps leadership build a mental model across charts.

**Mistake avoided:** Did not use a pie chart for segment comparison — pie charts make it very hard to compare segments when their values are close (as they are here, with all three segments between ₹70M and ₹75M).

---

## Chart 5 — Return Rate by Category and Segment (Bar Chart)

**Question answered:** Which categories and customer segments have the highest return rates, and where is the return risk concentrated?

**Why this chart type:** A horizontal stacked bar chart shows both the total return rate per category and the breakdown by segment within each bar. This allows leadership to see at once which category has the most returns and which segment is driving those returns.

**Fields used:**
- Rows: Category
- Columns: AGG(Return Rate) — calculated field
- Color: Customer Segment

**Design principle applied:** Kept the axis as a decimal proportion (0.00 to 0.25) rather than a count, which makes the return rate immediately interpretable as a percentage rather than requiring mental calculation.

**Mistake avoided:** Did not use absolute return counts, which would have been misleading — a category with more orders would naturally have more returns. Using return rate (returns / total orders) normalises for volume and makes the comparison fair across categories.

---

## KPI Cards — Total Sales, Total Profit, Profit Margin

**Question answered:** What is the overall business performance at a glance?

**Why this format:** KPI cards (large single-number tiles) at the top of the dashboard serve as the first point of reference for leadership. Before looking at any chart, a leader can instantly see the three most important metrics: ₹217M total sales, ₹33.3M total profit, 15.35% margin.

**Design principle applied:** Placed KPIs at the top of the dashboard following the F-pattern reading convention — readers naturally scan left to right across the top first. Large font size ensures the numbers are immediately readable.

**Mistake avoided:** Did not embed the KPI numbers within charts where they would be harder to locate. Dedicated tiles make them impossible to miss.

---

## Filters — Region, Category, Customer Segment

**Why these three filters:** Region, Category and Customer Segment are the three primary dimensions by which leadership analyses performance. Filtering by these dimensions allows any chart on the dashboard to be instantly re-scoped to a specific market, product area or customer type.

**Applied to all worksheets:** All three filters are connected to all sheets in the workbook via "Apply to All Using This Data Source" — so selecting South region instantly updates every chart to show only South data, making cross-chart comparison within a filter selection seamless.

**Mistake avoided:** Did not add too many filters (like Ship Mode or Campaign Channel), which would have made the filter panel cluttered and confusing. Three well-chosen filters cover the most important analytical dimensions without overwhelming the user.
