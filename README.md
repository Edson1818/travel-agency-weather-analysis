# Travel Agency Weather Analysis

This project presents a linear regression model to help a European travel agency identify U.S. cities suitable for warm-weather holiday packages.

## Overview

Using publicly available weather data, the model predicts average temperatures based on geographic and meteorological variables. The goal is to support the agency in expanding its destination portfolio beyond traditionally popular cities by identifying lesser-known but consistently warm locations.

## Methodology

- Developed in **R** using `stats`, `ggplot2`, and `dplyr`.
- Built a linear regression model using five initial predictors:  
  `latitude`, `log_elevation`, `wind_speed`, `precipitation`, and `log_distance_to_coast`.
- Applied **stepwise AIC** to select the most informative model.
- Final model included three key variables: `latitude`, `log_elevation`, and `wind`, all negatively associated with temperature.
- Assessed model performance using R², RMSE, MAE, and residual diagnostics.

## Key Findings

- **R² = 0.87** — the model explains 87% of the variance in average temperature.
- Coastal cities (within 60 km of the coast) are warmer and more consistent in temperature than inland cities.
- Springfield, OH was correctly excluded based on a 55 °F threshold.
- The Florida prediction was within a reasonable range, supporting model validity.

## Dataset

The dataset used in this analysis contains U.S. city-level weather information, including:

- Average annual temperature  
- Latitude  
- Elevation  
- Wind speed  
- Precipitation  
- Distance to the coast  

📂 [Download the dataset (weather.RData)](weather.RData)

This `.RData` file was used to train and validate the model presented in the report.

## Report

📎 [Read the full project report](Travel_Agency_Weather_Analysis_Report.pdf)

Includes methodology, model diagnostics, evaluation metrics, and recommendations for city selection.

## Tools Used

- **Language:** R  
- **Libraries:** `stats`, `ggplot2`, `dplyr`  
- **Modeling Approach:** Linear regression with stepwise AIC

## Author

Edi Okwok

## Copyright and Usage

© 2025 Edi Okwok. All rights reserved.

This work is publicly viewable for personal learning and portfolio review only.  
**Reproduction, redistribution, or reuse for academic, commercial, or publication purposes is strictly prohibited without written permission.**
