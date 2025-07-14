# Metro. Zillow Home Value Index Forecasting & Analysis

This project explores trends in U.S. housing prices using the **Zillow Home Value Index (ZHVI)** dataset (2000–2025). It includes data cleaning, time-series analysis, SQL queries, and predictive modeling to understand how home values change over time and across regions.

---

## Project Summary

- Analyzed ZHVI data from Zillow covering U.S. housing markets over 20 years  
- Performed data cleaning with time-based imputation and reshaped the dataset for time-series analysis  
- Engineered features to capture temporal patterns (lags, rolling averages, seasonal cycles)  
- Built regression models to predict future values and evaluated their performance  
- Visualized housing trends 
- Used SQL for querying market insights and identifying growth patterns

---

## Tools & Libraries

Python, Pandas, Scikit-learn, SQLite (SQL), Matplotlib, Seaborn, Plotly, Geopy

---

## Data Processing

- Interpolated missing values using neighboring time points. Dropped all the remaining ZHVI without neighbors
- Converted data to long format for easier time-series modeling  
- Created new features for Month, Quarter, and encoded regions  


---

## Feature Engineering

To improve predictions:
- **Lag Features**: Past ZHVI values (1 month, 12 months)  
- **Rolling Means**: 3-month and 6-month averages  

These features help the model detect both short-term fluctuations and longer-term trends.

---

## Modeling - Linear Regression

### First Model  
- Used only categorical and seasonal features  
- **Test MSE**:  44712374615.17
- **Test RMSE**:  211453.01
- **Test R^2**:  -0.4
- **Approx. Accuracy**:  %55.96

### Improved Model  
- Included lag and rolling features  
- **Test MSE**:  468537.39
- **Test RMSE**:  684.5
- **Test R^2**:  1.0
- **Approx. Accuracy**:  %99.84

### Model Evaluation Metrics

- **Mean Squared Error (MSE):** Average of squared differences between actual and predicted values. Lower is better.  

- **Root Mean Squared Error (RMSE):** Square root of MSE, in the same units as the target. Lower means better accuracy.  

- **R-squared (R²):** Percentage of variance explained by the model. Closer to 1 means better fit; negative means worse than predicting the mean.  

- **Mean Absolute Percentage Error (MAPE):** Average absolute error as a percentage of actual values. Accuracy = 100 - MAPE (%). Lower MAPE means higher accuracy.  

## Visualization

- Line plots showing national and regional ZHVI trends  
- Yearly average values for selected states (NY, NJ, CT)  
- Interactive maps showing growth percentages across regions  
- Animated plots to observe market dynamics across the US from 2000–2025

---

## SQL Integration

- Loaded processed data into SQLite  
- Wrote queries to:
  - Calculate average ZHVI by year and state  
  - Find cities with highest average home values  
  - Track year-over-year growth rates

---

## Geolocation

Used `Geopy` to collect latitude and longitude for each region, enabling map-based visualizations of housing growth and comparisons across the U.S.

---

## About

This independent project was completed to strengthen my skills in SQLite (SQL), data analysis, time-series modeling, and geographic visualization. 
