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

<a id="design-thinking-process"></a>
## 🧠 Design Thinking Process  
<img width="1266" height="708" alt="image" src="https://github.com/user-attachments/assets/45a59d17-a5b2-4f83-b710-32864c19f1df" />
<img width="1242" height="690" alt="image" src="https://github.com/user-attachments/assets/1a38825a-df51-4971-a915-1df6aef350f4" />
<img width="1160" height="355" alt="image" src="https://github.com/user-attachments/assets/2ab0a45e-96c8-40f9-a557-bcac163d3580" />
<img width="1214" height="674" alt="image" src="https://github.com/user-attachments/assets/6cf83b55-6093-4f96-a8b3-d24f015f6028" />
<img width="1271" height="703" alt="image" src="https://github.com/user-attachments/assets/f2cac882-1fe1-4b8a-940f-9a2cd7a8e273" />
<img width="1219" height="599" alt="image" src="https://github.com/user-attachments/assets/4bb9165b-d804-41ab-9f9c-13a110e6afad" />
<img width="1221" height="603" alt="image" src="https://github.com/user-attachments/assets/82a78656-f36c-46d1-bfa4-e0f40a09b4c9" />

<a id="key-insights--visualizations"></a>
## 📊 Key Insights & Visualizations

## 1️⃣ Dashboard 1 — Executive Overview

<img width="1147" height="739" alt="image" src="https://github.com/user-attachments/assets/46a00595-9356-415b-8521-1176eb74166f" />

### 📌 Analysis 1

#### Observation 

**Overall business performance is strong:**
- **Total Sales:** $12.64M  
- **Total Profit:** $1.47M  
- **Profit Margin:** 12%  
- **Return Rate:** 4.68%

Sales and profit show a **steady upward trend from 2011 to 2014**, while profit margin remains relatively stable (~11–12%).  
➡️ This indicates that the business is growing **without significant margin erosion**.

However, performance is **not evenly distributed**:
- *Total Sales by Region* shows that revenue is heavily concentrated in a few regions, while several regions contribute marginally.
- *Total Sales YoY (%) by Market* highlights **Canada** as the fastest-growing market (~59.93% YoY), while **EU** records the lowest growth (~46.98% YoY).

➡️ Growth opportunities exist, but **growth quality and scalability** need deeper validation.

---

#### Interpretation (Why it matters)

At the executive level, the key question is not only:

> **“Are we growing?”**

but more importantly:

> **“Where is growth sustainable and profitable for expansion?”**

This dashboard confirms:
- The business is **healthy overall**
- But expansion decisions cannot rely on topline growth alone due to:
  - Market concentration risk
  - Uneven growth quality across regions

---

#### Recommendation

- Use **Dashboard 2 and Dashboard 3** to validate growth quality by answering:
  - Which products truly generate profit (not just sales)?
  - Which markets combine growth with margin stability?
- Treat **Return Rate (4.68%)** as an early profit risk signal, especially when scaling fast-growing markets.

✅ **Transition to Dashboard 2**  
Now that overall performance is confirmed as healthy, the next step is to identify **what actually drives profit** and whether growth is coming from *high-quality* or *risky* products.

---

## 2️⃣ Dashboard 2 — Product Performance


<img width="1076" height="739" alt="image" src="https://github.com/user-attachments/assets/f51827a4-374d-4791-b0cb-6d823c56caa0" />


### 📌 Analysis 2

#### Observation 

**Sales and profit concentration by Sub-Category is clear:**
- Top Sales Sub-Categories:
  - Phones (~$1.71M)
  - Copiers (~$1.51M)
  - Chairs (~$1.50M)
  - Bookcases (~$1.47M)
  - Storage (~$1.13M)

**Profit vs Sales Growth (YoY) bubble chart reveals:**
- Some sub-categories show **high YoY growth but low profit**, suggesting:
  - Margin pressure
  - High operational or logistics cost
- Other sub-categories deliver **strong profit even with moderate growth**, acting as stable “profit engines”.

The decomposition tree further shows:
- Revenue is largely driven by the **Consumer segment**
- **Technology** (especially Phones & Copiers) is a key profit contributor

