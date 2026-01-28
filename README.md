# Electronic-Sales-Performance-Dashboard
A business intelligence project built in Power BI to analyze electronics sales, profitability, product performance,regional and time-based trends using DAX. this insights help stakeholders to make data-driven decisions by tracking key business metrics over time.


## 📊Project Overview
This project was developed to provide business stakeholders with a single source of truth for monitoring electronics sales performance. Prior reporting was static and time‑consuming, making it difficult to compare current results with historical performance. The goal was to design an interactive BI solution that delivers fast, accurate, and actionable insights.


## 🛠 Approach & Methodology

1. **Data Preparation**
    Cleaned and validated sales data to remove inconsistencies and duplicates
    Standardized date formats and categorical fields

2. **Data Modeling**
   Built a star-schema style model
   Created and marked a custom calendar table to support time intelligence

3. **DAX & Calculations**
   Developed core KPIs such as Total Sales, Total Profit, and Profit Margin
   Implemented advanced time-based measures (YTD, QTD, YoY, SPLY)
   Enabled year-over-year performance comparison

4. **Visualization & UX**
   Designed KPI cards for quick executive insights, Used trend lines, bar charts, and maps for intuitive storytelling
   Added slicers for flexible data exploration


## 🎯Objectives
Management needed a clear and interactive way to:

Track overall sales and profit performance

Compare current results with historical periods

Identify high‑performing and underperforming products

Understand regional and channel‑based sales patterns


## Dataset
The dataset includes supply chain information such as:


Order date

Order id


Order quantity


Unit cost



Price


Sales


Channel


Product categories



Product name


Product sub categories


Promotion name


State


Zone


## 📈Key & Metrics Implemented
The following key business metrics were calculated using DAX:

Total Sales

Total Profit

Profit Margin (%)

Average Order Value (AOV)

Product Count

Sales Year‑to‑Date (YTD)

Sales Quarter‑to‑Date (QTD)

Previous Year Sales (PLY)

Same Period Last Year (SPLY)

Sales Year‑on‑Year (YoY)

Profit Year‑on‑Year (YoY)

Sales Last Month

These metrics enable accurate performance comparison across different time periods.


## 🗓Time Intelligence & Data Modeling

A custom calendar (date) table was created and marked as a date table to support advanced time‑based analysis, including:

Year, Quarter, and Month

YTD and QTD calculations

YoY and SPLY comparisons

Trend analysis over time


## 📊 Dashboard Features
* Sales and profit trends over time

* Top 5 and Bottom 5 products by revenue

* Product category contribution analysis

* Regional sales performance using map visuals

* Weekday vs Weekend sales comparison

* Interactive slicers for:Year, Month, Product Name, Product Category, Sales Channel, Zone
  

## 🔍Insights

1. **Sales Are Concentrated in a Few Products**
Analysis shows that a small group of products contributes a large percentage of total sales revenue. This indicates a classic Pareto (80/20) pattern, where top-performing products drive overall performance.


2. **Weekend Sales Outperform Weekday Sales**
Sales volume and revenue are consistently higher on weekdays compared to weekends, suggesting stronger customer purchase behavior during working days.


3. **Regional Performance Varies Significantly**
Certain regions/zones generate higher sales and profit than others, highlighting uneven market penetration and potential growth opportunities in underperforming regions.


4. **Seasonal Trends Impact Sales and Profit**
Time-based analysis reveals noticeable peaks and dips in sales across different months and quarters, indicating seasonality effects on customer demand.


5. **Some Products Generate High Sales but Low Profit**
While some products perform well in terms of revenue, their profit margins are relatively low, suggesting high discounting or cost-related issues.


6. **Year-on-Year Growth Is Inconsistent**
YoY and SPLY comparisons show that growth is not uniform across periods, signaling potential issues with product lifecycle, pricing strategy, or market demand.



## ✅Recommendations

1. **Prioritize High-Performing Products**
    Focus inventory planning, marketing, and promotions on top-selling and high-margin products
    Ensure consistent stock availability for these products to avoid lost sales

2. **Improve Performance of Low-Performing Products**
     Review pricing and discount strategies for products with low sales or margins
     Consider bundling slow-moving products with top sellers
     Discontinue consistently underperforming products where necessary

3. **Leverage Weekdays Sales Behavior**
   Schedule promotions, flash sales, and marketing campaigns on weekdays
   Increase staffing and inventory availability during high-demand periods

4. **Target Underperforming Regions**
   Introduce region-specific promotions and pricing strategies
   Investigate distribution or supply chain challenges in low-performing zones

5. **Optimize Discount and Pricing Strategy**
   Reduce excessive discounting on products with low profit margins
   Focus discounts on products that increase overall profitability rather than just sales volume

6. **Use Seasonal Trends for Forecasting**
   Align inventory and procurement planning with seasonal demand patterns
   Prepare marketing campaigns ahead of peak sales periods
   
Implementation of these recommendations can Increase overall profitability, Improve inventory efficiency, Enhance regional market performance and Support proactive, data-driven decision-making


## 🛠Tools & Skills Demonstrated
* Power BI – Data modeling, visualization, and reporting
* DAX – KPI creation and time intelligence
* Data Analysis – Trend analysis, performance comparison
* Business Intelligence – Translating data into insights
* Excel – Data sourcing and preparation

  
## 📂File Included
powerbi Electronic_Sales_dashboard.png / [`Electronic_Dasboard.png`](Electronic_Dasboard.png) 


├──  Electronic_Sales_dataset.xlsx

│        └── data/[`Electronic_Sales.xlsx`](Electronic_Sales.xlsx) 

│ 

├── Electronic_Sales_dashboard.pbix


│   └── dashboard/[`Electronic_Sales_Dashboard.pbix`](Electronic_Sales_Dashboard.pbix)

│


├── images.png


│   └── Images/[`Product_Category_by_Quantity.png`](Product_Category_by_Quantity.png) / [`Regional_Map.png`](Regional_Map.png) / [`Sales_&_Profit_Trends.png`](Sales_&_Profit_Trends.png) / [`Top_&_Buttom_5_Product.png`](Top_&_Buttom_5_Product.png) / [`Total_Sales_&_Profit_Generated_by_Channels.png`](Total_Sales_&_Profit_Generated_by_Channels.png) / [`Weekday_Vs_Weekend_Sales.png`](Weekday_Vs_Weekend_Sales.png)

│

├── Insight.md

│     └── Insights/ [`Insights.md`](Insights.md) 


└── README.md / [`README.md`](README.md) 




## How to Use
1. Download the .pbix file from the dashboard folder [`Electronic_Sales_Dashboard.pbix`](Electronic_Sales_Dashboard.pbix)
2. Open with Power BI Desktop [Power BI Desktop](https://powerbi.microsoft.com/).
3.  Use slicers to explore insights across different dimensions


## 👤 Author
Afolakemi Olalekan
<table>
  <tbody>
    <tr>
<td>📧</td>
      <td><a href="mailtoAfolakemiayomiposi@gmail.com">Afolakemiayomiposi@gmail.com</a></td>
    </tr>
    <tr>
 <td>🌐</td>
      <td><a href="https://linkedin.com/in/afolakemi-olalekan-145174253">My LinkedIn Profile</a></td>
    </tr>
    <tr>  
<td>💻</td>
      <td><a href="https://github.com/Olalekan4545">My GitHub profile</a></td>
    </tr>
    <tr>     
