# Product-Level Discount vs. Profit Analysis

**Filename:** `Product_Discount_vs_Profit_Insight.md`  
🔗 **Related Strategic Recommendation:** [Product_Discount_Strategy.md](../../Strategic_Recommendations/Product_Discount_Strategy.md)

---

## 🟪 Overview

This product-level scatter plot explores the relationship between **True Discount ($)** and **Profit** across individual products. Each bubble represents a unique product and is color-coded by **Category**, sized by **Sales Volume**, and analyzed via regression trend lines by category.

- **X-Axis:** True Discount ($)  
- **Y-Axis:** Profit ($)  
- **Size:** Total Sales  
- **Color:** Product Category (Furniture, Office Supplies, Technology)  

---

## 🟩 Key Observations

- **Outlier – High Performer:**  
  *Canon imageCLASS 2200 Advanced Copier*  
  - **Profit:** $25,200  
  - **True Discount:** $8,400  
  - **Sales:** $61,600  
  - **Revenue Lost %:** 12%

- **Outlier – Loss Leader:**  
  *Cubify CubeX 3D Printer Double Head Print*  
  - **Profit:** -$8,880  
  - **True Discount:** $12,686  
  - **Revenue Lost %:** 46.98%

- **Anchoring Point:**  
  *Alliance Big Bands Rubber Bands, 12/Pack*  
  - **Profit:** $0  
  - **True Discount:** $0  
  - **Sales:** $30

- **Horizontal Outlier:**  
  *Cisco TelePresence System EX90 Videoconferencing Unit*  
  - **Profit:** -$1,811  
  - **True Discount:** $22,638  
  - **Revenue Lost %:** 50%

---

## 📉 Regression Trendlines by Category

These trendlines help illustrate the impact of discounting on profitability across categories.

### Furniture  
- **Equation:** Profit = -0.1131 × True Discount + 104.446  
- **R²:** 0.0438  
- **P-value:** < 0.0001  
> Discounts correlate negatively with profit — stronger downward slope.

### Office Supplies  
- **Equation:** Profit = 0.0261 × True Discount + 340.437  
- **R²:** 0.0007  
- **P-value:** 0.5869  
> Nearly flat trend, no significant correlation detected.

### Technology  
- **Equation:** Profit = 0.1172 × True Discount + 97.1322  
- **R²:** 0.0829  
- **P-value:** < 0.0001  
> Slightly positive correlation, indicating select discounted items can retain or boost profitability.

---

## 🟦 Strategic Angle

> This insight surfaces the complex and **nonlinear impact of discounting at the product level**. Some high-discount items remain profitable due to volume or perceived value (e.g., Canon Copiers), while others (e.g., Cisco TelePresence) suffer steep margin erosion.  
>  
> Understanding these dynamics enables **precision targeting** of product-level discount policies and paves the way for **AI-assisted strategies**, such as profit-optimized price recommendations and dynamic guardrails.

---

### 🟡 Visual Reference  
![Product Disc vs Profit Scatter](../../Assets/Product_Disc_vs_Profit_Scatter.png)

---

