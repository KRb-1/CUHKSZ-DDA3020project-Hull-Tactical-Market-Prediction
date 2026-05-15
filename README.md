# CUHKSZ_DDA3020: Hull-Tactical Market Prediction

[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 📌 Project Overview
This project focuses on predicting S&P 500 excess returns while managing volatility constraints. By leveraging a diverse set of market indicators, the project aims to:
*   **Test the Efficient Market Hypothesis (EMH)** in a modern quantitative context.
*   **Challenge traditional personal finance tenets** through data-driven tactical allocation.
*   **Optimize predictive performance** under strict risk management parameters.

---

## 📊 Dataset Description
The dataset consists of historical market data spanning several decades. It includes a high-dimensional feature set designed to capture various facets of the economy and market psychology.

### Data Files
| File | Description |
| :--- | :--- |
| `train.csv` | Historical market data used for model development. Contains target variables. |
| `test.csv` | Mock test set for local validation and API integration testing. |
| `kaggle_evaluation/` | Utility files required for the competition evaluation API. |

### Feature Taxonomy
The features are categorized by their underlying economic or technical drivers:

| Prefix | Category | Description |
| :--- | :--- | :--- |
| **M*** | Market Dynamics | Technical indicators and internal market flow. |
| **E*** | Macro Economic | Broad economic health indicators (e.g., GDP, employment). |
| **I*** | Interest Rates | Yield curves and central bank policy metrics. |
| **P*** | Price/Valuation | Fundamental valuation ratios and price levels. |
| **V*** | Volatility | Market stress and risk metrics. |
| **S*** | Sentiment | Investor psychology and news-based signals. |
| **MOM*** | Momentum | Trend-following indicators and price velocity. |
| **D*** | Binary/Dummy | Categorical flags and regime identifiers. |

---

## ⚙️ Competition Phases
The evaluation follows a two-stage process to ensure model robustness and prevent overfitting to historical bias.

1. **Phase 1: Model Training**
   * **Scope:** 6 months of historical data.
   * **Note:** Public leaderboard scores in this phase are for testing infrastructure only, as data is publicly accessible.

2. **Phase 2: Forecasting (Out-of-Sample)**
   * **Scope:** Real-time data collected after the submission deadline.
   * **Evaluation:** Models are served data via a specialized API to simulate a live trading environment.

---

## 📈 Key Targets & Metrics
The model aims to predict the following primary targets (available in `train.csv` and as lagged features in `test.csv`):

*   **`forward_returns`**: The raw 1-day lead return of the S&P 500.
*   **`market_forward_excess_returns`**: Returns relative to expectations (Winsorized using Median Absolute Deviation with a criterion of 4).
*   **`risk_free_rate`**: The federal funds rate used for calculating the Sharpe ratio and excess returns.

---

## 🚀 Getting Started
To use the evaluation API and run the baseline models:
1. Clone the repository.
2. Ensure `train.csv` is placed in the `/data` directory.
3. Refer to the `demo_submission.py` for API integration logic.

---

## 📄 Project Report

For detailed methodology, experiments, and results, please refer to the [**full project report (PDF)**](./docs/report.pdf).



