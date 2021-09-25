# Sales-Insight-Project
In this project, I will do some analysis with MySQL and Tableau. 

Data Analysis Using SQL

1. Accessing created salesdatabase in MySQL

Use Salesdatabase;

2. Try to see what tables are included in the salesdatabase

Show tables;

3. Show all customer records

SELECT * FROM customers;

4. Show total number of customers

SELECT count(*) FROM customers;

5. Show transactions for Chennai market (market code for chennai is Mark001)

SELECT * FROM transactions where market_code='Mark001';

6. Show unique product codes that were sold in chennai

SELECT distinct product_code FROM transactions where market_code='Mark001';

7. Show transactions where currency is US dollars

SELECT * from transactions where currency="USD"

8. Show transactions in 2020 join by date table

SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;

9. Show total revenue in year 2020,

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";

10. Show total revenue in year 2020, January Month,

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and date.month_name="January";

11. Show total revenue in year 2020 in Chennai

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark001";
