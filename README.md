### Overview
#### This project aims to collect textual data from different sources, perform sentiment analysis on the data , calculate various sentiment scores and finally predict the labels for different stocks (negative and positive depending on when the stock price has decreased or increased over the month).
#### Stocks taken for the study: Nvidia, Microsoft and Tesla. 
#### Time period: 2014-2024
#### Sources for data : NYT archives (for news headlines) and the Edgar webiste (for SEC filings). The stock prices have been taken from yahoo finance.
#### Weightage: News headlines have been given a weight of 0.6 , quarterly SEC filings a weight of 0.25 and annual SEC filings a weight of 0.15. The weights have been given in the order to sensitivity of the stock prices to these information.
#### Label: -1 if open price > close price and 1 if open price < close price.
#### Model used: CatBoost which gives ROC-AUC value of 0.61.
#### Following is an analysis of buy and sell points with their respective probabilities:-
![stock_analysis](https://github.com/Ashita17/Stock-Sentiment-Analysis-using-ML/assets/101327935/f0ac77be-b9e9-45f1-89f4-b845bf051a71)
#### Metrics obtained are: 
1. Total returns: 240.41 %
2. Sharpe Ratio: 5.19
3. Number of Trades: -107.79 ( Model is giving absurd value for this :|, clearly a drawback )
4. Win Ratio: 64.18%
