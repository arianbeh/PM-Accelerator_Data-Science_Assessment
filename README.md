# Weather Trend Forecasting

Advanced weather trend forecasting project using the Global Weather Repository dataset.

## Project Files

- `weather_trend_forecasting_advanced.ipynb` - main notebook with data loading, cleaning, EDA, anomaly detection, forecasting models, ensembles, and feature importance.
- `data/GlobalWeatherRepository.csv` - weather dataset used by the notebook.
- `requirements.txt` - Python packages needed to run the notebook.

## Project Scope

- Data cleaning and preprocessing: timestamp parsing, duplicate handling, explicit feature selection, scaling, categorical encoding, and conservative outlier handling.
- EDA: temperature, precipitation, correlation/association tables, weather condition summaries, time patterns, air quality relationships, and geography/spatial plots.
- Advanced EDA: IQR outliers, location-relative z-score anomalies, and Local Outlier Factor anomaly detection.
- Forecasting: Ridge Regression, Random Forest, HistGradientBoosting, soft average ensemble, and holdout stacking ensemble.
- Evaluation: MAE, RMSE, R2, and forecast accuracy within +/-2C, +/-3C, and +/-5C.
- Unique analyses: climate/time patterns, environmental impact, feature importance, spatial/geographical patterns.
- PM Accelerator mission statement: included in the notebook with source attribution.

## How To Run

1. Create and activate a Python environment.
2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Open and run:

```bash
jupyter notebook weather_trend_forecasting_advanced.ipynb
```

The notebook expects the dataset at `data/GlobalWeatherRepository.csv`.

## Current Best Model

Strict future-holdout validation selects Random Forest trained on the conservative filtered training set:

- MAE: 3.057 C
- RMSE: 4.464 C
- R2: 0.831
- Accuracy within +/-2C: 50.4%
- Accuracy within +/-3C: 64.1%
- Accuracy within +/-5C: 81.0%
