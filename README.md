# Stock Price Prediction

**Week 1 · Foundations — Task 3 of 3**

## Description
Build a machine learning model to predict future stock prices using historical stock market data. This project uses 5 years of daily AAPL price data to train and compare three models — Linear Regression, Random Forest, and LSTM — then evaluates, visualizes, and forecasts with them.

## Objective
Understand time-series forecasting and regression techniques in machine learning: preparing time-series data correctly, comparing how different model types learn from sequential financial data, evaluating forecasts with standard regression metrics, and recognizing each model's limitations.

## What's Included
A single script, `stock_price_prediction.py`, that runs all 9 subtasks in order:

1. Collect and load historical stock price data
2. Perform exploratory data analysis and visualization
3. Prepare features for prediction
4. Split data into training and testing sets
5. Train a prediction model (Linear Regression, Random Forest, LSTM)
6. Evaluate the model using MAE, MSE, and RMSE
7. Visualize actual vs predicted stock prices
8. Generate predictions for future dates
9. Document model limitations and observations

## How to Run
```bash
pip install -r requirements.txt
python stock_price_prediction.py
```

Charts and a final report are saved to the `outputs/` folder.

## Note
The script tries to download real AAPL data via `yfinance` first, and falls back to a realistic simulated dataset if there's no internet access — so it runs end-to-end either way.
