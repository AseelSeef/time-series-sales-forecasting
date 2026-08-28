# 📈 Sales & Demand Forecasting with Time Series and Machine Learning

An end-to-end forecasting analysis comparing statistical, machine learning,
deep learning, and hybrid approaches for predicting book sales.

The analysis evaluates weekly and monthly demand forecasting using historical
sales data for *The Very Hungry Caterpillar* and *The Alchemist*.

## 🎯 Objective

Build and compare forecasting approaches that can support inventory planning
and help reduce the risk of stock shortages and excess inventory.

## 🧠 Models

- SARIMA / Auto ARIMA
- XGBoost
- LSTM
- Sequential SARIMA–LSTM
- Parallel SARIMA–LSTM

Hyperparameter optimization was performed using Hyperopt and KerasTuner.

## 🔍 Approach

The workflow includes:

- Time-series preprocessing and weekly resampling
- Exploratory data analysis
- Seasonal decomposition
- ACF / PACF analysis
- Stationarity testing
- Lag-based feature engineering
- Hyperparameter tuning
- Recursive forecasting
- Hybrid model evaluation
- Weekly and monthly forecasting
- Model comparison using MAE, RMSE and MAPE

## 📊 Key Results

Model performance varied by title rather than one model consistently
outperforming all others.

For **The Very Hungry Caterpillar**, tuned XGBoost achieved the strongest
weekly MAE and MAPE:

| Model | MAE | RMSE | MAPE |
|---|---:|---:|---:|
| SARIMA | 349.06 | **448.93** | 18.47% |
| **Tuned XGBoost** | **341.37** | 460.76 | **15.76%** |
| Tuned LSTM | 460.45 | 577.73 | 23.15% |
| SARIMA–LSTM | 355.79 | 461.10 | 17.95% |

For **The Alchemist**, SARIMA provided the strongest overall weekly
performance with an MAE of **139.02** and RMSE of **213.38**.

SARIMA also outperformed XGBoost for monthly forecasting across both titles.

A key finding was that increasing model complexity did not necessarily improve
forecast accuracy: LSTM and hybrid approaches provided limited benefit compared
with the simpler SARIMA and XGBoost models.

## 🛠️ Technologies

Python · Pandas · NumPy · Statsmodels · pmdarima · Scikit-learn ·
XGBoost · TensorFlow/Keras · Hyperopt · KerasTuner · Matplotlib

## 📁 Repository

- `sales_demand_forecasting.ipynb` — complete implementation and experiments
- `sales_demand_forecasting_report.pdf` — detailed analysis, results
  and recommendations
- `requirements.txt` — Python dependencies

## 📄 Data

The original dataset is not included in this repository due to data
distribution restrictions.
