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


### 📌 Analysis 1

**Observation**

The business generated substantial revenue and profit while maintaining a relatively stable profit margin over time. Sales and profit both show consistent growth across years, indicating that the company is expanding without significant margin deterioration.

However, revenue distribution is uneven across regions, with a limited number of markets contributing a disproportionate share of total sales. At the same time, growth rates differ significantly between markets, suggesting that expansion momentum is not evenly distributed.

**Interpretation**

Although overall performance appears stable, the business is structurally dependent on a small number of revenue-driving markets. This creates concentration risk, where future growth becomes vulnerable if key markets slow down.

Additionally, high growth in smaller markets may reflect early-stage expansion rather than scalable opportunities, meaning not all growth signals are equally reliable.

**Business Impact**

Strategic decisions should move beyond tracking total revenue growth and instead evaluate **growth quality**, focusing on whether markets can sustain expansion without weakening profitability.

**Recommendation**

- Prioritize evaluating markets based on **profitability and scalability**, not just growth rate.  
- Identify over-reliance on top-performing markets and explore diversification opportunities.  
- Use Return Rate and Profit Margin as early indicators to assess whether growth is sustainable.  

## 2️⃣ Dashboard 2 — Product Performance

<img width="1078" height="737" alt="image" src="https://github.com/user-attachments/assets/bc26a559-3c4f-4abc-82c3-313b684915d8" />

### 📌 Analysis 2

**Observation**

Sales performance is concentrated within a limited number of sub-categories, indicating that revenue generation relies heavily on a small portion of the product portfolio.

However, comparing profit and sales growth across sub-categories reveals a mismatch. Some products contribute significantly to revenue but generate relatively limited profit, while others maintain stable profitability even without aggressive growth.

In addition, revenue is largely driven by specific customer segments, and certain product categories—particularly within technology—play a central role in overall profit generation.

**Interpretation**

Not all revenue contributes equally to business value. Products that generate high sales but low profit may create operational pressure without improving financial performance.

This suggests that the current growth model may partially rely on volume-driven products rather than profit-driven ones, which can limit long-term scalability.

**Business Impact**

Expansion strategies should be aligned with **profit-generating products rather than high-volume products**. Scaling markets based on low-margin products may increase revenue while diluting overall profitability.

**Recommendation**

- Focus expansion on **sub-categories with stable profit contribution**, not just high sales volume.  
- Review pricing, discounting, and cost structure for products with high sales but low profit.  
- Monitor product-level return rates to identify items that negatively impact profitability.  
- Align product strategy with expansion strategy to ensure revenue growth translates into profit growth.  


## 3️⃣ Dashboard 3 — Market Analysis

<img width="1077" height="743" alt="image" src="https://github.com/user-attachments/assets/094cdfff-ae9f-4a60-8004-43d312ef3577" />

### 📌 Analysis 3

**Observation**

Market performance shows clear differences in scale, growth, and profitability. Some markets combine strong revenue contribution with stable margins, while others exhibit rapid growth but operate from a relatively small revenue base.

In addition, certain markets display signs of margin instability, suggesting potential inefficiencies in pricing, cost structure, or operations. Return rate patterns further highlight that some market–product combinations carry higher operational risk.

Sales performance is also unevenly distributed among sales agents, indicating dependency on a limited number of high-performing individuals.

**Interpretation**

Market expansion should not be driven by growth alone. Markets with high growth but low scale may not generate meaningful financial impact, while markets with unstable margins may reduce overall profitability when scaled.

A sustainable expansion strategy requires balancing revenue scale, margin stability, and operational risk.

**Business Impact**

Expanding into markets without stable profitability may increase sales volume while reducing overall business efficiency. Conversely, focusing on markets that combine scale and margin stability increases the likelihood of generating consistent and scalable profit growth.

**Recommendation**

- Prioritize expansion in markets with **strong revenue base and stable margins**.  
- Use controlled pilot strategies for high-growth but small-scale markets before full investment.  
- Address margin instability and return-related issues before scaling in weaker markets.  
- Reduce dependency on a small number of sales agents by improving distribution of sales performance.  

---
<a id="final-conclusion--recommendations"></a>
## 🔎 Final Conclusion & Recommendations

**1. Prioritize expansion in scalable and stable markets**  
Focus investment on markets that combine a strong revenue base with stable profit margins, as these markets are more likely to deliver predictable and sustainable returns.

**2. Validate high-growth markets before scaling**  
For markets showing rapid growth but small revenue scale, implement controlled pilot strategies to test demand sustainability, margin behavior, and operational risk before committing large resources.

**3. Align product strategy with market expansion**  
Prioritize scaling products that consistently generate profit contribution, rather than those that only drive high sales volume, to ensure that growth translates into real financial value.

**4. Address margin instability before expansion**  
In markets with fluctuating or declining profit margins, review pricing strategies, cost structure, and operational efficiency before increasing sales volume.

**5. Integrate Return Rate into decision-making**  
Treat Return Rate as a core KPI alongside Sales and Profit, as high return levels can significantly erode profitability when scaling markets or products.

**6. Reduce dependency on concentrated performance drivers**  
Mitigate reliance on a small number of markets, products, or sales agents by diversifying revenue sources and improving performance distribution.


### 📌 Key Takeaways 

✔️ **Prioritize expansion in APAC (and EU)** where large revenue base and stable margins deliver the highest confidence ROI.  
✔️ **Treat Canada as a pilot market**, validating profitability and return risk before committing full-scale expansion.  
✔️ **Avoid expanding in low-margin or unstable markets** (e.g., Africa) until profitability issues are resolved.  
✔️ **Integrate product strategy into market expansion** by scaling only profit-driving sub-categories (Phones, Copiers, Chairs).  
✔️ **Use Return Rate as a mandatory risk KPI**, alongside Sales, Profit, and YoY Growth, to prevent profit erosion during expansion.

---

📎 *This project demonstrates how an executive-focused analytics dashboard can support data-driven market expansion and product portfolio optimization decisions.*
