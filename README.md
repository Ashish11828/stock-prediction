# Stock Trading AI — Pattern-Based Trader

## 📈 Overview

This project implements an intelligent algorithm to predict and trade stocks in a simulated environment. Starting with a fixed capital of `$100`, the program processes stock price histories and decides when to **BUY**, **SELL**, or **HOLD** shares of various stocks.

Your objective: **maximize profit by the end of the simulation**.

---

## 🧠 Strategy

This program uses a **rule-based trading strategy** that considers recent price trends of each stock:

- **Trend Analysis**: Uses the difference between the 5th and 1st day price to identify upward or downward momentum.
- **Buying Logic**: If a stock is rising steadily, the algorithm attempts to buy as many shares as possible (limited by available cash).
- **Selling Logic**: If a stock is falling and we own it, we sell all holdings.
- **Delayed Funds**: Money from sold stocks only becomes available the next day — this constraint is respected.

Optional (Advanced versions):
- Linear Regression-based trend fitting.
- Volatility filtering.
- Persistent history tracking using file I/O.
- Final day liquidation strategy.

---

## 🧾 Input Format

Each day, the algorithm receives:

- First line:
- `m`: money available for buying **(float)**
- `k`: number of stocks available **(int)**
- `d`: remaining trading days **(int)**

- Followed by `k` lines (one per stock):

---


---

## ▶️ How to Run

This code is designed to be run in an interactive judge that supplies one day's input at a time. To run it locally for debugging:

```bash
python3 main.py < input.txt > output.txt
