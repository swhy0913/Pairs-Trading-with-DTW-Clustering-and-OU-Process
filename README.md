# Pairs-Trading-with-DTW-Clustering-and-OU-Process
#### This project aims to implement a pairs trading strategy on Hong Kong equities using Dynamic Time Warping (DTW) and Clustering algorithms. The strategy was backtested using a Z-Score based trading strategy and the Ornstein-Uhlenbeck process trading strategy. Pairs trading is a technique that capitalizes on the historical correlation between the price movements of two stocks. This strategy bets that stocks which have deviated in the short term will revert to their long-term mean equilibrium, based on their historical correlated price movement. The strategy involves taking a long position in one stock and a short position in the other when a significant price deviation is identified.

#### Initially, we implemented the dynamic time warping technique to filter stock price time series that correlate with each other. This was achieved by discretizing individual stock price time sequences and using the DTW algorithm to search for the most optimal pairs. Subsequently, unsupervised machine learning clustering algorithms were applied to verify the legitimacy of the pairs identified by DTW, serving as a secondary check. A tertiary cross-check with Bloomberg industry GICS (Global Industry Classification Standard) categorization was employed to finalize our verification. In total, we identified 38 pairs from a selection of 100 stocks.

#### For the trading strategy, we tested our models on 5 years of data, encompassing 1,131 trading days from 22 May 2018 to 22 May 2023, and employed an 80:20 train-test split. We applied a Z-score based strategy and compared it to an Ornstein-Uhlenbeck process trading strategy (S-score), as proposed by Marco Avellaneda & Jeong-Hyun Lee (2010), to generate our trading signals.

#### The results showed that, without a stop-loss implemented, the Z-Score based strategy achieved the highest annualized returns of 116%, with a Sharpe Ratio of 1.27 and a maximum drawdown of 81%. In contrast, the S-score based strategy yielded a Sharpe Ratio of 1.32 and a maximum drawdown of 7.22%, despite its annualized returns being only 24%. Our findings conclude that the S-score strategy, although it generates fewer trading signals than the Z-score based strategy, is a less volatile approach.

## Test Results Conclusion:
![In-Sample Test Results](https://github.com/swhy0913/Pairs-Trading-with-DTW-Clustering-and-OU-Process/assets/19575677/53519e74-74a5-4d3f-9798-0a73f3c320a5)

![OOS Test Results](https://github.com/swhy0913/Pairs-Trading-with-DTW-Clustering-and-OU-Process/assets/19575677/011ea8ac-906e-4351-898d-b0c769bbe8d7)

![OOS Stoploss Test Results](https://github.com/swhy0913/Pairs-Trading-with-DTW-Clustering-and-OU-Process/assets/19575677/61e54f7d-6ec1-4bb1-9845-8df5a7620b23)

![OOS Results Table](https://github.com/swhy0913/Pairs-Trading-with-DTW-Clustering-and-OU-Process/assets/19575677/a269b7e6-34ce-4bf0-a1e8-6086f17bbac8)
