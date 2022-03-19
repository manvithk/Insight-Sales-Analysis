## Sales Insights Data Analysis Project 
### AIMS GRID
1. <b>Purpose</b> <i>(Why are we doing this? (in order to ...)</i>
   <p>To unlock Sales Insight that is not visible for before the Sales Team for decision support & automate them to reduced manual time spent in data gathering </p>
2. <b>Stakeholders</b> <i> (For whom are we doing this?) </i>
   <p> Sales Director, Marketing Team, Custom Service Team, Data & Analytics Team, IT team  </p>
3. <b>End Result</b> <i> (What do we need to achieve in the time) </i>
   <p> An automated Dashboard providing quick & latest insights in order to support data driven decision making </p>
4. <b>Success Criteria</b> <i> (Against which criteria will the result be measured?) </i>
   <p> a) Dashboard(s) uncovering sales order insights with latest data available </p>
   <p> b) Sales Team able to take better decisions & prove 10% cost savings of total spend </p>   
   <p> c) Sales Analyst stop data gathering manually in order to save 20% of business time and reinvest it in value added 
	  activity </p>   
      
### DATA ANALYSIS USING SQL

1. Show all customer records

    `SELECT * FROM customers;`

2. Show total number of customers

    `SELECT count(*) FROM customers;`

3. Show transactions for Chennai market (market code for chennai is Mark001)

    `SELECT * FROM transactions where market_code='Mark001';`

4. Show distrinct product codes that were sold in chennai

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

5. Show transactions where currency is US dollars

    `SELECT * from transactions where currency="USD":`

6. Show transactions in 2020 join by date table

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

7. Show total revenue in year 2020,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and (transactions.currency="INR" or          transactions.currency="USD");`
	
8. Show total revenue in year 2020, January Month,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and         (transactions.currency="INR" or transactions.currency="USD");`

9. Show total revenue in year 2020 in Chennai

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020
     and transactions.market_code="Mark001";`

### SALES INSIGHTS DASHBOARD URL
 
    <p>https://public.tableau.com/app/profile/manvith.k/viz/SalesAnalysis_16457932371540/Dashboard-ProfitAnalysis#1</p>

