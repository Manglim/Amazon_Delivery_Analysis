# Delivery Time Prediction

This repository contains a Jupyter Notebook (`delivery_time_prediction.ipynb`) for predicting food delivery times using a dataset from the Amazon Business Research Analyst Hiring Challenge. The project is implemented in a single cell, covering data cleaning, feature engineering, modeling with a Random Forest regressor, and visualization of results to predict the `Time_taken(min)` variable.

## Dataset
- **File**: `updated.csv` (not included in the repository due to size; replace with your own data)
- **Description**: The dataset includes delivery details such as:
  - Delivery person age and ratings
  - Restaurant and delivery location coordinates
  - Order and pickup times
  - Weather conditions, road traffic density, vehicle condition, etc.
  - Target variable: `Time_taken(min)` (delivery time in minutes)

## Project Structure
- **`delivery_time_prediction.ipynb`**: Jupyter Notebook with a single-cell pipeline:
  1. **Data Cleaning**: Handles missing values, fixes invalid times, and corrects coordinates.
  2. **Feature Engineering**: Calculates distance, pickup delay, hour of day, and interaction features.
  3. **Modeling**: Trains a Random Forest Regressor to predict delivery time.
  4. **Evaluation**: Computes RMSE and R² metrics.
  5. **Visualization**: Generates six graphs (see below).

## Graphs
The notebook produces the following visualizations in a single run:
1. **Actual vs Predicted Delivery Time**: Scatter plot comparing model predictions to actual values.
2. **Feature Importance**: Bar plot showing the most influential features in the model.
3. **Distribution of Delivery Time**: Histogram and KDE of the target variable.
4. **Delivery Time vs Distance**: Scatter plot of time taken vs calculated distance.
5. **Delivery Time by Road Traffic Density**: Box plot showing time distribution across traffic levels.
6. **Delivery Time by Weather Conditions**: Box plot of time across weather conditions.

## Requirements
To run the notebook, install the following Python libraries:
```bash
pip install pandas numpy scikit-learn matplotlib seaborn
