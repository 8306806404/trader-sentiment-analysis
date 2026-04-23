📊 Trader Performance vs Market Sentiment Analysis

📌 Overview

This project analyzes how market sentiment (Fear vs Greed) impacts trader behavior and performance using historical trading data from Hyperliquid and Bitcoin sentiment data.

The goal is to identify patterns that can help design smarter, sentiment-aware trading strategies.

📂 Datasets Used

1. Market Sentiment Data

* Contains daily Fear/Greed classification
* Columns: `date`, `classification`, `value`

2. Historical Trader Data

* Contains trade-level details
* Key columns: `Account`, `Execution Price`, `Size USD`, `Side`, `Timestamp IST`, `Closed PnL`

⚙️ Methodology

🔹 Data Preparation

* Loaded both datasets using Pandas
* Converted timestamps to datetime format
* Extracted **date** from trade timestamps
* Merged datasets on date to align trades with sentiment
* Handled missing values and duplicates

🔹 Feature Engineering

* Created **win column** (`Closed PnL > 0`)
* Approximated **leverage proxy** using `Size USD`
* Created trader segments:

  * High vs Low leverage traders
  * Frequent vs Infrequent traders
  * Winners vs Losers

📊 Analysis Performed

* Compared **PnL and win rate** across Fear vs Greed days
* Analyzed **trading behavior changes**:

  * Trade frequency
  * Position direction (Buy/Sell)
  * Trade size (risk proxy)
* Evaluated performance across different trader segments

💡 Key Insights

1. **Market sentiment strongly impacts performance**

   * Greed periods show relatively higher trading activity and profitability
   * Fear periods are associated with lower win rates and higher uncertainty

2. **Trader behavior changes with sentiment**

   * Traders take more aggressive positions during Greed
   * Fear leads to cautious or inconsistent trading behavior

3. **Risk (trade size) plays a major role**

   * Larger trades (proxy for leverage) show higher variability in outcomes
   * High-risk traders are more vulnerable during Fear periods

4. **Frequent traders behave differently**

   * More active traders adapt faster to sentiment shifts
   * Infrequent traders show inconsistent performance

🚀 Strategy Recommendations

✅ Strategy 1: Risk Control in Fear Markets

* Reduce trade size during Fear periods
* Avoid aggressive positions under uncertainty

✅ Strategy 2: Controlled Aggression in Greed Markets

* Increase participation during Greed phases
* Use strict stop-loss to manage downside risk

✅ Strategy 3: Segment-Based Strategy

* High-frequency traders can exploit short-term sentiment shifts
* Low-frequency traders should avoid overtrading in volatile periods

📈 Tools & Libraries

* Python
* Pandas
* Matplotlib / Seaborn
* Google Colab

Conclusion

This analysis demonstrates that **market sentiment significantly influences trader behavior and performance**. Incorporating sentiment signals into trading decisions can improve risk management and overall profitability.

▶️ How to Run

1. Open the notebook in Google Colab
2. Upload datasets or connect Google Drive
3. Run all cells step-by-step
4. View outputs and charts

Author

Data Science Intern Candidate
(Your Name)
