
# 📊 Retail Sales Performance Dashboard (Power BI)

## 🚀 Project Overview
This project presents an interactive Retail Sales Dashboard built using Power BI.  
The goal is to transform raw transactional data into meaningful insights for business decision-making.

---

## 📂 Data Source
- Dataset: Kaggle Retail Sales Dataset  
- Records: 1000 transactions  
- Features include:
  - Date
  - Product Category
  - Gender
  - Age
  - Quantity
  - Price per Unit
  - Total Amount

---

## 🎯 Key Objectives
- Analyze sales trends over time  
- Identify top-performing product categories  
- Understand customer purchasing behavior  
- Perform customer segmentation  
- Build a clean and professional dashboard  

---

## 📊 Key Insights
- 📈 Electronics contributes the highest revenue (~34%)  
- 👥 High spenders generate the majority of revenue  
- 🎯 Age group 46–55 spends the most  
- 📅 Sales show monthly fluctuations and patterns  
- ⚖️ Gender contribution is nearly balanced  

---

## 🧠 DAX Measures Used
```DAX
Total Revenue = SUM(Sales[Total Amount])
Total Orders = COUNTROWS(Sales)
Total Quantity = SUM(Sales[Quantity])
Average Order Value = AVERAGE(Sales[Total Amount])

Revenue % = 
DIVIDE(
    [Total Revenue],
    CALCULATE([Total Revenue], ALL(Sales[Product Category]))
)
