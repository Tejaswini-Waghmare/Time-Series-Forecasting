# Time Series Forecasting — Zero to Applied

Eight educational modules covering forecasting foundations, seasonality, autocorrelation, baselines, exponential smoothing, ARIMA, machine learning, and a case study.

**Dataset:** 730 synthetic daily store sales observations, not real business data.

## Quick start
```bash
python -m pip install -r requirements.txt
jupyter notebook
```
Open each module’s `Examples.ipynb` from the repository root. For Colab, upload the notebook and `data/daily_store_sales.csv` to the same session.

## Learning sequence
- [01_Time_Series_Fundamentals](01_Time_Series_Fundamentals/README.md) — Time series fundamentals
- [02_Trends_Seasonality](02_Trends_Seasonality/README.md) — Trend and seasonality
- [03_Stationarity_Autocorrelation](03_Stationarity_Autocorrelation/README.md) — Stationarity and autocorrelation
- [04_Forecasting_Baselines](04_Forecasting_Baselines/README.md) — Forecasting baselines
- [05_Exponential_Smoothing](05_Exponential_Smoothing/README.md) — Exponential smoothing
- [06_ARIMA_SARIMA](06_ARIMA_SARIMA/README.md) — ARIMA and SARIMA
- [07_ML_for_Time_Series](07_ML_for_Time_Series/README.md) — Machine learning for time series
- [08_End_to_End_Forecasting](08_End_to_End_Forecasting/README.md) — End-to-end forecasting case study

## Responsible use
Educational examples, not production forecasts. Train/test splits are chronological. Compare against baselines and assess uncertainty before real-world deployment.
