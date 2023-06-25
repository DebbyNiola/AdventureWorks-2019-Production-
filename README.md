# AdventureWorks 2019 Production Analysis

![](intro_image.jfif)
_ _ _

## Introduction
This project was carried out on Power BI, the aim being to give insight to the producers about their production performance by the products, work order, work order routing and by date.

## Problem Statement
- Create a **Products** dashboard to show production performnce by products,
- Create a **Work Order** dashboard to show production by work order and measure performance,
- Create a **Work Order Routing** dashboard to show routing details and production performance,
- Create a dashboard to show production by date and trend
  
  ## Skills Used
  - Slicers,
  - Measures(Using DAX),
  - Model Relationship,
  - Data cleaning and transformation

    ## Data Sourcing
    The data used was gotten from the AdventureWorks database by connecting my Power BI Desktop to an SQL server(my local machine in this instance). only four tables were used, all under production
    ![](Connect_to_server1.jpeg)
    ![](Connect_to_server2.jpeg)
  - - -
    ## Data Transformation
    Using the power query editor, the data was cleaned.
    - Column headers were renamed using appropriate cases,
    - Data types of some columns were adjusted
    - 
    Within the Power BI itelf, that is after leaving the power query editor, the following were done.
- A date table was created using the 'CALENDARAUTO()' function,
To guage production performance, KPIs were calculated , by creating measures and calculated columns.
- **First Pass Yield** was calculated with a measure by dividing total good products by total quantity produced,
-  **Throughput** was calculated with a measure by dividing total quantity produced by total resource hours invested,
- **Profit** was gottten by subtracting cost price from selling price,
- **Cycle Time** was calculated with a measure by dividing total resource hours by total quantity produced

## Modelling
The tables formed a snowflake schema, as fact table ws connected to dimensions table and there was alo dimension to dimension table relationship.
![](Model_View.jpg)

## Visualizations and Analysis
The report was spread across four tables, all showing production but by different metrics.
The first showed production by products
![](Products_Page.jpg)
We can get the following from above
1. The overall First pass yield at **99.76%** shows that the production process is effective and wasted products are at a minimal.
2. Approximately **59%** of their product had finished production process, while about **41%** haven't.
3. The Throughput of the company at approximately **20** shows that the company makes about 20 products per hour. this is becaus production time was measured in hours.
4. Overall, **BB Ball Bearing** was the most produced item.
- - -
The second paage shows production by workorder
![](Work_Order_Page.jpg)
From above, we can see the following
1. The **Order to Stock quantity** value at **-11k** meaning **-11 Thousand** shows that total production is less than total order by 11 thousand products.
2. The due-to-end date column shows the amount of days between when a product was due and when the product was actually delivered. The negative value shows that the company is lagging behind in meeting up with deadlines.
