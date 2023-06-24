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
    The data used was gotten from the AdventureWorks database by connecting my Power BI to an SQL server(my local machine in this instance). only four tables were used, all from the production
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
