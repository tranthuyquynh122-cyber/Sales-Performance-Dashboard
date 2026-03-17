# 📊Sales Performance and Market Expansion Analysis for Global Superstore Retail | Power BI


**Domain:** Retail / E-commerce  
**Tools:** Power BI, DAX, Excel  

**Author:** Tran Thuy Quynh
**Date:** 2025  

---

## 📑 Table of Contents

1. [📌 Background & Overview](#-background--overview)  
2. [📂 Dataset Description & Data Structure](#-dataset-description--data-structure)  
3. [🧠 Design Thinking Process](#-design-thinking-process)  
4. [📊 Key Insights & Visualizations](#-key-insights--visualizations)  
5. [🔎 Final Conclusion & Recommendations](#-final-conclusion--recommendations)

---
<a id="background--overview"></a>
## 📌 Background & Overview
### 📖 What is this project about?

This project analyzes **sales performance and market expansion opportunities** for a global retail business using **Power BI**.

The core business question addressed in this project is:

> **Which markets and product categories should the business prioritize to grow sustainably and profitably?**

While overall revenue is increasing, the **quality of growth** varies significantly across markets and product categories:

- Profitability differs widely despite similar sales volumes  
- Strong sales growth does not always translate into higher profit due to margin pressure and product returns  
- Some fast-growing segments carry higher operational and profitability risks  

This project aims to help decision-makers:

- Understand **where revenue and profit are truly generated**
- Identify **high-growth but high-risk markets and product segments**
- Allocate resources more effectively between **volume-driven** and **profit-driven** areas  

✔ **The final output** is an **executive-level Power BI dashboard** that transforms raw sales data into **clear, actionable insights** to support strategic and data-driven decision-making.

---

### 👤 Who is this project for?

This project is designed for:

✔️ Senior Managers & Business Leaders  
✔️ Business Analysts / Data Analysts  
✔️ Sales & Strategy Teams  
✔️ Anyone interested in data-driven business decision making  

---
<a id="dataset-description--data-structure"></a>
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

## 📘 Table Schema & Sample Structure  

### 🔹 Fact_Orders (Main Fact Table)
<details>
<summary><strong>📦 Fact_Orders (Main Fact Table)</strong></summary>
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
</details>
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

<a id="design-thinking-process"></a>
## 🧠 Design Thinking Process

<img width="1162" height="655" alt="image" src="https://github.com/user-attachments/assets/6f775abe-81ab-410c-9d97-daf4d6d5d4cf" />

<img width="1242" height="690" alt="image" src="https://github.com/user-attachments/assets/1a38825a-df51-4971-a915-1df6aef350f4" />

<img width="1160" height="355" alt="image" src="https://github.com/user-attachments/assets/2ab0a45e-96c8-40f9-a557-bcac163d3580" />

<img width="1214" height="674" alt="image" src="https://github.com/user-attachments/assets/6cf83b55-6093-4f96-a8b3-d24f015f6028" />

<img width="1187" height="677" alt="image" src="https://github.com/user-attachments/assets/13dfb17b-fd1f-4120-b83a-0ac35459810d" />

<img width="1219" height="599" alt="image" src="https://github.com/user-attachments/assets/4bb9165b-d804-41ab-9f9c-13a110e6afad" />

<img width="1221" height="603" alt="image" src="https://github.com/user-attachments/assets/82a78656-f36c-46d1-bfa4-e0f40a09b4c9" />

<a id="key-insights--visualizations"></a>
## 📊 Key Insights & Visualizations

## 1️⃣ Dashboard 1 — Executive Overview

<img width="1097" height="717" alt="image" src="https://github.com/user-attachments/assets/54be4fa3-527f-4e0d-bef5-bd05b9d138ac" />

### 📌Analysis 1: Revenue Growth vs Profit Quality

#### Observation
Total sales increase consistently over time.  
However, profit fluctuates and does not grow at the same pace.  
Profit margin remains relatively stable without clear improvement.

#### Interpretation
Revenue growth is primarily driven by **increasing sales volume rather than margin improvement**.  
This indicates that higher sales do not consistently translate into higher profitability.

#### Recommendation
- Track **profit margin alongside revenue growth** to assess performance quality  
- Review **pricing, discounting, and cost structure**  
- Shift focus from **volume growth → profit efficiency**

---

### 📌Analysis 2: Market Structure — Core vs Emerging Markets

#### Observation
APAC and EU contribute the majority of total revenue.  
Canada and Africa operate at a smaller scale but show higher growth rates.

#### Interpretation
Markets are at different stages:
- APAC, EU → **mature markets (high scale, stable contribution)**  
- Canada, Africa → **emerging markets (lower base, higher growth)**  

#### Recommendation
- Maintain stability and performance in **core markets (APAC, EU)**  
- Expand selectively in **emerging markets (Canada, Africa)**  
- Align resource allocation with **market maturity**

---

### 📌Analysis 3: Return Rate as a Hidden Cost Factor

#### Observation
Return rate remains stable at around 4–5% over time.

#### Interpretation
Returns are a **persistent operational factor**, not a short-term issue.  
Even small percentages can significantly impact profitability at scale.

#### Recommendation
- Monitor return rate as a **core KPI**  
- Identify product categories with higher return frequency  
- Improve **product quality and fulfillment accuracy**
## 2️⃣ Dashboard 2 — Product Performance

<img width="1078" height="737" alt="image" src="https://github.com/user-attachments/assets/bc26a559-3c4f-4abc-82c3-313b684915d8" />


### 📌 Analysis 1: Product Revenue Concentration

#### Observation
Sales are concentrated in a few sub-categories such as **Phones, Copiers, and Chairs**.

#### Interpretation
Revenue dependency is concentrated in a limited number of products rather than evenly distributed.

#### Recommendation
- Reduce dependency on top-performing products  
- Strengthen mid-performing categories  
- Diversify product portfolio to balance revenue sources

---

### 📌 Analysis 2: Sales vs Profit Misalignment

#### Observation
Some products generate high sales but do not contribute proportionally to profit.

#### Interpretation
High sales volume does not necessarily indicate high business value.  
Profitability varies due to margin differences across products.

#### Recommendation
- Evaluate products based on **profit contribution, not only revenue**  
- Review pricing and cost structure for low-margin products  
- Prioritize products with **balanced sales and profitability**

### 📌 Analysis 3: Growth vs Profit Trade-off

#### Observation
Some sub-categories show strong sales growth but relatively lower profit contribution.

#### Interpretation
Growth and profitability are not always aligned.  
Scaling high-growth products may not improve overall performance.

#### Recommendation
- Combine **growth and margin metrics** in product evaluation  
- Focus on products with **sustainable performance**  
- Avoid scaling low-margin, high-growth products


## 3️⃣ Dashboard 3 — Market Analysis

<img width="1077" height="743" alt="image" src="https://github.com/user-attachments/assets/094cdfff-ae9f-4a60-8004-43d312ef3577" />

### 📌 Analysis 1: Market Maturity — Scale vs Growth Trade-off

#### Observation
APAC and EU maintain high revenue with stable growth.  
Canada and Africa show higher growth but operate at smaller scale.

#### Interpretation
The business operates across:
- **Mature markets → stable revenue**
- **Emerging markets → higher growth potential**

#### Recommendation
- Balance strategy between **stability and expansion**  
- Continue optimizing mature markets  
- Scale emerging markets gradually based on performance

---

### 📌 Analysis 2: Profit Efficiency by Market

#### Observation
Markets with similar revenue levels show different profit margins.

#### Interpretation
Revenue alone does not reflect performance quality.  
Profitability is influenced by cost structure and product mix in each market.

#### Recommendation
- Prioritize markets with **strong margin efficiency**  
- Re-evaluate markets with high revenue but lower profitability  
- Align market expansion decisions with **profit performance**

---

### 📌 Analysis 3: Sales Contribution Concentration

#### Observation
A small group of sales agents contributes a large portion of total revenue.

#### Interpretation
Revenue contribution is unevenly distributed, indicating dependency on a few individuals.

#### Recommendation
- Improve distribution of sales responsibilities  
- Reduce reliance on top-performing agents  
- Standardize sales practices across the team
---
<a id="final-conclusion--recommendations"></a>
## 🔎 Final Conclusion & Recommendations

### 📌 Final Conclusion

The business shows a **volume-driven growth pattern**, where increases in sales are not consistently matched by improvements in profitability.

Revenue is concentrated in a few **core markets (APAC, EU)** and **key product categories (Phones, Copiers)**, while other markets and products contribute at a smaller scale.  
At the same time, **profitability varies across both markets and products**, indicating differences in margin efficiency.

In addition, revenue contribution is unevenly distributed across sales agents, and return rate remains a consistent operational factor.

Overall, performance is influenced by:
- Differences in **market maturity (scale vs growth)**
- Variability in **product margin efficiency**
- Concentration across **products and sales contributors**

This suggests that future improvement depends on **optimizing efficiency rather than increasing volume alone**.

---

### 🚀 Recommendations

#### 1. Shift from Volume Growth to Profit Efficiency
- Track **profit margin alongside revenue growth**
- Review pricing, discounting, and cost structure at product level
- Prioritize **profit contribution over sales volume**

---

#### 2. Differentiate Market Strategy by Maturity
- Maintain stability in **core markets (APAC, EU)**
- Expand selectively in **emerging markets (Canada, Africa)**
- Align resource allocation with **market scale and growth stage**

---

#### 3. Optimize Product Portfolio
- Focus on products with **balanced sales and margin performance**
- Re-evaluate sub-categories with high sales but lower profitability
- Reduce dependency on a limited number of product groups

---

#### 4. Improve Sales Contribution Balance
- Reduce reliance on top-performing sales agents
- Improve distribution of accounts and workload
- Standardize sales practices across teams

---

#### 5. Manage Return-Related Impact
- Monitor return rate as a **core performance indicator**
- Identify product categories with higher return frequency
- Improve product quality and fulfillment accuracy

---

📎 *This project demonstrates how an executive-focused analytics dashboard can support data-driven market expansion and product portfolio optimization decisions.*
