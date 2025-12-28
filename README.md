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


📌 **Note:**  
Only relevant columns used in analysis are documented to keep the model clean and business-focused.

