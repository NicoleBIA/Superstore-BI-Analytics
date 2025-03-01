# 🧐 Customer Count Validation – Uncovering a KPI Discrepancy  

## 🔍 Discovery Moment  
While analyzing customer segmentation, I noticed something unusual: my **Customer Count KPI** reported **9994 customers**, but my **Customer Segmentation Analysis** only identified **793 unique customers** across high, medium, and low-value tiers.  

This discrepancy raised a red flag! Why would my total customer count be significantly higher than the sum of my segmented customer groups?  

## 🛠️ Investigation & Resolution  
Upon deeper analysis, I realized that my **original Customer Count KPI was flawed**—instead of counting **unique customers**, it was counting **total transactions (orders).**  

### **🔬 The Issue:**  
- The initial KPI used **`COUNT([Customer ID])`**, which counted **every instance** of Customer ID in the dataset (including repeat purchases).  
- The **correct approach** was to use **`COUNTD([Customer ID])`**, ensuring that each customer was counted only once, regardless of the number of orders they placed.  

### **✅ Solution Implemented:**  
- **Updated the Customer Count KPI Calculation:**  
  ```tableau
  COUNTD([Customer ID])
