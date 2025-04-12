# Statistical Arbitrage Strategy Using Pairs Trading (XLE & VDE)

This project implements a statistical arbitrage strategy using cointegration-based pairs trading on two energy sector ETFs: XLE (Energy Select Sector SPDR Fund) and VDE (Vanguard Energy ETF). The strategy exploits the mean-reverting behavior of the price spread between the two highly correlated ETFs.

---

## Project Overview

- Cointegration Test: Engle-Granger test confirms long-term relationship between XLE and VDE
- Hedge Ratio: Calculated via linear regression to construct the spread
- Trading Signals: Z-score based entry/exit logic
  - Go Long: Z < -1 → Buy XLE, Sell VDE
  - Go Short: Z > +1 → Sell XLE, Buy VDE
  - Exit: Z-score returns to within ±0.5
- Backtesting: Simulates daily returns and visualizes cumulative performance from 2019 to 2025

---

## Key Features

- Time series analysis and regression modeling with statsmodels
- Live market data fetched using yfinance
- Signal generation based on Z-score thresholds
- Strategy backtesting with daily PnL simulation
- Visualization of price spread, signals, and performance

---

## Tech Used

- Python (Jupyter Notebook)
- pandas, matplotlib, statsmodels, yfinance
