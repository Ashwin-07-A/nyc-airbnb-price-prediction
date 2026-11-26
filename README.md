# Predicting New York City Airbnb Prices

Minor Project 2 | Linear Regression | AIML Batch (November Batch)
Name: Ashwin Ananth

## About
A Linear Regression model that predicts the nightly price of a New York City Airbnb listing.

## Dataset
New York City Airbnb Open Data (AB_NYC_2019.csv), 48,895 listings.
https://www.kaggle.com/datasets/dgomonov/new-york-city-airbnb-open-data
(The CSV is not included here. Download it from Kaggle to re-run the notebook.)

## What I did
- Cleaned the data: dropped last_review and ID columns, filled missing reviews_per_month with 0
- Removed outliers: prices above $355 (95th percentile), $0 prices and 365+ night stays
- Dropped the 200+ value neighbourhood column and one-hot encoded neighbourhood_group and room_type
- Split the data 80/20 (random_state=42) and trained a Linear Regression model

## Results (on unseen test data)
- R-squared: 0.47 (the model explains about 47% of the variation in price)
- MAE: $38.14 (predictions are off by about $38 per night on average)
- RMSE: $52.13
- The model is more accurate on cheaper listings (MAE $29.48) than on expensive ones (MAE $47.58).

## Files
- airbnb_price_prediction.ipynb: the full notebook
- EDA_Report_Airbnb_Ashwin_A.pdf: the summary report
