# Market Regime Detection & Strategy Adaptation

This project analyzes how financial markets behave under different conditions by detecting **market regimes** (Bull, Bear, and Sideways) using unsupervised machine learning and evaluating how simple trading strategies perform in each regime.

---

## 📌 Project Overview

Financial markets do not behave the same way all the time. Strategies that work well during bullish periods often fail during bearish or sideways markets.

This project:
- Detects market regimes using **K-Means clustering**
- Uses **returns and volatility** to characterize market behavior
- Analyzes **regime transitions and stability**
- Compares **strategy performance across regimes**

---

## 📊 Data

- Market: **NIFTY 50 Index**
- Frequency: **Weekly**
- Source: Yahoo Finance (`yfinance`)
- Time Period: From 2018 onwards

---

## 🧠 Methodology

### Feature Engineering
- Weekly returns
- Rolling 5-week returns (momentum)
- Rolling 5-week volatility (risk)

### Regime Detection
- Unsupervised learning using **K-Means (3 clusters)**
- Clusters mapped to:
  - **Bull**: Positive return, low volatility
  - **Bear**: Negative return, elevated volatility
  - **Sideways**: Low return, mixed volatility

### Regime Analysis
- Transition probability matrix
- Average regime duration
- Stability analysis

---

## 📈 Strategies Evaluated

- **Buy & Hold**
- **Momentum Strategy** (invest only when recent returns are positive)

Strategies are evaluated **separately for each market regime**.

---

## 🔍 Key Insights

- Bull regimes last longer than Bear regimes
- Bear regimes are shorter but more volatile
- Momentum strategy performs best during Bull regimes
- Strategy performance varies significantly across market regimes

---

## 🛠 Tech Stack

- Python
- Pandas, NumPy
- scikit-learn
- yfinance
- matplotlib, seaborn

---

## 📁 Repository Structure

Market-Regime-Detection/
│
├── market_regime_detection.ipynb
├── requirements.txt
├── README.md
└── .gitignore


---

## 🚀 How to Run

1. Clone the repository
```bash
git clone  https://github.com/Atul-Kumar002/Market-Regime-Detection.git

2. pip install -r requirements.txt

3. jupyter notebook market_regime_detection.ipynb
