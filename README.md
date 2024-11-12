# Spotify-Song-Popularity

Project Overview

This project explores factors that influence song popularity on Spotify, leveraging a dataset of audio features to develop predictive models. Using multiple regression methods and tree-based models, the analysis provides insights into the linear and non-linear relationships between song attributes and popularity. The project highlights how features such as acousticness, loudness, and release year contribute to predicting popularity.

Dataset:

The dataset, downloaded via Google Drive, includes over 170,000 songs with key attributes like:

Song Attributes: valence, year, acousticness, artists, danceability, duration_ms, energy, explicit, instrumentalness, key, liveness, loudness, mode, speechiness, tempo

Target: popularity (popularity score between 0 and 100)


Project Goals

Predict Song Popularity: Use various regression techniques to predict a song's popularity score.

Feature Importance Analysis: Identify and interpret the most impactful features influencing song popularity.


Project Workflow

1. Data Preprocessing

Data Cleaning: Checked for missing values, removed unnecessary columns (id, name, release_date, etc.), and one-hot encoded categorical fields (year, explicit, key, and mode).

Scaling: Standardized numerical features to prepare for model training.

2. Regression Models

The project implements several regression techniques to predict song popularity:

Linear Regression: Provided a baseline model with an R-squared of 0.79.

LASSO and Ridge Regression: Enhanced feature selection while slightly lowering R-squared (LASSO: 0.78, Ridge: 0.79).

Elastic Net: Combined properties of LASSO and Ridge with similar results (R-squared: 0.78).

Tree-Based Models:

Regression Tree: Captured non-linear interactions but performed less well with an R-squared of 0.58.

Bagged Forest and Random Forest: Improved non-linear predictions with R-squared values around 0.72.

XGBoost: Achieved the highest R-squared of 0.80, indicating strong performance on the dataset.

3. Model Comparison
   
After training each model, the performance was evaluated using Mean Squared Error (MSE) and R-squared scores. XGBoost emerged as the best performer, indicating some non-linear relationships among features, though linear models like Linear Regression and Ridge showed close accuracy.

4. Feature Importance
   
Feature importances were extracted from each model to understand which attributes most influence song popularity. Key findings include:

Top Features: year, acousticness, loudness, speechiness
Visualization: The top 10 features from the XGBoost model were visualized to illustrate their influence on popularity.

Visualizations

Feature Distribution: Histogram of song release years to explore historical trends.

Heatmap: Correlation heatmap to display relationships among features.

Scatter Plots: Detailed views of important features like year and acousticness against popularity.


Conclusion

The project demonstrates how both linear and non-linear models can be leveraged to predict song popularity. While tree-based models captured some complex interactions, linear models performed competitively, suggesting that song popularity has significant linear relationships with features like release year and acousticness.
