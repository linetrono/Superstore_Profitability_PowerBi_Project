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

## Dataset Information

- **Dataset Name:** Superstore Dataset (Final Version)  
- **Source:** [Kaggle – Superstore Dataset Final](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)  
- **Format:** CSV  

### Column Descriptions

| Column Name | Description |
|--------------|-------------|
| Order ID | Unique identifier for each customer order |
| Order Date | Date the order was placed |
| Ship Date | Date the order was shipped |
| Ship Mode | Shipping method used (e.g., First Class, Standard Class) |
| Customer ID | Unique customer identifier |
| Customer Name | Full name of the customer |
| Segment | Customer type (Consumer, Corporate, or Home Office) |
| Country | Country of the order (primarily United States) |
| City | City where the order was placed |
| State | State where the order was placed |
| Region | Regional grouping (East, West, Central, South) |
| Product ID | Unique product identifier |
| Category | High-level product grouping (Furniture, Office Supplies, Technology) |
| Sub-Category | More detailed product category |
| Product Name | Name of the product sold |
| Sales | Total sales revenue for the order line |
| Quantity | Quantity of items sold |
| Discount | Discount rate applied to the sale |
| Profit | Profit generated from the sale |
| Postal Code | Postal code of the customer’s location |

---

##  Data Preparation & Cleaning (Power Query)

The dataset was cleaned and transformed in **Power Query** before loading it into the Power BI model.  
Key data preparation steps included:

- **Removed Duplicates:** Eliminated duplicate rows to ensure data accuracy and consistency.  
- **Changed Data Types:** Assigned appropriate data types for each column — e.g., *Order Date* and *Ship Date* as **Date**, and *Sales*, *Profit*, and *Discount* as **Decimal Numbers**.  
- **Replaced Missing Values:** Handled and replaced null values to prevent calculation or visualization errors.  
- **Added Calculated Columns:**  
  - **Profit Margin:** Computed as *Profit ÷ Sales* to measure profitability efficiency for each transaction.  
  - **Year:** Extracted from *Order Date* to enable year-based analysis and trends.  
  - **Month:** Extracted from *Order Date* to analyze monthly seasonality.  
  - **Delivery Days:** Calculated as the difference between *Ship Date* and *Order Date* to evaluate delivery performance.  
  - **Month-Year Index:** Created to maintain proper chronological order in visuals across multiple years (since using “Month” alone sorts alphabetically or mixes years).  
- **Validated Data Integrity:** Confirmed all transformations and computed columns before loading the cleaned dataset into Power BI for modeling.

---

##  Data Modeling & Analysis
- The cleaned dataset was loaded into Power BI’s **Data Model**, where relationships and hierarchies (Year → Month → Category) were structured.  
- Created **measures** using **DAX (Data Analysis Expressions)** for KPI calculations.

### Key DAX Measures
```DAX
Total Sales = SUM(Sales[Sales])
Total Profit = SUM(Sales[Profit])
Profit Margin % = DIVIDE([Total Profit], [Total Sales])
Total Discount = SUM(Sales[Discount])
Average Discount % = AVERAGE(Sales[Discount])
Interactivity & Features
Slicers: Added for State, Category, Shipmode, Year and Segment to allow dynamic filtering.
Tooltips: Created to display quick summaries when hovering over visuals.
```

---

##  Key Insights

- **Total Sales:** $2.30M | **Total Profit:** $286K | **Average Discount:** 16%
  
**Profitability:** The company maintains a healthy **12.5% margin**, but performance varies sharply by region;**West** leads overall, the **South** operates most efficiently, while the **Central** region underdelivers due to likely cost or discount inefficiencies.  

**Discount Impact:** Heavy discounting in the **Consumer segment** erodes profit, whereas disciplined pricing in **Corporate** and **Home Office** segments sustains strong margins.  

**Product Focus:** **Copiers, Phones, and Accessories** are high-return categories. **Tables** and **Bookcases** underperform and need cost or pricing review.  

**Strategic Priorities:** Strengthen discount governance, investigate **Central region** profitability issues, and replicate **South region’s efficiency model** to lift overall margins.  

---

##  Tools & Techniques
- **Power BI Desktop:** For modeling, report building, and visualization  
- **Power Query:** For cleaning and transforming raw Superstore data  
- **DAX (Data Analysis Expressions):** For KPI calculations and measures  
- **Visualization:** Cards, bar charts, slicers, and interactive tooltips  

---

## VISUALS
[Dashboard View](dashboard_image_view.png)

[Download Insights Report(PDF)](Superstore_Insights_Report.pdf)

[Download/Watch Interactive Dashboard Demo](Superstore_Dashboard_GIF.gif)

---

## How to Use

1. **Explore the Dashboard**
   - View the interactive Power BI dashboard demo below or open the GIF preview to see the dashboard in action.

2. **Project Files**
   - `Superstore_Full_Report.pbix` – Contains the **dashboard sheet**, **tooltip sheet**, and **insights sheet**.  
   - `dashboard_image_view.png` – Static image of the final dashboard view.  
   - `Superstore_Dashboard_GIF.gif` – Animated dashboard preview.  
   - `Superstore_Insights_Report.pdf` – Downloadable insights report in PDF format.

3. **Interactivity**
   - Use slicers such as **Region**, **Category**, **Year**, and **Segment** to dynamically explore sales and profit data.  
   - Hover over visuals to see **tooltips** summarizing KPIs like Profit Margin, Sales, and Discounts.  
   - Navigate between the **Dashboard**, **Tooltip**, and **Insights** sheets for different levels of analysis.

---

## Topics / Tags

#powerbi #excel #dataanalysis #superstore #businessintelligence #salesdashboard #profitability #analytics #kpi #datavisualization

---

## Contact

If you’d like to connect or have questions about this project, feel free to reach out:

- **LinkedIn:** [Linet Rono](https://www.linkedin.com/in/linet-rono-b32130277/)  
- **Email:** mukamihrono@gmail.com  

---

## Reuse

This project is open for **learning and portfolio** purposes.  
You’re welcome to **reference, adapt, or build upon** this work in your own analyses or dashboards.  
If you reuse any part of this project, please credit or reference this repository.



