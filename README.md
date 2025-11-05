# 📊  WTF-Sales-Analysis

This project explores and visualizes sales performance data for two countries (Germany and United States) across multiple years and regions using Excel. The dataset includes detailed transaction records such as revenue, sales quantity, cost of goods manufactured (COGM), discounts, and customer information from Germany and the United States.

---
## 🧠 Table of Contents
- [Project Context](#project-context)
- [Key Questions](#key-questions)
- [Dataset Description](#dataset-description)
- [Data Cleaning & Preparation](#data-cleaning--preparation)
- [Visuals & Dashboard](#visuals--dashboard)
- [Data Analysis & Insights](#data-analysis--insights)
- [Key Insights Summary](#key-insights-summary)
- [Recommendations](#recommendations)
- [Contact](#contact)
---

## 🧩 Project Context

**Industry**: Fintech & Sales Analytics
**Role**: Junior Data Analyst
**Tools Used**: Microsoft Excel (Pivot Tables, Charts, Slicers, Conditional Formatting, KPI Cards)

---

## 🎯 Key Questions

This project explores sales data to uncover trends, performance patterns, and seasonality insights across multiple years. It is divided into two main sections: A (Country Analysis) and B (Product Performance Analysis).

**Section A** — Country Sales Trends

1. Revenue Behavior: Highlight the sales revenue trend of the two countries over the years.

2. Pattern Analysis: Identify possible reasons for the observed sales behavior using evidence from the data.

3. Crisis Impact: Excluding Silicon Valley Bikes, compare monthly sales revenue year-over-year 2007 and 2008

**Section B** — Product Performance & Seasonality

1. Flop Product: Determine the product with the lowest sales quantity each year.

2. Top Seller: Identify which product category generated the highest revenue each year.

3. Category Contribution: Calculate what percentage the Off-Road Bikes category contributed to total bicycle sales.

4. Seasonal Behavior Case Study: Examine whether bicycles and accessories show expected seasonality patterns (higher sales in spring/summer). Identify any products that lack seasonality and support findings with temporal charts.

---

## 🗂️ Dataset Description

**Total Records**: 48,384
**Columns**: 23

Each row in the dataset represents a single sales transaction, detailing the customer, product, and financial performance of each sale across different regions and time periods.

This dataset was provided as part of a data analysis skill assessment project, designed to test the ability to identify, clean, and use the most relevant fields for accurate analysis and reporting. Specifically, it includes duplicate financial columns — one set in mixed currencies and another converted to U.S. dollars (USD).

**Fields included**:

YEAR, MONTH, DAY: Transaction date details used for temporal and seasonal analysis.

Customer / CustomerDescr: Unique customer ID and descriptive name.

City / Country / Salesorg: Location and organization of the sale.

OrderNumber / OrderItem: Unique identifiers for each sales order and line item.

Product / ProductDescr / Product Category: Product identifiers and descriptive details.

Division: Department or category under which the product is sold.

SalesQuantity: Number of units sold per transaction.

UnitOfMeasure: Unit in which the quantity is measured (e.g., pcs).

Revenue (Mixed Currency): Original sales amount in various currencies.

Revenue (USD): Converted sales amount standardized in U.S. dollars — used for analysis.

Discount (Mixed Currency) / Discount (USD): Discount amounts before and after conversion to USD.

CostOfGoodsManufactured (Mixed Currency) / CostOfGoodsManufactured (USD): Product manufacturing or procurement cost in both original and USD values.

Currency: Indicates the original currency before conversion.

**Note**:
All analyses, visualizations, and insights in this project are based on the USD-converted columns (Revenue USD, Discount USD, and COGM USD) to ensure consistency and comparability across countries.

---

## 🧹 Data Cleaning & Preparation

I performed all the cleaning and setup in Excel before moving into analysis. Here’s what I worked on:

First, I cleaned the table, promoted the first row to headers, and ensured each column had the correct data type.

I combined the Year, Month, and Day columns into a single Date column to support trend analysis over time.

Added new time-based fields — Month Name, Day Name, and Quarter of the Year — to enhance temporal insights.

Created four dimension tables (dim_calendar, dim_country, dim_customer, dim_product) and one Fact table.

Removed duplicates from all dimension tables to maintain data integrity.

For the Fact table, I used the USD columns for Revenue, Discount, and COGM, since they were the standardized versions of the mixed-currency values.

Finally, I established proper relationships between tables using the correct primary keys in the model view.

---

## 📸 Visuals & Dashboard

**1️⃣ Dashboard Overview**
<br><br>
![Dashboard Overview](images/dashboard.PNG)
<br><br>
**2️⃣ Sales Table – Before Cleaning**
<br><br>
![Sales table-Raw Data Overview](images/sales_dirty.PNG)
<br><br>
**3️⃣ Sales Table – After Cleaning**
<br><br>
![Sales table-After Cleaning Overview](images/sales_cleaned_data.PNG)
<br><br>
**4️⃣ Fact table**
<br><br>
![Fact table Overview](images/fact_table.PNG)
<br><br>
**5️⃣ Calendar Table (Dimension)**
<br><br>
![Calendar table Overview](images/calendar.PNG)
<br><br>
**6️⃣ Country table (Dimension)**
<br><br>
![Country table Overview](images/country.PNG)
<br><br>
**7️⃣ Customer table  (Dimension)**
<br><br>
![Customer table Overview](images/customer.PNG)
<br><br>
**8️⃣ Product table (Dimension)**
<br><br>
![Product table Overview](images/product.PNG)
<br><br>

---

## 📊 Data Analysis & Insights

After cleaning and structuring the dataset, several analyses were conducted in Microsoft Excel using Pivot Tables, Pivot Charts, Slicers, and Conditional Formatting to explore trends, performance, and seasonal patterns across countries and product categories.
<br>
**🏁 Section A — Country Sales Performance**

1. Sales Revenue Trend:

The two countries showed varying revenue patterns over the years.

Germany displayed steady growth, while USA experienced fluctuations, likely influenced by market size, customer base, and external economic conditions.

2. Possible Causes of Variation:

Differences in product demand, and purchasing power were key drivers of these variations.

Promotional discounts and currency effects also contributed to revenue differences.

3. After excluding Silicon Valley Bikes, the year-over-year comparison showed a noticeable dip in monthly revenue during 2008.

<br>

**🚴 Section B — Product Performance & Seasonality**

1. Flop Products:

Each year had 3 products(Fixed Gear Bike, City Bike Max, E-bike Tailwind) with very low sales quantities, indicating poor customer interest or overpricing.

Such items may require re-evaluation or marketing adjustments.

2. Top-Selling Products:

The three top revenue gennerating categories( Air pump,deluxe Road Bike, Men's off road bike hard tail) consistently generated the highest revenue across all years.

3. Category Contribution (2011 Focus):

In 2011, Off-Road Bikes contributed approximately 23% to overall bicycle sales.

4. Seasonal Behavior Case Study:

As expected, sales peaked during spring and summer months raising from March to June, reflecting increased outdoor activity. However, there was dropped in sales from June to December.

Temporal charts confirmed these patterns through visible monthly and quarterly trends.
<br><br>
---
<br><br>

## 💡 Key Insights Summary

Germany generated the highest overall revenue throughout the year.

Bike-related products remain the main revenue drivers.

Seasonal sales behavior aligns with outdoor weather patterns.
<br><br>

---

<br><br>
## 💡 Recommendations

Based on the sales analysis and insights drawn from the dataset, the following recommendations are suggested to help improve business performance and decision-making:

1. Focus on High-Performing Product Categories:
Continue to prioritize product categories with consistent revenue growth (e.g., Off-Road Bikes and Touring Bikes). Allocate more marketing and inventory resources to these categories.

2. Revisit Underperforming Products:
Products with persistently low sales volumes should be reviewed. Consider strategies such as redesign, bundling with high-selling items, or targeted discount promotions to improve performance.

3. Strengthen Country-Specific Sales Strategies:
Since sales trends vary between countries, tailor marketing and pricing strategies based on regional demand patterns and seasonality.

4. Manage Seasonal Demand Efficiently:
Seasonal patterns indicate higher sales during spring and summer. Stock levels, promotional campaigns, and staffing should align with these peaks to maximize profit and reduce overstock in off-peak months.

5. Leverage Data Continuously:
Maintain a consistent sales data tracking system to enable real-time insights, improve forecasting accuracy, and support data-driven business decisions.
<br><br>
---
<br><br>
## 🏁 Conclusion

This project applied data analysis techniques in Microsoft Excel to uncover key sales trends, product performance insights, and seasonal behaviors.

Overall, the project reinforced the power of data-driven decision-making in identifying business opportunities and improving performance through insight-led strategies.
<br><br>

---

## 📬 Contact

I’d love to connect and discuss more about data analytics, visualization, or collaborative projects!

💼 LinkedIn: www.linkedin.com/in/rafatadebanjo

📧 Email: aderafat.com

💻 GitHub: https://github.com/Rophah

Feel free to reach out — let’s turn data into meaningful insights together! 🚀


