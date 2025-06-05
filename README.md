# Gold-Price-Prediction-with-RNN

This repository implements three recurrent-neural-network families—**Vanilla RNN, LSTM and GRU**—and compares their ability to model the non-linear, time-dependent patterns of the gold market.

---

## 1. Project Results
| Model | RMSE | MAE | R-squared | Notes |
|-------|-----------|----------|-------|-------|
| RNN   | 0.0202 | 0.0156 | 0.8839 | Captured the general ups and downs quite well |
| LSTM  | 0.0245 | 0.0183 | 0.8334 | Caught the general trend, but missed on timing |
| GRU   | 0.0416 | 0.0372 | 0.5051 | Visibly smoother and seemed to underestimate volatility |


---

## 2. Repository Layout
.
├── data/
│ └── processed data
│ └── gold_price(2013-2022).csv
│ └── gold_price(2023).csv 
├── notebooks/
│ ├── Thesis_EDA.ipynb # exploratory data analysis – trends, seasonality, stationarity
│ ├── RNN.ipynb # baseline vanilla RNN
│ ├── LSTM.ipynb # LSTM architecture & tuning
│ └── GRU_Thesis.ipynb # GRU architecture & tuning
├── models/ # saved (best) weights & scalers
└── README.md

---

## 3. Data
* Source: [Gold Futures Historical Data](https://www.investing.com/commodities/gold-historical-data)
* Frequency: **Daily**, fields = Date, Price, Open, High, Low, Vol., Change%

---


