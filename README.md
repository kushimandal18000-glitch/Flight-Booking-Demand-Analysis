# Flight-Booking-Demand-Analysis
# Flight Price Prediction using Decision Tree

## Overview
Predicts flight ticket prices from booking details and compares a Linear
Regression baseline with a Decision Tree regressor.

## Dataset
- 300,153 flight bookings, 11 columns after dropping the index column
- Features: airline, source city, departure time, stops, arrival time,
  destination city, class, duration, days left
- Target: price
- No missing values or duplicates found
- Source: [Kaggle dataset link]

## Approach
1. Data checks: info, describe, null and duplicate checks
2. EDA: price vs airline, price vs days left, price by class and airline
3. Label encoding of categorical variables
4. Correlation heatmap and VIF analysis; dropped `flight` (high VIF)
5. 75/25 train-test split
6. Models: Linear Regression (baseline) and Decision Tree Regressor

## Results
| Model | Test R² | Test RMSE |
|---|---|---|
| Linear Regression | ~0.89 | ~7,007 |
| Decision Tree | ~0.97 | ~3,545 |

## Tools Used
Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Statsmodels

## Future Improvements
- Tune hyperparameters (max depth, min samples split) to reduce overfitting
- Compare with Random Forest and Gradient Boosting
- Deploy as a simple web app
