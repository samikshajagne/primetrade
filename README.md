# primetrade
📌 Project Title:

Analyzing the Impact of Market Sentiment on Trader Performance using the Fear–Greed Index & Hyperliquid Trading Data

🧩 Project Overview

This project explores how market sentiment—captured using the Fear–Greed Index—affects the trading performance of users on the Hyperliquid platform.
The goal is to determine whether emotional market conditions like Fear and Greed meaningfully influence trader profits and losses.

This project includes:

Data Cleaning

Exploratory Data Analysis (EDA)

Visualization

Statistical Hypothesis Testing

Machine Learning Modeling

Insight Generation & Reporting

🎯 Objective

To understand whether market sentiment impacts trader performance
and
to evaluate if sentiment can be used to predict daily trading profit and loss (PnL).

📂 Dataset Description
1. Market Sentiment Data

Date

Sentiment Score

Classification (Extreme Fear, Fear, Neutral, Greed, Extreme Greed)

2. Hyperliquid Trader Data

Trade details (symbol, size, leverage, etc.)

Closed PnL

Timestamps

Account and trade metadata

Merged Dataset

Both datasets were merged on the date column to align daily sentiment with trading outcomes.

🔧 Data Processing Steps
✔ Cleaning

Fixed date formats

Converted numeric columns

Removed invalid/missing entries

✔ Feature Engineering

Created features such as:

sentiment_change

sentiment_ma3, sentiment_ma7

winrate, avg_leverage, avg_trade_size

sent_class_num (numeric version of sentiment class)

✔ Daily Aggregation

Converted trade-level data into daily summaries:

Total daily PnL

Average sentiment

Daily winrate

Average leverage

📊 Exploratory Analysis & Visualizations

The project includes over 10 visualizations, such as:

Sentiment trends over time

Distribution of trader PnL

Sentiment category counts

Daily PnL patterns

Correlation heatmap

Sentiment vs PnL scatter plots

Volatility comparisons

Key Insight:

Markets experience clear emotional cycles, but PnL does not rise or fall consistently with sentiment.

🔬 Statistical Tests Conducted
Test	Purpose	Result
Shapiro–Wilk	Normality of PnL	Non-normal (heavy tails)
Levene’s test	Equal variance in Fear vs Greed	Variances similar
Welch t-test	Difference in mean PnL	No significant difference
Cohen’s d	Effect size	Near zero
Mann–Whitney U	Distribution difference	Statistically diff., negligible effect
Pearson correlation	Sentiment vs PnL	≈ 0 correlation
Chi-square	Sentiment vs win/loss	Very weak relationship

Conclusion:
Sentiment level (Fear/Greed) shows minimal direct influence on trader PnL.

🤖 Machine Learning Modeling

Two models were implemented:

1. Linear Regression

R² = –0.28

Could not predict PnL

Confirms weak linear relationship

2. Random Forest

R² = –0.26

Slight improvement but still low predictive power

Feature Importance Results

Most important features:

Sentiment moving averages (trend > absolute score)

Winrate

Leverage

Least important:

Sentiment class (Fear/Greed level)

Insight:

Sentiment change and trend matter more than sentiment levels.
Trader behavior > sentiment level when predicting PnL.

⭐ Key Conclusions

Sentiment level does NOT directly predict trader performance.

Sentiment volatility and moving averages are more important than the raw sentiment value.

Trader behavior metrics (winrate, leverage) have far stronger influence on PnL.

ML models confirm poor predictive power of sentiment alone.

Market sentiment acts as a contextual indicator, not a predictive one.

🚀 What Makes This Project Stand Out

End-to-end analysis using EDA + statistics + ML + insights

Clear narrative supported by data-driven evidence

Realistic financial interpretation

Proper use of hypothesis testing

Demonstration of both technical and analytical thinking

Install dependencies:
pip install pandas numpy matplotlib seaborn scikit-learn scipy

How To Run

Upload the datasets

Open the notebook(s) in the notebooks/ folder

Run cells step-by-step
Contact / Credits

Author: Samiksha Jagne 
mail: samikshajagne2@gmail.com
phone : 7620979617
linkedin: https://www.linkedin.com/in/samiksha-jagne/
Feel free to reach out for collaboration or queries!
