# 📊 Global Superstore Sales Performance Dashboard  
**Business Performance Analysis for Strategic Decision-Making | Power BI**

## 📌 Project Overview  

**Analyze and evaluate business performance across markets and product categories to support strategic decision-making.**

**Domain:** Retail / E-commerce  
**Tools:** Power BI, DAX, Excel  

**Author:** Quỳnh Trần  
**Date:** 2025  

---

## 📌 Background & Overview  

### 📖 What is this project about?

This project analyzes **Global Superstore sales data** to help business leaders understand overall performance and make better strategic decisions.

The dashboard focuses on answering key business questions such as:

- How is the company performing in terms of sales and profit?
- Which markets contribute the most to revenue and profitability?
- Which product categories drive business growth?
- Where are potential risks such as low margin or high return rates?
- How should management prioritize expansion and optimization efforts?

The goal is to transform raw transactional data into **clear, actionable insights** that support executive-level decision-making.

---

### 👤 Who is this project for?

This project is designed for:

✔️ Senior Managers & Business Leaders  
✔️ Business Analysts / Data Analysts  
✔️ Sales & Strategy Teams  
✔️ Anyone interested in data-driven business decision making  

---
## 📂 Dataset Description & Data Structure  

### 📌 Data Source  

- Dataset: **Global Superstore Dataset**  
- Domain: Retail / E-commerce  
- Format: CSV  
- Granularity: Order-level transactions  
- Purpose: Analyze sales, profit, customer behavior, and product performance  

---

## 📊 Data Structure & Relationships  

The dataset follows a **star schema model**, where one central fact table connects to multiple dimension tables.  
This structure supports efficient analysis and aggregation in Power BI.

---

### 1️⃣ Tables Used  

The project uses the following tables:

- **Fact_Orders** (main fact table)  
- **Product**  
- **Customer**  
- **People**  
- **Returns**  
- **Date**

---

## 📘 Table Schema & Sample Structure  

### 🔹 Fact_Orders (Main Fact Table)

This table contains transaction-level sales data and serves as the core of all calculations.

| Column Name | Data Type | Description |
|------------|-----------|-------------|
| Order ID | String | Unique identifier for each order |
| Order Date | Date | Date when the order was placed |
| Sales | Decimal | Total sales amount |
| Profit | Decimal | Profit generated from the order |
| Quantity | Integer | Number of items sold |
| Customer ID | String | Foreign key linking to Customer table |
| Product ID | String | Foreign key linking to Product table |
| Returned | Boolean | Indicates whether the order was returned |

---

<details>
<summary><b>🔹 Product Table</b></summary>

Contains information about products and their classifications.

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| Product ID | String | Unique product identifier |
| Product Name | String | Name of the product |
| Category | String | High-level product category |
| Sub-Category | String | Detailed product category |

</details>


---

<details>
<summary><b>🔹 Customer Table</b></summary>
Stores customer attributes used for segmentation and regional analysis.

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| Customer ID | String | Unique customer identifier |
| Segment | String | Customer segment (Consumer, Corporate, Home Office) |
| Region | String | Geographic region |
| Market | String | Market classification |

</details>
---

<details>
<summary><b>🔹 People Table</b></summary>
Represents sales representatives assigned to each region.

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| Person | String | Name of sales representative |
| Region | String | Region managed by the person |

</details>
---

<details>
<summary><b>🔹 Returns Table</b></summary>
Contains information about returned orders.

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| Order ID | String | Order identifier |
| Returned | Boolean | Indicates whether the order was returned (Yes / No) |

</details>
---

<details>
<summary><b>🔹  Date Table</b></summary>

Used for time intelligence and trend analysis.

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| Date | Date | Calendar date |
| Year | Integer | Year value |
| Month | String | Month name |
| Month Number | Integer | Month order (1–12) |
| Quarter | String | Quarter (Q1–Q4) |

</details>
---

## 🔗 Data Relationships  

- One-to-many relationship between **Customer → Fact_Orders**  
- One-to-many relationship between **Product → Fact_Orders**  
- One-to-many relationship between **Date → Fact_Orders**  
- One-to-many relationship between **Returns → Fact_Orders**  
- People table linked by **Region**  

The model follows a **star schema**, enabling efficient filtering, aggregation, and performance in Power BI.

<img width="572" height="514" alt="image" src="https://github.com/user-attachments/assets/cb506d09-274b-4def-9368-fd211c676fa4" />


## 🧠 Design Thinking Process  

This project applies a **Design Thinking approach** to ensure the dashboard solves real business problems and delivers actionable insights instead of only displaying metrics.

The process consists of four main stages:

1. Empathize  
2. Define (Point of View)  
3. Ideate  
4. Prototype & Review  

