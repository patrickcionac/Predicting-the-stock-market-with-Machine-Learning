# Predicting-the-stock-market-with-Machine-Learning

S&P 500 STOCK MARKET PREDICTOR
This project uses Machine Learning (Random Forest) to predict whether the S&P 500 stock index will go up or down the next day based on historical data. It focuses on backtesting and feature engineering using technical indicators like rolling averages.

OVERVIEW
The goal of this project is to build a robust system that:

Downloads historical data using the yfinance API.

Cleans and prepares data for Machine Learning.

Implements a Random Forest Classifier to handle non-linear market trends.

Uses Backtesting to validate the model's performance over 30+ years of data.

Improves precision by adding custom Rolling Average ratios.

TECH STACK
Python 3.9+

VS Code (Jupyter Extension)

Libraries:

pandas - Data manipulation

scikit-learn - Machine Learning

yfinance - Financial data API

matplotlib - Visualization

KEY FEATURES

1. Data Processing
We use historical prices of the GSPC (S&P 500) index. The target is a binary classification:

1: Price goes UP tomorrow.

0: Price goes DOWN tomorrow.

2. Rolling Averages (Feature Engineering)
To give the model more context, we calculated "Rolling Average" ratios for multiple time horizons (2, 5, 60, 250, and 1000 days). This helps the model understand if the current price is a "peak" or a "dip" relative to recent history.

3. Backtesting Strategy
Instead of a simple train/test split, we implemented a robust backtesting function that:

Starts with 10 years of data for training.

Predicts the next year.

Moves forward year by year, "learning" from all previous history.

RESULTS
Baseline Precision: ~53% (Buying every day).

Model Precision: ~57% (Using a 60% confidence threshold).

Summary: By asking the model to only predict "Up" when it is 60% sure, we significantly reduced "false positives" and improved trading reliability.
