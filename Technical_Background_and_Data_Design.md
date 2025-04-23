# 🧠 Technical Background & Data Design Overview

This document serves as the technical companion to the **Superstore BI Analytics – Executive Business Intelligence Report**. It outlines the underlying dataset structure, relationships, modeling strategies, and data governance considerations that inform and support the insights and strategic recommendations presented in the main report.

---

## 📊 Dataset Overview

| Table Name | Row Count | Column Count | Description |
|------------|-----------|---------------|-------------|
| Orders     | 9,995     | 21            | Primary transaction dataset |
| People     | 5         | 2             | Sales Rep information (Region-based) |
| Returns    | 296       | 2             | Return status linked by Order ID |

---

## 🧱 Data Architecture & Table Relationships

The data model is built around the `Orders` table as the central fact table. The structure follows a one-to-many relationship model:

- `Orders` ←→ `Returns`: Joined by `Order ID`
- `Orders` ←→ `People`: Joined by `Region`

This design enables detailed profitability, discount, and return-level analysis while preserving referential clarity and segmentation logic.

---

## 🔗 Data Modeling Approach

- **Primary Key(s):** `Order ID` in Orders and Returns, `Region` in People
- **Join Types:** Left joins from `Orders` to both `Returns` and `People`
- **Cardinality Considerations:** Each order may or may not have a return; multiple orders per region are expected
- **Tool Used:** Tableau Desktop (Relationships/Joins set within Data Pane)

---

## 🧮 Custom Measures & Data Enrichment

The dataset was enriched with a series of calculated fields to enable deeper financial and behavioral analysis:

| Measure / Field Name         | Description |
|-----------------------------|-------------|
| `Total Sales by Year`       | Aggregated sales totals by year |
| `Returned %`                | Return rate by segment/category |
| `Returned Flag (Y/N)`       | Indicates if an order was returned |
| `Average Order Value (AOV)` | Total sales ÷ order count |
| `Original Sales Price`      | Sales before discount impact |
| `Profit Margin %`           | Profit ÷ Original Sales Price |
| `Revenue Lost %`            | Discount-driven erosion from original price |
| `Sales % of Total`          | Relative sales contribution (% of total) |
| `Sales Change ($)`          | Year-over-year sales delta |
| `True Discount`             | Effective discount relative to original price |
| `YoY Growth by Year`        | Year-over-year growth rate |
| `Running Total Sales`       | Cumulative sales performance (via QTC) |

---

## 🌍 Dataset Origin & Usage Rights

The dataset used is a **publicly available sample dataset** provided by Tableau and widely available through repositories like Kaggle and Tableau Public. It is intended for educational, analytical, and demonstration use.

- **Source:** Tableau Superstore Sample Dataset  
- **Usage:** Public domain, suitable for independent portfolio and analysis projects

---

## 🔐 Data Governance & Ethics Considerations

Although this project was completed in a simulated consultancy context with public data, the following data governance principles were respected:

- **Provenance:** Dataset source and public use license clearly cited
- **Accuracy:** Data integrity was reviewed during import and data prep
- **Security & Privacy:** No sensitive personal information is present in this dataset
- **Backup & Preservation:** `.twbx` file format maintained to prevent data loss during redesign or file migration

---

## 📘 Glossary of Key Terms

| Term | Definition |
|------|------------|
| **True Discount** | Difference between the original price and actual sales price, reflecting real revenue lost due to discounting. |
| **Profit Margin %** | Net profit as a percentage of the original sales price (Profit ÷ Original Sales Price). |
| **Revenue Lost %** | Percentage of potential revenue forfeited due to discounting. |
| **Returned %** | Proportion of total orders that were returned. |
| **Cost per Acquisition (CPA)** | The total cost incurred to acquire a customer or close a sale, often used to evaluate marketing or sales efficiency. |
| **Cost to Profit Conversion** | A measure of how effectively a cost input (e.g., discount, promotion, marketing) translates into net profit. |
| **Negative Inflection Point** | A moment in trend analysis where performance shifts direction, often signaling decline or deceleration in key metrics. |
| **Discount Erosion** | The gradual loss of profitability caused by excessive or poorly managed discounting strategies. |
| **Margin Efficiency** | A performance measure indicating how effectively a product, segment, or category generates profit relative to revenue. |
| **Regression (Linear)** | A statistical method used to model the relationship between a dependent variable and one or more independent variables. |
| **R² (Coefficient of Determination)** | Indicates how well a regression model explains variability in the data; values closer to 1 suggest a stronger model fit. |


---

## 📌 Related Files

- 📄 [Executive Business Intelligence Report README](./EExecutive_Portfolio_Summary_README.md)
- 📁 [Superstore-BI-Analytics GitHub Repository](./)

---

Let me know if you'd like me to generate the corresponding GitHub **commit message** or if you're ready to slot this into your repo structure and link it from the main README! 🚀