---

## 1️⃣ Empathize  

At this stage, we focus on understanding the stakeholder’s needs, goals, and challenges.

### 🎯 Target Stakeholder  
**Senior Manager / Business Leader**

### What the stakeholder wants:
- A quick and clear overview of overall business performance  
- Visibility into which markets and products drive revenue and profit  
- Early signals of risks such as declining margin or high return rates  
- Data-backed insights to support strategic decisions  

### What the stakeholder sees:
- Multiple markets and categories with different performance levels  
- Large volumes of raw data that are difficult to interpret  
- Performance changes across years  

### Pain Points:
- No single dashboard showing the full business picture  
- Hard to identify which markets or products should be prioritized  
- Difficult to compare performance across regions  
- Limited visibility into return rate impact  

### Gains (Expected Value):
- Clear understanding of business health  
- Easy identification of high-performing and underperforming areas  
- Faster and more confident decision-making  
- Actionable insights rather than raw numbers  

---

## 2️⃣ Define (Point of View)

### Problem Statement  

> Senior managers need a clear and intuitive dashboard that shows how sales and profit perform across markets and product categories, so they can prioritize investments, optimize resources, and improve overall business performance.

---

### Key Business Questions  

- How is the company performing overall?  
- Which markets generate the highest sales and profit?  
- Which markets show strong growth potential?  
- Which product categories contribute most to revenue and profit?  
- Are there markets or products with low margins or high return rates?  
- Where should management focus next to drive growth?  

---

## 3️⃣ Ideate  

Based on the business questions, the following analytical directions were explored:

### Core Analytical Ideas

- Analyze sales, profit, and margin trends over time  
- Compare performance across markets and regions  
- Evaluate product categories and sub-categories  
- Identify high-growth vs low-performing segments  
- Analyze return rates and their impact on profitability  
- Highlight opportunities and risks  

---

### Key Metrics Considered  

- Total Sales  
- Total Profit  
- Profit Margin  
- Total Orders  
- Return Rate  
- Sales Year-over-Year (YoY %)  

---

### Dimensions Used for Analysis  

- Time (Year, Month)  
- Market  
- Region  
- Country  
- Product Category  
- Sub-category  
- Customer Segment  

---

## 4️⃣ Prototype & Review  

Based on the ideation phase, the dashboard was structured into **four main pages**, each answering a specific business question.

### 📄 Page 1 — Executive Overview  
Provides a high-level snapshot of overall business performance.

Includes:
- KPI cards (Sales, Profit, Margin, Orders, Return Rate)  
- Sales & profit trends over time  
- Regional sales distribution  
- YoY performance overview  

---

### 📄 Page 2 — Market Analysis  
Focuses on understanding market-level performance.

Includes:
- Sales, profit, and margin by market  
- Year-over-year growth comparison  
- Market ranking  
- Identification of strong vs weak markets  

---

### 📄 Page 3 — Product Performance  
Analyzes performance across product categories and sub-categories.

Includes:
- Sales & profit by category  
- Sub-category performance comparison  
- Distribution of orders and profit  
- Identification of top and underperforming products  

---

### 📄 Page 4 — Recommendation & Insights  
Summarizes key findings and translates insights into actions.

Includes:
- Key business insights  
- Strategic recommendations  
- Growth opportunities  
- Risk areas to monitor  

---

📌 This design thinking process ensures the dashboard is **user-centered, insight-driven, and decision-oriented**, making it suitable for executive-level analysis.

## ⚒️ Main Process  

This section describes how the data was processed, analyzed, and transformed into meaningful dashboards.

---

## 1️⃣ Data Cleaning & Preparation  

Before analysis, the raw dataset was cleaned and structured to ensure accuracy and consistency.

### Key data preparation steps:

- Removed invalid or missing records  
- Standardized date formats  
- Converted data types (numeric, date, text)  
- Created calculated columns where necessary  
- Built relationships between fact and dimension tables  
- Ensured consistent category and market naming  
- Validated return flag values  

These steps help ensure reliable calculations and smooth performance in Power BI.

---

## 2️⃣ Exploratory Data Analysis (EDA)

Exploratory analysis was conducted to understand overall patterns before building dashboards.

### Key exploration areas:

- Distribution of total sales and profit  
- Trends over time (yearly performance)  
- Performance differences across markets  
- Product category contribution  
- Return rate behavior  

EDA helped identify early insights such as:
- Large variation in profitability between markets  
- Strong performance from a few key product categories  
- Potential risk areas with high return rates  

---

## 3️⃣ DAX Measures & Business Metrics  

Key business metrics were created using DAX to support analysis.

### Example DAX Measures

