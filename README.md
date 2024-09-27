Sales Insights - Data Analysis using Tableau & SQL  
I am sharing India based Hardware company Sales Insights - A Data Analysis Project performed on Tableau & SQL.
About Project 👨💻
•	Performed India based hardware company sales insights - A Data Analysis project.
•	Developed ETL mappings using SQL to extract the data from unstructured data and transformed it to the staging area to conduct data cleaning and design star schema data model on Tableau.
•	Developed a Tableau dashboard to perform analysis, producing quantitative visualizations in Tableau to draw valuable insights based on different parameters affecting the company performance year on year and further provide business solutions.
Technologies used ⚙️
•	Advance Excel  
•	MySQL   | SQL Server  
•	Tableau   | Power BI  
•	Statistics  
Project - India based Hardware company Sales Insights - Data Analysis performed on Tableau & SQL
Problem Statements
Sales director wants to know the performance of the company in various Indian states & accordingly provide some discount.
•	Q1. Revenue breakdown by cities.
•	Q2. Revenue brekdown by years & months.
•	Q3. Top 5 customers by revenue & sales quantity.
•	Q4. Top 5 Products by revenue.
•	Q5. Net Profit & Profit Margin by Market
Data Analysis - Approach
 
Setup Process
Step 1: Download file: db_dump.sql or db_dump.xlsx
Step 2: Import it in MySql do ETL(Extract, Transform, Load) if required
Step 3: Download Tableau Public  to perform Data Analysis
Step 4: Connect Tableau with MySql database or Excel database
Step 5: Save the file as (.twb or .twbx)
Data Analysis Using SQL
1.	Show all customer records
SELECT * FROM customers;
2.	Show total number of customers
SELECT count(*) FROM customers;
3.	Show transactions for Chennai market (market code for chennai is Mark001)
SELECT * FROM transactions where market_code='Mark001';
4.	Show distrinct product codes that were sold in chennai.
SELECT distinct product_code FROM transactions where market_code='Mark001';
5.	Show transactions where currency is US dollars.
SELECT * from transactions where currency="USD"
6.	Show transactions in 2020 join by date table.
SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;
7.	Show total revenue in year 2020.
SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";
8.	Show total revenue in year 2020, January Month.
SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");
9.	Show total revenue in year 2020 in Chennai.
SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020and transactions.market_code="Mark001";
Data Analysis Using Tableau
Tableau Public Dashboards: Revenue & Profit Analysis  
Creating Star Schema in Tableau
 
Tableau Dashboard - Revenue Analysis
 
Tableau Dashboard - Profit Analysis
 

