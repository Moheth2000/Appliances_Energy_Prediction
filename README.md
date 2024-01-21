# Appliances Energy Prediction

## Overview

This project focuses on predicting energy consumption by household appliances to facilitate energy conservation. By analyzing data collected from an airport weather station in Chievres Airport, Belgium, the goal is to identify which appliances consume more energy, enabling users to take informed steps for conservation.

## Data Source

The dataset, comprising 19736 rows and 29 columns, is sourced from Kaggle: [Appliances Energy Prediction](https://www.kaggle.com/loveall/appliances-energy-prediction). The target variable is 'Appliances,' representing energy consumption in Wh. Key features include temperature (T1, T2), humidity (RH1, RH2), lights, windspeed, visibility, and Tdewpoint.

## Data Processing

The dataset is loaded into a Pandas DataFrame, checked for null values (none found), and underwent initial statistical analysis. To improve model accuracy, redundant variables (correlated 'T' and 'RH' series) and unnecessary columns (Lights, Date) were removed.

## Data Exploration and Visualization

Correlation heatmaps, scatter matrices, and boxplots were used for data exploration. Scaling was applied using StandardScaler for improved visualization. Outliers were identified and boxplots created both with and without outliers to understand predictor distributions.

## Data Mining Tasks and Models

Cross-validation was performed on various models, including Lasso, Ridge, K Neighbors Regressor, SVR, Random Forest, Gradient Boosting Classifier, XGB Regressor, and MLP Regressor. RandomForestRegressor was chosen for its highest accuracy.

## Implementation of Selected Model

After model selection, the 'Tdewpoint' column was removed to enhance accuracy. Principal Component Analysis (PCA) was applied to evaluate the impact of component reduction on accuracy.

## Performance Evaluation and Interpretation

For the selected RandomForestRegressor model, accuracy, RMSE, MAE, and MSE were calculated. These metrics were compared across all models for comprehensive evaluation.

## Results

- **Actual vs Fitted Values:** Plot depicting the actual vs fitted values for the target variable 'Appliances.'
- **Lift Chart/Decile Lift Chart:** Visualization showing the model's performance.
- **Correlation between Actual and Predicted Values:** Correlation plot indicating a strong model (correlation = 0.68).

## Impact of Project Outcomes

The project's predictive capabilities enable users to identify high-energy-consuming appliances, promoting energy conservation. On a global scale, this initiative could contribute to environmental protection by reducing excessive natural resource consumption for power supplies.
