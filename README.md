# classic-cars-sales-dashboard

## CAPSTONE POWER BI PROJECT Problem Statement:
A small company Axon, which is a retailer selling classic cars, is facing issues in managing and analyzing their sales data. The sales team is struggling to make sense of the data and they do not have a centralized system to manage and analyze the data. The management is unable to get accurate and up-to-date sales reports, which is affecting the decision-making process.
To address this issue, the company has decided to implement a Business Intelligence (Bl) tool that can help them manage and analyze their sales data effectively. They have shortlisted Microsoft Power BI and SQL as the Bl tools for this project.
## Task: 
 The goal of the capstone project is to design and implement a Bl solution using Power BI and SQL that can help the company manage and analyze their sales data effectively. 
## EER DIAGRAM: 
 
 ![EER DIAGRAM](https://github.com/Sonus5418/classic-cars-sales-dashboard/blob/main/eer%20%20diagram.jpg)


 
## Tools Used:
-My Sql
-Pivot Table and charts
-Power BI
-Power Query
-Dax Query
-Canva
## Classic Model Car’s Dashboard : 
         Sales View – To display the top-performing and bottom-performing Products with different key metrics. 
         Employee View – This includes the integrated view of key insights for Employees.
         Key Insights – To display the findings or key insights we learnt from analysis.
        

## SANPSHOTS:
![SALES VIEW](https://github.com/Sonus5418/classic-cars-sales-dashboard/blob/main/classic%20cars%20dashboards/classic%20car%201.jpg
## Project Execution
Step – 1 The first step was to load the (mysqlsampledatabase)data into MySQL Database and connect it to the Power BI.

Step – 2 Review the Database relationship created by Power BI.

Step – 3 Data validation using some tables in Power BI and matching the values with the data provided.

Step – 4 Transform and clean the Data as needed using Power Query Editor within Power BI Desktop. This involves renaming columns, removing null values , removing unnecessary column like: image.

Step – 5 Created columns in Power Query like Employee that concatenate the firstName and lastName of Employee

Step – 7 Created calculated columns using DAX formulas (Formulas listed at the bottom). After the columns were created, verified them in either MySQL or Excel file.

Step – 8 Build visualization by dragging fields from your data tables onto the canvas in Power BI Desktop.

## Key Findings:
· USA, Spain and France are the three countries, the most of the sales comes from over the years.

· The Sales was in the Peak in November may because holiday season and end-of-year festivities (like: Thanksgiving , Black Friday etc.). Many individuals may choose to purchase classic cars as gifts for 
  themselves or loved ones during this time, leading to increased sales.
  
· The Total Orders placed by customers are 2996 and the Total Sales of the Company is $9.6 Million and made profit of $ 3.8 Million.
  
· Total Distinct customer are 94. Most of the Customers are from USA.

· The Total employee count of the company is 22.

· Total no. of Products are 110. Most of the Product is Classic Cars.

· Classic Cars, Vintage Cars and Motor Cycles are the three product Categories earned more profit among the categories.

· 1992 Ferrari 360 Spider Red was the Top most selling car following by 2001 Ferrari Enzo and 1952 Alpine Renault 1300.

· Euro+ Shopping Channel, Mini Gifts Distribution Ltd., and Australian Collectors Co., are the 3 top customers bought products in high numbers.

· Gerald Hernandez, Leslie Jennings and Pamela Castillo are the three sales representatives who achieved better sales target compare to others.

· Barry Jones and Pamela Castillo have most no. of Customers.

## Measures Created(DAX):
1.	Total Sales	= SUMX('classicmodels orderdetails','classicmodels orderdetails'[quantityOrdered] * 'classicmodels orderdetails'[priceEach])

2.	Total Profit	= [Total Sales] - SUMX('classicmodels orderdetails', RELATED('classicmodels products'[buyPrice]) * 'classicmodels orderdetails'[quantityOrdered])

3.	Total no. of Product= countrows('classicmodels products')

4.	Total no. of Orders 	= COUNTROWS('classicmodels orderdetails')

5.	Total Employees 	= DISTINCTCOUNT('classicmodels employees'[Employee])

6.	Total Customers 	= DISTINCTCOUNT('classicmodels customers'[customerNumber])

7.	sum of quantity ordered 	= sum('classicmodels orderdetails'[quantityOrdered])

8.	Last year sales	= CALCULATE(SUMX('classicmodels orderdetails','classicmodels orderdetails'[quantityOrdered] * 'classicmodels orderdetails'[priceEach]),
                 SAMEPERIODLASTYEAR('classicmodels orders'[orderDate].[Date]))



