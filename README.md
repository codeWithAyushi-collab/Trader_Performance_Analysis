Trader Performance Analysis Across Market Sentiments

Author: Ayushi Bhati
 Internship: [Primetrade.ai Data Science internship]
 Date: September 2025
 
1. Project Overview
This project analyzes the relationship between Bitcoin market sentiment (Fear/Greed Index) and trader performance using historical trading data. The goal is to uncover patterns in how traders behave under different sentiment regimes (Fear, Greed, Extreme conditions, Neutral) and identify traders who consistently adapt or show contrarian strength.
Key objectives:
Analyze trader behavior in Fear, Neutral, and Greed market regimes.


Examine correlations between metrics like totalPnL, avgPnL, winRate, tradeCount, and Sharpe ratio.


Identify consistent or contrarian traders for strategy insights.


2. Dataset
Historical Trader Data (Hyperliquid)


Columns: Account, Coin, Execution Price, Size USD, Side, Timestamp, Closed PnL, etc.


~211k trade records.


Fear & Greed Index


Columns: date, value, classification (Extreme Fear, Fear, Neutral, Greed, Extreme Greed). 
~2600 records (daily sentiment)

3. Methodology
Data Preparation


Converted timestamps to datetime, aligned trades with daily sentiment classification.


Merged trader data with sentiment dataset on date.


Feature Engineering & Metrics
 For each trader × sentiment regime:


Total PnL (sum of profits/losses)


Average PnL per trade


Trade Count


Win Rate (% profitable trades)


Sharpe Ratio (risk-adjusted return)


Rank of traders within each sentiment regime by total PnL


Visualization


Boxplot → Distribution of PnL under different sentiment regimes


Barplot → Top 10 traders by PnL (per sentiment regime)


Heatmap → Correlation between performance metrics

4. Key Insights & Conclusions
1. Trader behavior varies with market sentiment
Some traders excel during Fear/Extreme Fear periods — these are contrarian traders, profiting when others panic.


Most traders perform better in Greed/Extreme Greed periods, following herd behavior.


Neutral market periods showed mixed results with no strong bias.


2. Consistency is crucial
Only a small group of traders maintained consistent profitability across multiple market regimes.


Many traders performed well in one sentiment regime but poorly in others.


3. Metrics correlation
totalPnL correlates strongly with avgPnL and winRate — traders with higher win rates tend to earn more.


tradeCount (number of trades) does not guarantee profits — quality of trades matters more than quantity.


Sharpe ratios indicate that some high-PnL traders have unstable returns, implying higher risk.


4. Standout traders and rankings
In each sentiment class, a few traders consistently ranked at the top.


These traders can serve as benchmarks or signals for strategy development.


Plain Language Summary
Market mood strongly influences trader performance.


Most traders profit when the market is greedy, while a rare few thrive in fearful conditions.


More trades ≠ more profits — timing and skill matter.


Identifying consistent or contrarian traders can help design smarter, sentiment-aware trading strategies.


5. Future Work
Expand analysis to more granular timeframes (e.g., daily, weekly)


Include sector-based sentiment analysis for deeper insights


Apply predictive models to forecast trader performance based on sentiment
6. Tools & Technologies Used
Programming: Python


Libraries: Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn


Environment: Jupyter Notebook, Google Colab



Prepared by: Ayushi Bhati
 Date: 09 September 2025
