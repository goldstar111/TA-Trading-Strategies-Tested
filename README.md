# TA-Trading-Strategies-Tested

<b> <u> MAIN FILE: PTP_Signals.ipynb </b> </u>

Several trading strategies are programmed and then statistically backtested, through Monte Carlo and Bootstrap simulation methods.

Market Timing Portfolio Performance using Technical Indicators RSI, MACD and TD DeMark indicators.

We examine the performance of a portfolio of 27 stocks, selected from the top traded S&P 500 index, using technical indicators RSI, MACD and TD DeMark (Setup and Countdown) across 5 years of data. Market timing is of essence, as the point of entering a position is indicated by the signals generated by these technical, and subsequent fixed-period returns are backtested and compared with a random buy-and-hold strategy, to indicate excess returns. The portfolio is then optimized for beta neutrality and tested for 1 year of out-of-sample period. The results have shown to be statistically insignificant, as excess returns have often been outperformed by random strategies. 

<b>Keywords:</b>  Technical Analysis, Portfolio Optimization, Back-testing, Beta-Neutral, Financial Markets, S&P 500, Market Timing

<b> Instructions on how to use the code/files: </b>

1.	There are 2 excel files that are read into the code: 
a.	Daily Prices (DataTwentyEight.xlsx) for signal generation 
b.	Daily Returns Matrix (PTP Returns.csv) for Portfolio Optimization
2.	The Signal Generation Code can be found on the Python file PTP_Signals.py (or .ipynb if that is preferred). This code generates the following files:
a.	AllSignals.xlsx with the RSI, MACD and DeMark Buy Signals added (as 1 or 0)
b.	PTP_results_demark.csv, with the calculated returns distributions for all strategies. This Excel was later modified to generate charts that are used in the paper.
3.	Since Python doesn’t have a Quadratic Programming element to it, the TE, IR calculation was done on R. The R file is named ‘Optimization and Tracking Error.r’. This file needs the following files to be present in the directory:
a.	A_T.csv 
b.	Mean.csv
c.	Beta.csv
d.	Cov_Mat.csv
All these files are generated by the other Python File, PTP_Computations.py. (or .ipynb if that is preferred)
