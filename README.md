# AI Trading Bot

An AI-powered trading bot that uses sentiment analysis of financial news to inform trading decisions. This bot is designed to execute trades automatically based on the predicted sentiment of recent news articles related to a specific stock (e.g., SPY).


## Overview
The AI Trading Bot utilizes the FinBERT model to perform sentiment analysis on news headlines related to a specific stock. Based on the sentiment (positive, negative, or neutral) and the confidence level, the bot makes automated trading decisions using Alpaca's API. The bot is capable of both backtesting on historical data and live trading.


## Features
- **Sentiment Analysis**: Uses the FinBERT model to analyze news headlines and predict market sentiment.
- **Automated Trading**: Executes buy and sell orders based on the predicted sentiment and a predefined strategy.
- **Backtesting**: Tests the trading strategy on historical data to evaluate performance before live trading.
- **Risk Management**: Incorporates risk management techniques, such as stop-loss and take-profit orders.

## Project Structure
- `finbert.py`: Contains the `estimate_sentiment` function that performs sentiment analysis using the FinBERT model.
- `tradingbot.py`: The main trading bot script that integrates with Alpaca and LumiBot, defines the trading strategy, and handles trading operations.


## How It Works
1. **Sentiment Analysis**: The bot fetches recent news headlines for the specified stock symbol and uses the FinBERT model to estimate sentiment.
2. **Trading Strategy**: Based on the sentiment and confidence level, the bot decides whether to buy or sell the stock. It uses a predefined risk management strategy to place orders.
3. **Backtesting**: The bot can backtest the strategy on historical data to analyze performance before deploying it in a live environment.


## Results
The bot’s performance is benchmarked against SPY, with results visualized in a graph comparing cash, SPY, and the bot's strategy over time. In backtesting, the bot has demonstrated potential for consistent returns, particularly in periods of high market volatility.

!['cash graph.png'](https://github.com/Praneshv25/AI-Trading-Bot/blob/main/cash%20graph.png)
![](https://github.com/Praneshv25/AI-Trading-Bot/blob/main/cumulative%20returns.png)
