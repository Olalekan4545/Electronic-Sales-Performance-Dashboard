## Description

This document contains the DAX measures used in the Electronics Sales Dashboard. It explains the business logic and time-intelligence calculations applied to derive key performance indicators such as Total Sales, Profit, YTD, QTD, YoY, SPLY, and other comparative metrics. These measures enable accurate period-over-period analysis and support data-driven decision-making.

The Dax Measure i calculated includes:

1. ### Date Table (Calendar Table)
      I calculate this dax to enable accurate time-intelligence calculations such as YTD, QTD, YoY, and SPLY.


   **DAX Logic:**

   Date_Table = CALENDARAUTO()


   year = YEAR('Date_Table'[Date])


   Month = FORMAT('Date_Table'[Date],"MMMM")


   Month_no = MONTH('Date_Table'[Date])


   Day = FORMAT('Date_Table'[Date], "DDDD")


   Day_no = WEEKDAY('Date_Table'[Date],2)


   Quarter = "Q" & QUARTER('Date_Table'[Date])


   Day_Type = IF(WEEKDAY('Date_Table'[Date],1) >=6,"Weekend","Weekday")




After creating the **Dax Date** , i marked it as a Date table, Then i create a relationship between the electronics dataset and Date table, this lead us to Data Modelling

- A star schema model was used
- A **Many-to-one Relationship** was created from the Elecronic Sales fact table to Date Table


2. ### Base Meaures
  this measure was calculated in order to establish core business metrics that quantify revenue, cost, profitability, order activity, customer purchasing behavior, and        product performance, providing a consistent and reliable foundation for all advanced KPIs and time-intelligence calculations used in the dashboard.
  

  it Includes:
  - Total_Sales = [Quantity] * [Unit Price]
  - Total_Cost = [Quantity] * [Unit cost]
  - Total_Profit = [Total Sale] - [Total Cost]
  - Total_Quantity = SUM(Sales_Details[Order Qty])
  - Total_Order = DISTINCTCOUNT(Sales_Details[Order ID])
  - Average_Order = DIVIDE([Total_Sales],[Count_of_Order])
  - Count_of_Product = DISTINCTCOUNT(Sales_Details[Product Name])
  - Profit Margin % = DIVIDE([Profit],[Total_Sales])
    
    
3. ### Advanced (Time Intelligence) Measures
   this calculation was perform To enable time-based performance analysis by comparing sales and profit     across different periods, identifying growth trends, seasonality    patterns, and performance changes over time, thereby supporting informed    business decisions and strategic planning.
   
   The Dax calculation Includes:
   - Sales YTD = TOTALYTD(SUM(Sales_Details[Sales]),Sales_Details[Order Date])
   - Sales_QTD = TOTALQTD(SUM(Sales_Details[Sales]),'Sales_Details'[Order Date])
   - Sales_SPLY = CALCULATE([Total_Sales], SAMEPERIODLASTYEAR(Date_Table[Date]))
   - Sales_YOY_Variance = SUM(Sales_Details[Sales]) - [Sales_SPLY]
   - Sales_YOY % = DIVIDE([Sales_YOY_Variance],[Sales_SPLY])
   - Sales_Last_Month = CALCULATE([Total_Sales],PREVIOUSMONTH(Date_Table[Date]))
   - Profit YTD = TOTALYTD([Profit],Date_Table[Date])
   - Profit_QTD = TOTALQTD(SUM(Sales_Details[ Profit ]),'Sales_Details'[Order Date])
   - Profit_SPLY = CALCULATE([Profit], SAMEPERIODLASTYEAR(Date_Table[Date]))
   - Profit_YOY_Variance = SUM(Sales_Details[ Profit ]) - [Profit_SPLY]
   - Profit_YOY % = DIVIDE([Profit_YOY_Variance],[Profit_SPLY])

  ### closing Remark
  All measures in this model are structured using a layered approach, starting with base measures and extending to time-intelligence calculations, to ensure consistency, reusability, and accuracy across all analyses and dashboard visuals.
  







