# 📊 Crypto Trading Strategies

This repository contains two distinct algorithmic trading strategies for Ethereum (ETH) and Bitcoin (BTC), along with historical hourly price data for performance evaluation. The strategies employ different methodologies — one based on feature-driven signal logic and the other on reinforcement learning.

---

## 📁 Project Structure

| File               | Description                                                                 |
|--------------------|-----------------------------------------------------------------------------|
| `main_1_eth.py`     | ETH trading strategy using feature-based signal construction, including BTC-ETH price correlation |
| `main_1_btc.py`     | BTC trading strategy powered by a Q-learning reinforcement learning agent   |
| `ETHUSDT_1h.csv`    | Hourly historical price data for ETH/USDT                                   |
| `BTC_2019_2023_1h.csv` | Hourly historical price data for BTC from 2019 to 2023                     |

---

## 🧠 Strategy Overview

### 🟣 ETH Strategy – Feature-Based Signal Generation

- The ETH strategy is designed using a **feature-based rule engine** that derives trade signals from market behavior and cross-asset relationships.
- A key input feature is the **short-term price movement correlation between BTC and ETH**, which helps identify dislocations or alignment patterns between the two assets.
- Additional features include:
  - Relative momentum
  - Short-term return anomalies
  - Threshold-based divergence detection
- The strategy enters or exits positions based on **multi-factor signal rules** that aim to capture mean-reverting or continuation opportunities.

---

### 🟠 BTC Strategy – Q-Learning Reinforcement Agent

- The BTC strategy is built on **Q-learning**, a model-free reinforcement learning algorithm.
- The agent learns to take actions (`Buy`, `Sell`, or `Hold`) that maximize cumulative reward through iterative interaction with the environment.
- Core components:
  - **State representation**: Derived from price-derived technical indicators or normalized market features.
  - **Reward function**: Tied to portfolio performance over time.
  - **Learning mechanism**: Updates Q-values using the Bellman equation, with an ε-greedy exploration strategy.

---

## 🧪 Backtesting Instructions

### ✅ Setup

Install any required libraries:
```bash
pip install -r requirements.txt
```

### ▶ Run ETH Strategy
```bash
python main_1_eth.py
```

### ▶ Run BTC Q-Learning Agent
```bash
python main_1_btc.py
```

> Ensure the `.csv` files are located in the same directory or adjust the file paths inside the scripts.

---
