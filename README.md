## Sales Insights Data Analysis Project
#### Purpose
To unlock sales insights that are not visible before for sales team for decision support & automate them to reduced manual time spent in data gathering.
#### End Results
An automated dashboard providing quick & latest sales insights in order to suppoer data driven decision makeing.
#### Success Criteria
- Dashboard(s) uncovering sales order insights with latest data available.
- Sales team able to take better decisions & provide cost savings of total spend.
- Sales Analysts stop data gathering manually in order to save their business time and reinvest   it value added activity.


## Data Analysis Using SQL

1. Show all customer records

    `SELECT * FROM customers;`

1. Show total number of customers

    `SELECT count(*) FROM customers;`

2. Show transactions for Chennai market (market code for chennai is Mark001

    `SELECT * FROM transactions where market_code='Mark001';`

3. Show distrinct product codes that were sold in chennai

    `SELECT distinct product_code FROM transactions 
    where market_code='Mark001';`

4. Show transactions where currency is US dollars

    `SELECT * from transactions 
    where currency="USD"`

5. Show transactions in 2020 join by date table

    `SELECT t.*, d.* FROM transactions t
    INNER JOIN date d ON t.order_date = d.date
    where d.year=2020;`

6. Show total revenue in year 2020,

    `SELECT SUM(t.sales_amount) FROM transactions t
    INNER JOIN date d ON t.order_date = d.date
    where d.year=2020;`
	
7. Show total revenue in year 2020, January Month,

    `SELECT SUM(t.sales_amount) FROM transactions t
    INNER JOIN date d ON t.order_date = d.date
    where d.year=2020 and and d.month_name="January";`

8. Show total revenue in year 2020 in Chennai

    `SELECT SUM(transactions.sales_amount) FROM transactions t
    INNER JOIN date d ON t.order_date = d.date
    where d.year=2020 and t.market_code="Mark001";`
