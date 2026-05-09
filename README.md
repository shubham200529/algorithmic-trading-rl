# Trading RL System

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1QiuCYK4aHoYz4DOJVOyZI1XwmRq3pfWu?usp=sharing)

Reinforcement learning trading system built for an algorithmic trading internship coding task.

## Overview

This project implements:

- OHLCV data pipeline using yfinance
- Feature engineering with technical indicators
- Pattern discovery using KMeans clustering
- Custom Gymnasium RL trading environment
- R-multiple reward design
- PPO agent training using Stable-Baselines3
- Backtesting and evaluation metrics

The goal was not to build a profitable trading bot, but to demonstrate:
- environment correctness
- RL system design
- realistic reward engineering
- honest reporting of limitations

---

## Stack

- Python
- Gymnasium
- Stable-Baselines3
- yfinance
- pandas
- numpy
- scikit-learn
- ta

---

## Features

### Feature Engineering
- Returns
- ATR
- RSI
- MACD
- EMA ratios
- Volume z-score

### Pattern Discovery
- KMeans clustering used to identify recurring market states

### RL Environment
Actions:
- Hold
- Open Long
- Open Short
- Close Position

Includes:
- Commission
- Slippage
- Stop-loss / take-profit logic
- R-multiple reward system

---

## Evaluation Metrics

The notebook reports:
- Total return
- Sharpe ratio
- Max drawdown
- Number of trades
- Win rate
- Average R-multiple

Includes:
- Equity curve
- R-multiple distribution plot

---

## Run

Open the Colab notebook and run all cells from top to bottom.

Notebook link:

https://colab.research.google.com/drive/1QiuCYK4aHoYz4DOJVOyZI1XwmRq3pfWu?usp=sharing

---

## Notes

This project was completed under time constraints as an engineering-focused implementation task.

Several simplifications were intentionally made:
- KMeans instead of sequence models
- PPO without extensive hyperparameter search
- ATR-based risk management

Future improvements would include:
- Transformer/LSTM market-state encoders
- Walk-forward validation
- Better reward shaping
- Multi-asset training
