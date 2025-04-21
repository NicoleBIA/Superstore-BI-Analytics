## Segment Discount Analysis – Profitability & Revenue Lost from Discount Erosion

![Segment_DiscountErosion_Overall.png](/Assets/Segment_DiscountErosion_Overall.png)

---

### 🟪 Why This Visual Was Created

This analysis extends prior profitability diagnostics, including findings from the **5 Whys root cause exploration** of Machines and discount-heavy product categories. The segment-level view was designed to answer:

> **Key Business Question:**  
> *How much revenue are we truly giving away through discounts at the segment level?*

Row-level discount fields suggested minor markdowns, but this visual interrogates the **true cost of discounting**—the difference between what customers actually paid vs. what they would have paid without any discount.

---

### 🟦 What This Visual Reveals

Although the **Consumer Segment** shows only **$820.91** in row-level discounts, its **actual revenue loss**—based on calculated pre-discount sales—was **$218,166.21**, or nearly **15% of potential revenue**. Corporate and Home Office show similar patterns:

| Segment       | Row-Level Discount | True Discount ($) | Revenue Lost % |
|---------------|---------------------|-------------------|----------------|
| Consumer      | $820.91             | $218,166.21       | 14.98%         |
| Corporate     | $477.85             | $132,734.91       | 15.36%         |
| Home Office   | $262.33             | $74,119.24        | 13.64%         |

Hover-enabled visuals below offer segment-specific breakdowns:

- ![Consumer Tooltip](/Assets/Segment_DiscountErosion_ConsumerTT.png)
- ![Corporate Tooltip](/Assets/Segment_DiscountErosion_CorporateTT.png)
- ![Home Office Tooltip](/Assets/Segment_DiscountErosion_HomeOfficeTT.png)

---

### 🟩 Why This Matters

Flat discount fields are **incomplete and misleading**. This diagnostic visual reframes discounting as a **revenue risk**, surfacing margin erosion that goes unseen when relying only on row-level discount summaries.

This insight supports strategic decisions across:

- 🟣 **Pricing Strategy** – Understand segment-level markdown leakage  
- 🟡  **Margin Strategy** – Improve control over hidden erosion  
- 🟢 **Sales Strategy** – Reinforce pricing discipline by customer type  
- 🔵 **Product Strategy** – Evaluate whether low-margin SKUs are driving heavy discounts  
- 🟣 **Regional Strategy** – Apply segment sensitivity based on geography

---

### 🟦 Strategic Takeaway

> **"Death by Discount" isn't always visible at the surface.**  
> Row-level markdowns might seem insignificant, but when measured against original pricing, they reveal substantial **lost revenue potential.**  
>  
> Integrating `True Discount ($)` and `Revenue Lost %` into performance dashboards enables proactive **margin protection** and **strategic recalibration of discount policies.**
