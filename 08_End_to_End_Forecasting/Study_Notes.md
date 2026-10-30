# Module 08: End-to-end forecasting case study

Compare baselines and models, evaluate on a holdout and communicate uncertainty.

# Core time-series concepts

A time series is a sequence of observations indexed by time. Unlike randomly shuffled tabular data, order matters.

**Frequency and granularity:** daily data must be checked for gaps and duplicates before forecasting.

**Trend:** long-run movement. **Seasonality:** repeating variation at a fixed calendar period. **Noise:** irregular residual variation.

**Temporal split:** train on the past, validate on later dates, test on the latest untouched period. Never randomly shuffle rows.

**Leakage:** never use future observations to construct lag features, rolling averages, scaling statistics, or tuning choices.

**Baselines:** last-value and seasonal-naive forecasts are essential benchmarks; complex models must beat them.

**Metrics:** MAE is average absolute error, RMSE penalizes large errors, MAPE is unstable near zero, and sMAPE also requires care.

**Intervals:** point forecasts do not describe uncertainty. Residual-based intervals are approximate and require calibration checks.

**Correlation is not causation:** promotions and weather may be associated with sales but observational patterns do not establish effects.

**Synthetic data:** the included dataset is generated for education and is not a real store's history.

## Workflow
1. Load the data and parse timestamps.
2. Check time ordering, gaps and anomalies.
3. Plot raw observations and appropriate summaries.
4. Create a strictly chronological holdout.
5. Fit a benchmark and a candidate model on the training period.
6. Score forecasts on held-out observations.
7. Discuss errors, limitations, and possible drift.

## Questions to ask
- Is the time frequency appropriate for the decision?
- Are holiday or promotion calendars known ahead of the forecast horizon?
- Is there a meaningful seasonal period?
- Does the evaluation simulate how forecasts would be used?

## Key formulas
- MAE = mean(|actual - forecast|)
- RMSE = sqrt(mean((actual - forecast)^2))
- Seasonal naive: forecast at t = observed value at t - season_length

## Further reading
- Hyndman & Athanasopoulos, *Forecasting: Principles and Practice* (online).
- pandas time series user guide; statsmodels forecasting documentation; scikit-learn model selection documentation.
