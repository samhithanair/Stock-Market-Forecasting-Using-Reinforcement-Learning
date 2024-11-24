# Stock Market Forecasting with Reinforcement Learning

This project leverages advanced machine learning techniques to predict stock price movements. It integrates sentiment analysis, price forecasting, and volatility modeling into a reinforcement learning framework to enhance decision-making in financial markets.

## Overview
This system predicts stock price movements by:
1. Analyzing market sentiment using BERT.
2. Forecasting prices using a Random Forest model.
3. Modeling volatility with GARCH.
4. Combining these insights into a reinforcement learning framework to optimize trading decisions.

The final output is a binary decision (1 or 0), indicating whether the stock price is likely to increase (Bullish or Bearish).

---

## Project Workflow
1. Collect historical stock data (e.g., from [Yahoo Finance](https://finance.yahoo.com)).
2. Preprocess data for sentiment analysis, price prediction, and volatility modeling.
3. Use reinforcement learning to combine model outputs and optimize trading strategies.
4. Evaluate the performance of the system using ROC-AUC and other relevant metrics.

---

## Models and Components
### 1. **Sentiment Analysis**
- **Model**: BERT
- **Input**: Financial news, social media posts, reports.
- **Output**: Sentiment score (-1 to 1).

### 2. **Price Prediction**
- **Model**: Random Forest
- **Input**: Historical stock prices and features.
- **Output**: Predicted stock price.

### 3. **Volatility Modeling**
- **Model**: GARCH
- **Input**: Time-series stock price data.
- **Output**: Market volatility (standard deviation).

### 4. **Reinforcement Learning**
- **Environment**: Custom `MarketEnv` simulating stock market dynamics.
- **Policy**: Trains an agent to maximize reward (profit).
- **Decision Layer**: Combines sentiment, price prediction, and volatility to output a binary decision.

---

## Environment
- **Custom Environment**: `MarketEnv`
  - **States**: Sentiment score, predicted price, volatility.
  - **Actions**: Buy (1), Sell (0).
  - **Rewards**: Profit or loss based on stock price movement.

---

## Evaluation Metrics
The performance of the models is assessed using the following metrics:

### Proposed Reinforcement Learning Model
- ROC-AUC: Evaluates the model's ability to distinguish between stock price increases and decreases.
- Confusion Matrix: Provides insights into the number of true positives, true negatives, false positives, and false negatives, helping to assess classification accuracy.

### Random Forest Model (Price Prediction)
- Accuracy: Measures the overall correctness of the model's predictions.
- Precision: Calculates the proportion of true positive predictions among all positive predictions (focuses on relevance).
- Recall (Sensitivity): Measures the proportion of actual positives correctly identified by the model.
- Support: Shows the number of occurrences of each class in the dataset, helping to understand class imbalance.

---

## Installation
Run each `.ipynb` file
