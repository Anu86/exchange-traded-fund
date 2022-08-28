# exchange-traded-fund

ETF based on the data in the database. 
Use sqlalchemy to query db and calculate cumulative returns for GOST, GS, PYPL, and SQ.

## Implementation
Fintech ETF that consists of four stocks: GOST, GS, PYPL, and SQ. Each stock has its own table in the etf.db database

1. Analyze a single asset in the ETF
    a. Read market data from database 
    b. Verify data in dataframe
    c. Display hvplot visualization for daily returns

2. Optimize data access with Advanced SQL queries
   a. Query for closing price  higher than 200.0.
   b. Find top 10 daily returns by sorting data by “daily_returns", order by  desc and limit to top 10

3. Analyze the ETF portfolio
    a.  Join each table in the portfolio into a single DataFrame
    b.  Find averages the “daily_returns” columns for all four assets
    c. Display the annualized return value of the ETF portfolio
    d. Calculate cumulative returns of the ETF portfolio
    e. plot using hvplot with time as x-axis 
    
4. Conclusion 
- Note SQ daily returns grew higher while GDOT plunged in 2019 & 2020
