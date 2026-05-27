# Flipkart-GridLock-Traffic-Demand-Prediction



Problem Statement
-----------------
The goal of this project is to predict traffic demand using machine learning techniques based on:
- Geographical location
- Time information
- Road properties
- Weather conditions
- Vehicle information

Dataset Files
-------------
1. train.csv
2. test.csv
3. submission.csv

Approach Used
-------------
An ensemble machine learning pipeline was developed using:
- CatBoost Regressor
- XGBoost Regressor
- LightGBM Regressor

The final prediction was generated using weighted averaging of all three models.

Feature Engineering
-------------------
Several advanced features were created to improve model performance.

1. Time Features
- hour
- minute
- month
- weekofyear
- dayofweek
- is_weekend
- peak_hour
- is_night

2. Cyclic Encoding
Cyclic transformations were applied to:
- hour
- weekday

using sine and cosine encoding.

3. Interaction Features
- temp_lane
- road_hour
- geo_hour

4. Statistical Features
Grouped aggregation features were created:
- geohash mean demand
- hour mean demand
- geohash + hour mean demand
- geohash + hour standard deviation

Models Used
------------
1. CatBoostRegressor
2. XGBRegressor
3. LGBMRegressor

Ensemble Formula
----------------
Final prediction:

final_prediction =
0.4 * CatBoost +
0.3 * XGBoost +
0.3 * LightGBM

Evaluation Metric
-----------------
The evaluation metric used was:

R² Score

Files Included
--------------
1. Traffic_Demand_Prediction.ipynb
2. submission.csv
3. README.txt

Tools & Libraries
-----------------
- Python
