Objective of the Sales Dashboard / Business Problem
--------------------------------------------------
The objective of the report is to analyze and present comprehensive insights into sales, profit, orders, profit margin, and various comparisons. It aims to provide a clear understanding of key performance indicators and trends using Power BI. The report objectives can be summarized as follows:
1.	Calculate Total Sales: Calculate and display the total sales value for the selected period, allowing users to understand the overall revenue generated.
2.	Calculate Profit: Calculate and visualize the total profit achieved based on the sales data, providing insights into the financial performance.
3.	Analyze Orders: Analyze the number of orders placed during the selected period, helping to identify sales patterns and order trends.
4.	Calculate Profit Margin: Calculate and visualize the profit margin percentage, enabling users to assess the profitability of products or services.
5.	Compare Sales by Product with Previous Year: Compare sales performance for each product between the selected period and the previous year, highlighting growth or decline in sales.
6.	Compare Sales by Months with Previous Year: Compare sales performance across different months between the selected period and the previous year, identifying regions with significant changes.
7.	Display Top 5 Cities: Present a visualization showcasing the top 5 cities based on sales, allowing users to quickly identify the most lucrative locations.
8.	Compare Profit by Channel with Previous Year: Compare profit generated by each channel between the selected period and the previous year, indicating improvements or challenges in profitability.
9.	Analyze Sales by Customer and Compare with Previous Year: Analyze sales data by customer, highlighting the performance of individual customers and comparing it to the previous year.
10.	Create Slicers for Date, City, Product, and Channel: Enable users to interact with the data by providing slicers for selecting specific dates, cities, products, and channels, allowing for dynamic filtering and personalized analysis.


Steps to follow for an end-to-end Power BI Project
-----------------------------------------------------
1) Gather Data
Collect the necessary data for your project. This could include data from various sources such as databases, spreadsheets, or web services. Ensure the data is accurate and relevant to your objective. Download the Download section at the end of the page.
2) Power Querry – Data Extract, Transform & Load
Power Query Editor in Power BI is a powerful tool for data cleaning and transformation. We will use it Clean and transform the data to make it suitable for analysis. This may involve removing duplicates, handling missing values, merging datasets, or creating calculated columns.
3) Create a Date Table
To work with Data Analysis Expressions (DAX) time intelligence functions, there’s a prerequisite model requirement: You must have at least one data table in your model.
Note: Turn off Auto Date/Time for new files in Power BI Options Setting, as this will help to improve performance of your report.
4) Create Data Model in Power BI Desktop
Design and create a data model that represents the relationships between different tables in your data. Establish proper relationships, define keys, and establish hierarchies if needed. This step is crucial for accurate analysis and visualization
5) Develop Reports in Power BI Desktop
Use the Power BI Desktop application to create reports based on your data model. Add visualizations such as charts, tables, and maps to represent the data effectively. Apply filters, slicers, and drill-through functionalities to allow users to interact with the data.
•	Create Report Background in PowerPoint
•	Create Slicers – Date, City, Product, and Channel
•	Create Dax measures
•	Create Visuals:
1) Sales By Product and Comparing it with last year’s Sales.
2) Sales By Month and Comparing it with last year’s Sales.
3) Sales of top 5 Cities
4) Compare Profit by channel with Previous year’s Profit
5) Sales By Customer and Comparing it with last year’s Sales
6) Create Cards for Sales, Profit, Profit Margin & Product Sold


6) Implementing DAX Calculations
We will use Data Analysis Expressions (DAX) to create calculated columns, measures, and calculated tables to perform complex calculations and aggregations. DAX is a powerful formula language that allows you to manipulate data within Power BI.
//Measures Total Sales
Sales = SUM(Sales_Data[Sales])

//Measures Previous Year Toal Sales
Sales PY = CALCULATE([Sales], SAMEPERIODLASTYEAR(DateTable[Date]))

//Diffrence Between Current Year Sales & Previous Year Sales
Sales vs PY = [Sales] - [Sales PY]

//Percentage Increase or Decrease in sales year on year (YOY%)
Sales vs py % = DIVIDE([Sales vs PY],[Sales],0)
>> Products Sold = SUM(Sales_Data[Order Quantity])
>> Profit = SUM(Sales_Data[Profit]) 
>> Profit LY = CALCULATE([Profit], SAMEPERIODLASTYEAR(DateTable[Date]))
>> Profit Vs LY = [Profit]- [Profit LY]
>> Profit vs LY % = [Profit Vs LY]/[Profit]
>> Profit Margin = DIVIDE([Profit],[Sales],0)
>> Total Cost = SUM(Sales_Data[Total Cost])

Conclusion of Power BI Sales Dashboard Project
---------------------------------------------
Conclusion for the year 2019:
•	Sales decreased by more than 10%
•	There is a drop in sales of all the top 7 Products
•	4 Customers are leading to a drop in sales
•	The profit margin in the Export channel is higher

