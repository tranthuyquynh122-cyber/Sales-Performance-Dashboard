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

This project builds a Power BI dashboard using the **Global Superstore Sales dataset**, including transactions (Orders), sales representatives (People), and product returns (Returns).  

The objective is to provide senior management with data-driven insights to evaluate **business performance, market efficiency, and growth opportunities**, with a focus on supporting strategic decisions around market expansion and profitability.  

The analysis aims to:  

- Assess **current business performance** across markets, products, and sales channels  
- Identify **which markets deliver sustainable growth vs. revenue driven by low-margin strategies**  
- Determine **priority markets for expansion** to improve both revenue and ROI  
- Highlight **strategic product categories** that contribute to long-term performance  
- Support more **data-driven decision-making** by balancing growth, profitability, and operational efficiency

### 🎯 Project Outcome  

The project delivers an interactive dashboard that enables stakeholders to:  

- Monitor performance across key markets, products, and sales teams  
- Identify markets with **high growth potential and stable profitability**  
- Detect markets where revenue growth is **not translating into profit**  

---

### 👤 Who is this project for?  

✔️ Data analysts and business analysts seeking actionable and decision-oriented insights  

✔️ Marketing and sales teams focusing on product performance and market growth  

✔️ Route-to-market teams aiming to optimize distribution strategies and expand market reach  

---

### ❓ Business Questions  

✔️ What is the current performance of Superstore across markets and product categories?  

✔️ Which markets should Superstore prioritize for expansion to achieve sustainable revenue growth and improved ROI?  

✔️ Which product categories should be prioritized to support long-term business growth?  

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


This dashboard highlights how differently revenue growth translates into profitability across markets.

#### Key Observations
- Canada records approximately **~15–18% revenue growth** while maintaining a **stable profit margin (~12–14%)**  
- APAC contributes a relatively high share of revenue (**~30% total sales**) but shows **lower margins (~5–7%)**  
- The US remains the largest market (**~35–40% total revenue**) with **consistent margin (~10–12%)** but slower growth  

#### Interpretation
- Canada is the only market where **revenue growth (~15–18%) is closely aligned with stable profit margins (~12–14%)**, indicating more sustainable performance  
- APAC growth is likely driven by **discounting or lower-margin products**, as reflected in its lower margin (~5–7%) despite a large revenue share  
- The US shows characteristics of a **mature market**, with stable margins (~10–12%) but slower growth compared to emerging markets  

#### Recommendation
- Prioritize expansion in **Canada**, where both growth and margin performance are aligned  
- Delay expansion in **APAC** until margin efficiency improves, as current growth does not translate into profit  
- Maintain the **US** as a stable revenue base and focus on operational efficiency rather than expansion  
  
## 2️⃣ Dashboard 2 — Product Performance

<img width="1078" height="737" alt="image" src="https://github.com/user-attachments/assets/bc26a559-3c4f-4abc-82c3-313b684915d8" />

This dashboard reveals gaps between revenue growth and actual profit generation.

#### Key Observations
- Phones and Tables generate high revenue but show a **margin gap of approximately 4–6%** compared to higher-margin categories  
- In categories such as Tables, revenue increases by around **~10%**, while profit grows only **~2–3%**, indicating weak profit conversion  
- Profit contribution is concentrated in categories like **Copiers and Accessories**, despite their smaller share of total revenue  

#### Interpretation
- Revenue growth is partially driven by **low-margin categories such as Tables**, reducing overall profitability  
- High-performing categories like **Phones** contribute significantly to revenue but are less efficient in profit generation  
- The business is scaling sales volume faster than it is improving margin quality  

#### Recommendation
- Prioritize **Copiers and Accessories**, which deliver higher profit efficiency  
- Reassess pricing and discount strategy for **Tables**, where margin performance is weak  
- Avoid focusing solely on revenue growth in categories that do not improve profitability

## 3️⃣ Dashboard 3 — Market Analysis

<img width="1077" height="743" alt="image" src="https://github.com/user-attachments/assets/094cdfff-ae9f-4a60-8004-43d312ef3577" />

This dashboard evaluates which markets are suitable for expansion by comparing growth patterns and profit performance.

#### Key Observations
- APAC and EU contribute the majority of total revenue but show **slower growth and limited margin improvement**  
- Canada contributes **less than 5% of total revenue** but demonstrates **higher growth compared to mature markets**  
- Africa also shows growth potential but with **greater volatility in both sales and profit performance**  

#### Interpretation
- APAC and EU are mature markets where additional expansion is unlikely to significantly improve profitability  
- Canada represents a **more stable emerging market**, where growth is supported by more consistent profit performance  
- Africa shows potential but lacks stability, increasing the risk of expansion  

#### Recommendation
- Select **Canada as the primary expansion market**, where growth and profitability are better aligned  
- Treat **Africa as a secondary opportunity**, requiring further validation before scaling  
- Avoid expanding in **APAC and EU**, and instead focus on improving operational efficiency  

---
<a id="final-conclusion--recommendations"></a>
## 🔎 Final Conclusion & Recommendations

### 📌 Key Conclusion

Canada should be selected as the **primary market for expansion**, as it demonstrates the strongest alignment between revenue growth and profitability.

Specifically:
- Canada achieves **~15–18% revenue growth** while maintaining **stable profit margins (~12–14%)**, indicating scalable and sustainable performance  
- APAC contributes a large share of revenue but operates at **lower margins (~5–7%)**, suggesting growth driven by discounting or low-margin products  
- The US remains stable with **consistent margins (~10–12%)** but shows slower growth, limiting its expansion potential  

These differences indicate that **not all revenue growth leads to profitable expansion**, and market selection should prioritize margin-supported growth rather than volume-driven performance.

---

### 🎯 Strategic Recommendations

1. **Prioritize expansion in Canada**  
   - Growth and profitability are aligned, reducing expansion risk  
   - Suitable for scaling without heavy reliance on discounting  
   - Represents the most balanced and scalable market opportunity  

2. **Delay expansion in APAC until margin performance improves**  
   - Current growth does not translate effectively into profit  
   - Requires optimization of pricing strategy and cost structure  
   - Expansion at this stage may increase revenue but dilute profitability  

3. **Maintain and optimize the US market**  
   - Provides a stable revenue base with predictable margins  
   - Focus on operational efficiency and margin improvement  
   - Not a priority for aggressive expansion  

4. **Shift performance focus from revenue to profit quality**  
   - Track profit margin as a core KPI alongside revenue  
   - Avoid scaling segments that increase volume but reduce margin  
   - Ensure growth strategies contribute to overall profitability  

5. **Align product strategy with profitability goals**  
   - Prioritize high-margin categories such as **Copiers and Accessories**  
   - Reassess low-margin categories such as **Tables and Bookcases**  
   - Reduce reliance on high-volume but low-profit product segments  

---

### 🚀 Business Impact

By prioritizing expansion in markets where growth is supported by profitability:

- The business can avoid scaling low-margin markets that reduce overall performance  
- Improve profit efficiency without increasing operational complexity  
- Build a more sustainable growth strategy rather than relying on short-term revenue expansion  
