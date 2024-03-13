# Classic Cars Sales Dashboard

## CAPSTONE POWER BI PROJECT

### Problem Statement:
A small company named Axon, which is a retailer selling classic cars, is facing issues in managing and analyzing their sales data. The sales team is struggling to make sense of the data, and they do not have a centralized system to manage and analyze the data. The management is unable to get accurate and up-to-date sales reports, which is affecting the decision-making process.

To address this issue, the company has decided to implement a Business Intelligence (BI) tool that can help them manage and analyze their sales data effectively. They have shortlisted Microsoft Power BI and SQL as the BI tools for this project.

### Task:
The goal of the capstone project is to design and implement a BI solution using Power BI and SQL that can help the company manage and analyze their sales data effectively.

## EER DIAGRAM:

![EER DIAGRAM](https://github.com/Sonus5418/classic-cars-sales-dashboard/blob/main/eer%20%20diagram.jpg)

## Tools Used:
- MySQL
- Pivot Tables and Charts
- Power BI
- Power Query
- DAX Query
- Canva

## :bar_chart: Classic Model Car’s Dashboard:
- **Sales View:** Display the top-performing and bottom-performing products with different key metrics.
- **Employee View:** Integrated view of key insights for employees.
- **Key Insights:** Display the findings or key insights learned from the analysis.

## :camera_flash: SANPSHOTS:

![SALES VIEW](https://github.com/Sonus5418/classic-cars-sales-dashboard/blob/main/classic%20cars%20dashboards/classic%20car%201.jpg)
![EMPLOYEE VIEW](https://github.com/Sonus5418/classic-cars-sales-dashboard/blob/main/classic%20cars%20dashboards/classic%20car%202.jpg)
![KEY INSIGHTS](https://github.com/Sonus5418/classic-cars-sales-dashboard/blob/main/classic%20cars%20dashboards/classic%20car%203.jpg)

## Project Execution:
1. **Prepare Import:** Load the `mysqlsampledatabase` data into the MySQL Database and connect it to Power BI.
2. **Review Database Relationship:** Review the database relationship created by Power BI.
3. **Data Validation:** Validate the data using tables in Power BI and match the values with the provided data.
4. **Data Transformation:** Transform and clean the data as needed using Power Query Editor within Power BI Desktop. This involves renaming columns, removing null values, and removing unnecessary columns like images.
5. **Column Creation:** Create columns in Power Query, like the Employee column, that concatenates the firstName and lastName of the employee.
6. **Calculated Columns:** Create calculated columns using DAX formulas. Verify them in either MySQL or Excel files.
7. **Visualization:** Build visualizations by dragging fields from data tables onto the canvas in Power BI Desktop.

## Key Findings:
- The top three countries with the most sales are USA, Spain, and France.
- Sales peak in November, possibly due to holiday season festivities.
- Total orders placed by customers are 2996, with total sales of $9.6 million and a profit of $3.8 million.
- There are 94 distinct customers, most of whom are from the USA.
- The company has 22 employees.
- There are 110 products in total, with Classic Cars being the most common.
- Classic Cars, Vintage Cars, and Motorcycles are the most profitable product categories.
- The top-selling cars are 1992 Ferrari 360 Spider Red, 2001 Ferrari Enzo, and 1952 Alpine Renault 1300.
- Euro+ Shopping Channel, Mini Gifts Distribution Ltd., and Australian Collectors Co. are the top three customers.
- Gerald Hernandez, Leslie Jennings, and Pamela Castillo are the top-performing sales representatives.
- Barry Jones and Pamela Castillo have the most customers.

## Measures Created(DAX):
1.	**Total Sales**	= SUMX('classicmodels orderdetails','classicmodels orderdetails'[quantityOrdered] * 'classicmodels orderdetails'[priceEach])

2.	**Total Profit**	          = [Total Sales] - SUMX('classicmodels orderdetails', RELATED('classicmodels products'[buyPrice]) * 'classicmodels orderdetails'[quantityOrdered])

3.	**Total no. of Product**    = countrows('classicmodels products')

4.	**Total no. of Orders**     = COUNTROWS('classicmodels orderdetails')

5.	**Total Employees** 	      = DISTINCTCOUNT('classicmodels employees'[Employee])

6.	**Total Customers** 	      = DISTINCTCOUNT('classicmodels customers'[customerNumber])

7.	**sum of quantity ordered** = sum('classicmodels orderdetails'[quantityOrdered])

8.	**Last year sales**	        = CALCULATE(SUMX('classicmodels orderdetails','classicmodels orderdetails'[quantityOrdered] * 'classicmodels orderdetails'[priceEach]),
                                  SAMEPERIODLASTYEAR('classicmodels orders'[orderDate].[Date]))

## Conclusion:
The Classic Cars Sales Dashboard provides valuable insights into the company's sales performance, customer behavior, and product trends. By leveraging Power BI and SQL, Axon can make data-driven decisions to improve sales strategies and enhance customer satisfaction.

For more detailed insights, refer to the Power BI reports and analysis provided in the dashboard .

---




