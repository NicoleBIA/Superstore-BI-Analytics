# 📖 Diary Entry: Superstore BI Project – Key Insights & Breakthroughs

## 🚀 A Deep Dive into Data Validation & Customization

### 🔹 The Power of Verification – A Game-Changing Moment

Today, I had a powerful realization about the **importance of verifying calculations across different BI tools.** Initially, I was simply cross-checking the **Average Order Value (AOV) metric** in **Tableau** by running an `=AVERAGE(Sales)` formula in **Excel.** However, I noticed that the values didn’t match.

- **Tableau's AOV:** `$458.61`  
- **Excel's AOV (`=AVERAGE(Sales)`)**: `$229.86`  

Something wasn’t right. **If the same dataset is being used, why would Tableau and Excel calculate different AOV values?** This question led me to an important discovery about **data aggregation and BI methodology.**

### 🔍 Uncovering the Root Cause
After digging deeper, I realized that:
- **Excel’s `=AVERAGE(Sales)` function was averaging individual sales rows** (line items), rather than orders.
- **Tableau’s AOV calculation was correctly using:**
  ```sql
  SUM([Sales]) / COUNTD([Order ID])
