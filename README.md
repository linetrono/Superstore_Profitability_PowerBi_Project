#  Superstore Sales and Profitability Project

##  Project Overview
This Power BI project analyzes **sales, profit, and discount performance** across regions, product categories, and customer segments.  
It provides a clear view of key business drivers, helping management identify which areas contribute most to profit and which are affected by discounting and operational inefficiencies.

---

##  Objectives
- Understand overall **sales and profit trends** across different regions and categories.  
- Measure how **discounting impacts profit margins**.  
- Evaluate **regional and segment-level performance**.  
- Provide actionable insights to support **pricing and sales strategy** decisions.  

---

##  Key Insights
- **Total Sales:** $2.30M | **Total Profit:** $286K | **Average Discount:** 16%  
- The **West region** generated the highest revenue and profit, while the **Central region** had the lowest profit due to higher discounts.  
- **Technology** category showed strong profit margins despite moderate discounting.  
- **Furniture** had the largest share of discounts, significantly lowering profit margins.  
- **Consumer segment** contributed the highest sales volume but also received the highest discounts.  
- Overall, reducing excessive discounts in low-performing categories could lead to improved profitability.  

---

##  Tools & Techniques
- **Power BI Desktop:** For modeling, report building, and visualization  
- **Power Query:** For cleaning and transforming raw Superstore data  
- **DAX (Data Analysis Expressions):** For KPI calculations and measures  
- **Visualization:** Cards, bar charts, slicers, and interactive tooltips  

---

##  Key DAX Measures
```DAX
Total Sales = SUM(Sales[Sales])
Total Profit = SUM(Sales[Profit])
Profit Margin % = DIVIDE([Total Profit], [Total Sales])
```

---

[Dashboard View](dashboard_view.png)

[Download Insights Report(PDF)](Superstore_Insights_Report.pdf)

[Download/Watch Interactive Dashboard Demo](Superstore_Interactive_Dashboard)