```DAX
Total Sales = SUM(Fact_Orders[Sales])

Total Profit = SUM(Fact_Orders[Profit])

Profit Margin = DIVIDE([Total Profit], [Total Sales])

Total Orders = DISTINCTCOUNT(Fact_Orders[Order ID])

Sales LY =
CALCULATE(
    [Total Sales],
    SAMEPERIODLASTYEAR('Date'[Date])
)

Sales YoY % =
DIVIDE([Total Sales] - [Sales LY], [Sales LY])

Return Rate =
DIVIDE(
    CALCULATE(COUNTROWS(Fact_Orders), Fact_Orders[Returned] = TRUE()),
    COUNTROWS(Fact_Orders)
)

---




### 📊 Key Insights & Visualizations

This section highlights the key findings derived from the Power BI dashboards.  
Each subsection corresponds to one dashboard page and summarizes **observations → insights → recommendations**.

---

This section highlights the key findings derived from the Power BI dashboards.  
Each subsection corresponds to one dashboard page and summarizes **observations → insights → recommendations**.


## 📘 Dashboard 1 — Executive Overview  

![Executive Overview](./images/dashboard_executive_overview.png)

### 🔍 Key Observations
- Overall sales and profit show a generally positive trend over time.
- Profit margin remains relatively stable across years.
- Return rate stays within a moderate range but should be monitored.
- A small number of regions contribute the majority of total revenue.

### 💡 Key Insights
- Business performance is growing steadily, indicating healthy operations.
- Revenue concentration suggests dependency on a few high-performing regions.
- Stable margin indicates cost control is effective overall.
- Even small increases in return rate may significantly impact profit.

### ✅ Recommendations
- Continue investing in high-performing regions to sustain growth.
- Track return rate closely as an early warning signal for operational issues.
- Use YoY growth metrics as a regular executive KPI.
- Monitor margin trends to prevent profitability erosion.

---

## 📘 Dashboard 2 — Market Analysis  

![Market Analysis](./images/dashboard_market_analysis.png)

### 🔍 Key Observations
- APAC and EU generate the highest total sales and profit.
- Some smaller markets show strong growth despite lower absolute revenue.
- Certain markets exhibit lower profit margins compared to others.
- Sales performance varies significantly across regions.

### 💡 Key Insights
- High-performing markets represent stable revenue pillars.
- Emerging markets with strong growth rates offer expansion opportunities.
- Low-margin markets may suffer from pricing pressure or high operational costs.

### ✅ Recommendations
- Prioritize investment and expansion in high-growth, high-profit markets.
- Review pricing strategies and cost structures in low-margin regions.
- Use YoY growth as a key indicator for market prioritization.
- Develop targeted strategies for underperforming markets.

---

## 📘 Dashboard 3 — Product Performance  

![Product Performance](./images/dashboard_product_performance.png)

### 🔍 Key Observations
- Categories such as **Phones, Copiers, and Chairs** generate the highest revenue.
- Some sub-categories achieve high sales but low profit.
- Return rates differ significantly across product groups.
- A small number of products account for a large share of profit.

### 💡 Key Insights
- High-performing categories should be treated as strategic products.
- Low-margin products may indicate pricing or cost inefficiencies.
- High return rates can negatively impact overall profitability.
- Product portfolio performance is uneven and requires prioritization.

### ✅ Recommendations
- Focus marketing and sales efforts on high-profit product categories.
- Reassess pricing, sourcing, or discount strategies for low-margin items.
- Improve quality control and logistics for products with high return rates.
- Use product-level insights to guide assortment and inventory planning.

---

## 📘 Dashboard 4 — Recommendations & Strategic Insights  

![Recommendations](./images/dashboard_recommendations.png)

### 🔍 Key Observations
- Growth is concentrated in specific markets and product groups.
- Profitability varies significantly across segments.
- Return rates represent a hidden cost driver.
- Data reveals clear opportunities for optimization.

### 💡 Strategic Insights
- Business performance can be improved by focusing on profitable growth rather than volume alone.
- Market-level differentiation is essential for expansion strategies.
- Product portfolio optimization has strong impact on margins.
- Continuous monitoring is required to prevent declining profitability.

### ✅ Actionable Recommendations
- Invest more resources in high-margin and high-growth markets.
- Scale successful product categories and phase out weak performers.
- Introduce tighter return management and quality checks.
- Use dashboard insights as a recurring decision-support tool for leadership.

---

📌 **Summary**

This visualization-driven analysis enables decision-makers to:
- Understand overall business performance at a glance  
- Identify growth opportunities and risk areas  
- Make informed, data-driven strategic decisions  
- Align operations, sales, and strategy using a single source of truth  



