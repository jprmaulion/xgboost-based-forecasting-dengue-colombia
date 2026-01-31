## Developing an XGBoost-based, Bayesian-optimized pipeline for forecasting dengue cases in Magdalena, Colombia 🇨🇴

## Description

This repository houses a machine learning pipeline that leveraged XGBoost and Bayesian optimization to forecast weekly dengue cases in Magdalena, Colombia. This pipeline also includes time series feature engineering and rolling statistics for accurate short-term predictions.

## Overview

This project implements a machine learning approach to forecast weekly dengue cases in Colombian regions (Magdalena and Cúcuta). Leveraging time series feature engineering—including lagged variables, rolling statistics, and epidemiological seasonal indicators—combined with Bayesian optimization of an XGBoost model, the pipeline achieves accurate short-term forecasting of dengue incidence. The work demonstrates how data-driven methods can support public health surveillance with limited available data.



## Data

- Weekly reported dengue case counts from Colombian health authorities.
- Regions covered: Magdalena and Cúcuta (2022 data).
- Additional seasonal and temporal features generated.

---

## Methods

1. **Exploratory Data Analysis:**  
   Seasonal-trend decomposition (STL), stationarity testing (ADF), and autocorrelation (ACF/PACF) to understand temporal dependencies and seasonality.

2. **Feature Engineering:**  
   - Lag features up to 13 weeks (due to data length constraints).  
   - Rolling window statistics (2, 4, 8 weeks).  
   - Seasonal indicators (epi_week, year).

3. **Modeling:**  
   - XGBoost regression for forecasting, with hyperparameters tuned via Bayesian Optimization.  
   - Performance evaluated using RMSE, MAE, and R² on train/test splits.

---

## Results

- High predictive accuracy ($R^{2}$ ~0.98) on both training and testing datasets.  
- Forecasts generated for 13 weeks ahead demonstrating moderate fluctuations in dengue incidence.


## Graphical summary


![Forecast Curve](forecasted-dengue-colombia.png)

*Figure*: Weekly observed dengue cases in Magdalena, Colombia during 2022 (solid line) and the model’s forecasted cases for the subsequent 13 weeks (dashed line with red markers), illustrating near-term predicted trends.
---

## License

This project is licensed under the MIT License. 

---

## Questions?

For questions or clarifications (or maybe collaboration opportunities!), please open an issue or contact jprmaulion[at]gmail[dot]com.
