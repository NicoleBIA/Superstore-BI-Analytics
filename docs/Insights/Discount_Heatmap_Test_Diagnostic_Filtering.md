# 🧪 Discount Heatmap Test: Diagnostic Aggregation Filtering

This diagnostic test visual was designed to explore how **filtering by `Order ID` at different granularities** affected the outcome of a heatmap showing **Discounts by Sales Rep and Sub-Category**. The initial goal was to identify whether large aggregate discount values observed in previous dashboard analyses were skewed by a **small number of high-discount transactions** or if broader patterns persisted across the dataset.

---

## 🧠 Test Setup

- **Dimensions Used:**  
  - `Person` (Sales Rep)  
  - `Sub-Category`  
- **Measures Used:**  
  - `SUM(Discount)` → **Color & Size** encoding  
  - `SUM(Profit)` → Tooltip  
  - `SUM(Sales)` → Tooltip  
- **Mark Type:** Square  
- **Key Visual Features:**  
  - Color and size encode total discount per sales rep and sub-category  
  - Tooltip includes total sales and profit for context  
  - Diagnostic filtering applied via **Order ID** → Condition by Count (≥ X)  

---

## 🔍 Diagnostic Filtering Strategy

To test the **impact of aggregation filtering**, different thresholds were applied to `Order ID` based on **number of Sub-Category records** per order:

| Filter Condition Applied (`CountD Sub-Category >= X`) | Screenshot Filename | Insights |
|--|--|--|
| No Filter | `Discount_Heatmap_Test_BySalesRep_SubCategory.png` | Full distribution view; reveals max discounts like Kelly Williams → Binders ($186.4) |
| `>= 14` | `Discount_Heatmap_Test_BySalesRep_SubCategory14.png` | Highly sparse results; only high-volume orders with 14+ sub-categories survive |
| `>= 10` | `Discount_Heatmap_Test_BySalesRep_SubCategory10.png` | Balanced middle-ground; slightly denser, captures moderate-to-large orders |
| `>= 8` | `Discount_Heatmap_Test_BySalesRep_SubCategory8.png` | Broader distribution; more reps and sub-categories populate the heatmap |

---

## 🧩 Key Observations

- ✅ **Kelly Williams → Binders** repeatedly showed deep discounting across all filters  
- ✅ Discount totals drastically dropped when filtered for orders with many sub-category records, suggesting **bulk-discounting patterns may cluster** in a few orders  
- 🔄 **Tooltip-level context** provided crucial insight — some sub-categories had high sales and discount totals but minimal profit (e.g., negative margin)  
- 🧠 Filtering by `Order ID` at different thresholds was effective for simulating real-world segmentation logic (e.g., analyzing only large bundle orders)  

---

### Visual Assets

All visuals are stored in the `/Images/` folder. Here are the linked references:

🖼 ![No Filter](/Assets/Discount_Heatmap_Test_BySalesRep_SubCategory.png) 
🖼 ![Filter ≥ 14](/Assets/Discount_Heatmap_Test_BySalesRep_SubCategory14.png)
🖼 ![Filter ≥ 10](/Assets/Discount_Heatmap_Test_BySalesRep_SubCategory10.png) 
🖼 ![Filter ≥ 8](/Assets/Discount_Heatmap_Test_BySalesRep_SubCategory8.png)

---

## 🧭 Why This Test Was Important

This diagnostic heatmap served as a **validation point** in the discounting investigation process. By applying filtering at the `Order ID` level, we were able to **simulate bulk order scenarios**, isolate high-discount transactions, and better understand **how a few orders may skew overall discount totals** in Tableau aggregations.

This type of analysis is helpful for:
- Validating dashboard KPIs
- Debugging “discount anomalies”
- Understanding data granularity limits
- Testing downstream visuals impacted by filter logic

---

