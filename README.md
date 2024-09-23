# Efficient-Supply-Allocation-for-Ride-Hailing-Service

## Overview
This project aims to develop a machine learning-based solution to predict ride demand in specific regions of a city, enabling better driver allocation and improving overall service efficiency. The solution uses clustering to identify high-demand areas and leverages historical data to guide drivers toward regions with the highest predicted demand.

## Key Features
- **Demand Prediction**: Uses historical ride data to predict demand at different locations and times.
- **Clustering**: Applies K-means clustering to divide the city into regions, ensuring even dense areas are properly segmented.
- **Driver Guidance**: Guides drivers to regions with higher demand based on model predictions.
- **Modeling Approaches**: Implemented Random Forest, LightGBM, and XGBoost models, with hyperparameter tuning to improve predictions.

## Datasets
The dataset contains geospatial and temporal information of ride requests, such as:
- Latitude and Longitude of pickup and drop-off locations
- Ride timestamp (day, hour, minute)
- Ride Value of each ride

## Project Structure
- **Data Preprocessing**: Cleaned and transformed raw data into features for machine learning. Applied label encoding, ordinal encoding for geohash clusters, and time-based features.
- **Clustering**: K-means clustering was applied to the dataset to group city areas into distinct clusters for efficient prediction and guidance.
- **Modeling**: Three machine learning models (Random Forest, LightGBM, XGBoost) were trained to predict demand based on historical data. Evaluated using metrics like MAE, RMSE, and R2 Score.
- **Driver Guidance System**: Provided real-time guidance to drivers by predicting demand in nearby regions and suggesting the most profitable area to move.

## Technologies Used
- **Python**: For data processing, modeling, and analysis.
- **Scikit-learn**: For clustering and machine learning models.
- **Seaborn & Matplotlib**: For data visualization.
- **Folium**: For geospatial visualizations
- **Google Cloud Storage & BigQuery**: For data storage and querying.

## Future Work
- **Real-time Integration**: Integrating a real-time system to provide instant demand predictions to drivers.
- **A/B Testing**: Implementing experiments to assess the effectiveness of the solution in live operations.
- **POI/District Mapping**: Replacing clusters with meaningful points of interest or districts to improve communication with drivers.
