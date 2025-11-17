## Sales Data Analysis with SQL and Power BI

### Run Locally

Clone the project

```bash
  git clone https://github.com/dhathriksjuly/Sales-Data-Analysis-using-Power-BI-and-SQL.git
```

Go to the project directory and open ``` .pbix ``` file with Microsoft Power BI Desktop

### Data Analysis Using SQL

1. Show all customer records

    `SELECT * FROM customers;`

1. Show total number of customers

    `SELECT count(*) FROM customers;`

1. Show transactions for Chennai market (market code for chennai is Mark001

    `SELECT * FROM transactions where market_code='Mark001';`

1. Show distrinct product codes that were sold in chennai

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

1. Show transactions where currency is US dollars

    `SELECT * from transactions where currency="USD"`

1. Show transactions in 2020 join by date table

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

1. Show total revenue in year 2020,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
1. Show total revenue in year 2020, January Month,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

1. Show total revenue in year 2020 in Chennai

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020
and transactions.market_code="Mark001";`


Power BI Dashboard Preview
============================

<img width="1003" height="627" alt="image" src="https://github.com/user-attachments/assets/8a736b3a-56ba-4b74-936c-d3ef7db93b90" />
<img width="1007" height="637" alt="image" src="https://github.com/user-attachments/assets/6ddb82bc-7ba2-4c1a-8697-baff109f3952" />
<img width="1005" height="635" alt="image" src="https://github.com/user-attachments/assets/d75f7c5a-60bf-4eb9-8f86-79fb4a6a4435" />




