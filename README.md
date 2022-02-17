# Whale Portfolio Analysis

### Prepare the Data

First, read and cleaned several CSV files for analysis. The CSV files include whale portfolio returns, algorithmic trading portfolio returns, and S&P 500 historical prices. Used the [Whale Analysis Starter Code](Starter_Code/whale_analysis.ipynb) to complete the following steps:

1. Used Pandas to read the following CSV files as a DataFrame. 

    * `whale_returns.csv`: Contains returns of some famous "whale" investors' portfolios.

    * `algo_returns.csv`: Contains returns from the in-house trading algorithms from Harold's company.

    * `sp500_history.csv`: Contains historical closing prices of the S&P 500 Index.

2. Detect and removed null values.

3. If any columns have dollar signs or characters other than numeric values, removed those characters and converted the data types as needed.

4. The whale portfolios and algorithmic portfolio CSV files contain daily returns, but the S&P 500 CSV file contains closing prices. Converted the S&P 500 closing prices to daily returns.

5. Joined `Whale Returns`, `Algorithmic Returns`, and the `S&P 500 Returns` into a single DataFrame with columns for each portfolio's returns.

    ![returns-dataframe.png](Images/returns-dataframe.png)

### Conduct Quantitative Analysis

Analyzed the data to see if any of the portfolios outperform the stock market (i.e., the S&P 500).

#### Performance Analysis

1. Calculated and plot daily returns of all portfolios.

2. Calculated and plot cumulative returns for all portfolios.

#### Risk Analysis

1. Created a box plot for each of the returns. 

2. Calculated the standard deviation for each portfolio. 

3. Determined which portfolios are riskier than the S&P 500.

4. Calculated the Annualized Standard Deviation.

#### Rolling Statistics

1. Calculated and plotted the rolling standard deviation for all portfolios using a 21-day window.

2. Calculated and plottted the correlation between each stock to determine which portfolios may mimick the S&P 500.

3. Chose one portfolio, then calculated and plot the 60-day rolling beta between it and the S&P 500.

#### Rolling Statistics Challenge: Exponentially Weighted Average

An alternative method to calculate a rolling window is to take the exponentially weighted moving average. This is like a moving window average, but it assigns greater importance to more recent observations. Calculated the [`ewm`](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.ewm.html) with a 21-day half-life.

### Sharpe Ratios

Investment managers and their institutional investors look at the return-to-risk ratio, not just the returns. After all, if you have two portfolios that each offer a 10% return, yet one is lower risk, you would invest in the lower-risk portfolio, right?

Using the daily returns, Visualize the Sharpe ratios using a bar plot.


### Create a Custom Portfolio


2. Downloaded the data as CSV files and calculate the portfolio returns.

3. Calculated the weighted returns for my portfolio, assuming equal number of shares per stock.

4. Add my portfolio returns to the DataFrame with the other portfolios.

5. Ran the following analyses:

    * Annualized Standard Deviation.
    * plot rolling `std` with a 21-day window.
    * Calculate and plot the correlation.
    * Calculate and plot beta for your portfolio compared to the S&P 60 TSX.
    * Calculate the Sharpe ratios and generate a bar plot.