---

#### Interpretation (Why it matters)

For market expansion, scaling is risky if growth is driven by:
- Low-margin products
- Products with unstable profit performance

This dashboard highlights that:
> **Not all revenue is equal**  
Some products generate sustainable profit, while others inflate sales but add limited business value.

---

#### Recommendation 

- Anchor expansion strategy on **profit-driving sub-categories**, not just top-selling ones.
- Prioritize products with:
  - Strong profit contribution
  - Stable margin behavior
  - Reasonable, sustainable growth
- For sub-categories with high growth but weak profit, investigate:
  - Over-discounting strategies
  - Shipping and logistics cost
  - Return-related issues
  - Customer expectation mismatch

✅ **Transition to Dashboard 3**  
Once profit-worthy products are identified, the final question becomes:
> **Which markets should receive investment for expansion—considering growth, profitability, and risk?**

---

## 3️⃣ Dashboard 3 — Market Analysis

<img width="1077" height="743" alt="image" src="https://github.com/user-attachments/assets/094cdfff-ae9f-4a60-8004-43d312ef3577" />

### 📌 Analysis 3

#### Observation 

**Market growth performance (YoY):**
- **Canada:** Highest YoY growth (~59.93%) but very small revenue base (~$0.1M)
- **APAC:** Large sales (~$3.9M) with healthy growth (~51.76%) → strong scale-growth balance

**Market profitability view shows:**
- APAC and EU generate the highest sales and profit, with stable margins around ~12%
- Some markets (e.g., Africa) experience margin drops to ~7%, indicating instability

**Sales Agent leaderboard reveals concentration risk:**
- One agent contributes a disproportionately large share of revenue (~$2.70M)
- This suggests dependency risk and uneven sales capability distribution

**Detailed table highlights hidden risk:**
- Several market + sub-category combinations show **high return rates**, even when sales are strong
- These returns can silently erode net profit during expansion

---

#### Interpretation (Why it matters)

This dashboard directly informs **market expansion decisions**:

- **APAC:** Expansion-ready  
  ✔ Large revenue base  
  ✔ Stable margin  
  ✔ Healthy growth

- **Canada:** High-growth but fragile  
  ✔ Strong momentum  
  ⚠ Small scale and higher uncertainty

- **Low-margin markets (e.g., Africa):** High risk  
  ⚠ Margin volatility signals unresolved operational or pricing issues

Return Rate must be treated as a **core expansion risk factor**, because scaling high-return markets increases cost and reduces net profitability.

---

#### Recommendation 

**Core Expansion (Low Risk, High ROI): APAC, EU**
- Scale best-performing product bundles (Technology / Phones / Copiers)
- Increase distribution and marketing investment due to stable profit structure

**Test Expansion (High Growth, Small Base): Canada**
- Run controlled pilot campaigns:
  - Focus on top-performing sub-categories only
  - Enforce strict return monitoring
- Track margin performance monthly before scaling further

**Fix-then-Grow Markets (Margin Risk): Africa & similar markets**
- Review pricing and discount strategies
- Address return drivers (logistics, product expectation)
- Expand only after margin stabilizes to target range

---
<a id="final-conclusion--recommendations"></a>
## 🔎 Final Conclusion & Recommendations

Based on the insights above, we recommend the **Senior Management / Commercial Strategy Team** to:

### 📌 Key Takeaways 

✔️ **Prioritize expansion in APAC (and EU)** where large revenue base and stable margins deliver the highest confidence ROI.  
✔️ **Treat Canada as a pilot market**, validating profitability and return risk before committing full-scale expansion.  
✔️ **Avoid expanding in low-margin or unstable markets** (e.g., Africa) until profitability issues are resolved.  
✔️ **Integrate product strategy into market expansion** by scaling only profit-driving sub-categories (Phones, Copiers, Chairs).  
✔️ **Use Return Rate as a mandatory risk KPI**, alongside Sales, Profit, and YoY Growth, to prevent profit erosion during expansion.

---

📎 *This project demonstrates how an executive-focused analytics dashboard can support data-driven market expansion and product portfolio optimization decisions.*
