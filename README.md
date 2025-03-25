# Delivery Time Prediction with Random Forest

## Overview
This project predicts food delivery times using a Random Forest Regressor on data from `updated.csv`. It cleans the dataset, engineers features like distance and pickup delay, evaluates the model, and visualizes key insights to understand delivery time drivers.

## Functionality
1. **Data Cleaning**:
   - Fixes invalid times (e.g., "10:60" → "11:00"), replaces 0s with NaN, fills missing values with medians.
   - Drops rows missing critical data.

2. **Feature Engineering**:
   - `Distance_km`: Haversine distance between restaurant and delivery locations.
   - `Pickup_Delay`: Time between order and pickup (adjusted for midnight).
   - `Hour_of_Day`: Extracted from order time.
   - `Age_Rating_Interaction`: Delivery person age × ratings.

3. **Modeling**:
   - Random Forest Regressor (100 trees) predicts `Time_taken(min)`.
   - 80/20 train-test split.

4. **Evaluation**:
   - RMSE and R² metrics.

5. **Visualization**:
   - Actual vs. predicted, feature importance, delivery time distribution, and relationships with distance, traffic, and weather.

## Frameworks and Libraries
- **Python**: Core.
- **Pandas**: Data handling (`pd`).
- **NumPy**: Numerical ops (`np`).
- **Math**: Haversine formula.
- **Scikit-learn**: Modeling (`RandomForestRegressor`, etc.).
- **Matplotlib**: Plots (`plt`).
- **Seaborn**: Visualizations (`sns`).

## Dataset
- Source: `updated.csv`.
- Rows: 2,266 post-cleaning.
- Key Columns: `Delivery_person_Age`, `Restaurant_latitude`, `Time_taken(min)`, etc.
- Features: 14, Target: `Time_taken(min)`.

## Key Features
- **Data Prep**: Robust handling of messy data.
- **Geo Features**: Accurate distance calculation.
- **Temporal Context**: Pickup delay and hour of day.
- **Insightful**: Visuals and feature importance.

## Installation
```bash
pip install pandas numpy scikit-learn matplotlib seaborn
