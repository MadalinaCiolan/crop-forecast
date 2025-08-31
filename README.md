# Crop Forecast

Repository for the Final Project of Data Science and Computing degree: Crop Forecast based on Weather Data

## Overview

This project predicts crop yields (barley, oats, rapeseed, wheat) in Wales using historical weather data and crop calendars. It demonstrates the application of data science techniques to agricultural forecasting.

## Project Structure

```
.gitignore
README.md
code/
    prediction_filtered_by_crop_calendar.ipynb
    prediction_full.ipynb
data/
    barley_calendar.csv
    oats_calendar.csv
    rapeseed_calendar.csv
    wheat_calendar.csv
    wales/
        wales_airfrost_days.csv
        wales_barley_production_averaged.csv
        wales_monthly_sunshine.csv
        wales_monthly_temp.csv
        wales_oats_production_averaged.csv
        ...
images/
    input_data_trends_no_crop_smoothing.png
    output_prediction_no_crop_smoothing.png
    yearly_output_prediction_no_crop_smoothing.png
```

## Data Sources

- **Weather Data**: Monthly air frost, sunshine, temperature, and rainfall for Wales ([data/wales/](data/wales/)).
- **Crop Calendars**: Planting and harvesting periods for each crop ([data/barley_calendar.csv](data/barley_calendar.csv), etc.).
- **Crop Production**: Historical yield data for each crop ([data/wales/wales_barley_production_averaged.csv](data/wales/wales_barley_production_averaged.csv), etc.).

## Methodology

- **Data Preprocessing**: Combines weather and crop data, aligns with crop calendars.
- **Exploratory Analysis**: Visualizes trends and seasonality (see [images/](images/)).
- **Stationarity Testing**: Uses ACF and Box-Cox transformation for time series analysis.
- **Modeling**: Implements time series forecasting and machine learning models (see [code/prediction_full.ipynb](code/prediction_full.ipynb)).
    - Hyperparameter tuning (learning rate, batch size, epochs).
    - Cross-validation (folds for train/test splits).
- **Evaluation**: Reports loss and validation loss per epoch.

## Usage

1. Place all data files in the `data/` directory.
2. Open and run [code/prediction_full.ipynb](code/prediction_full.ipynb) or [code/prediction_filtered_by_crop_calendar.ipynb](code/prediction_filtered_by_crop_calendar.ipynb) in Jupyter.
3. View output plots in [images/](images/).

## Results

- Forecasts crop yields for future months based on weather trends.
- Visualizes input data and predictions.
- Evaluates model performance using loss metrics.

## Requirements

- Python 3.x
- Jupyter Notebook
- pandas, numpy, matplotlib, scikit-learn, statsmodels

## Authors

- Final Year Data Science and Computing Student

## License

For academic use only.
