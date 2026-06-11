Gridlock 2.0 – Traffic Demand Prediction

Overview

This project was developed for Flipkart Gridlock 2.0, an AI/ML hackathon focused on building intelligent mobility solutions for Bengaluru. The objective is to predict traffic demand using historical traffic, road, weather, and location-based data to support smarter urban mobility decisions.

Problem Statement

Traffic congestion is one of the biggest challenges faced by rapidly growing cities. Accurate demand forecasting can help authorities and mobility platforms optimize routing, resource allocation, and congestion management.

The goal is to build a machine learning model capable of predicting traffic demand from road, weather, temporal, and geospatial features.



Dataset Features

The dataset contains information related to:

* Road characteristics
* Weather conditions
* Geospatial location (Geohash)
* Temporal information
* Historical traffic demand



Feature Engineering

Several advanced feature engineering techniques were implemented:

Geohash Decoding

* Converted geohash coordinates into latitude and longitude.
* Extracted geographical information for better spatial learning.

Temporal Features

* Hour-based patterns
* Day-level traffic behavior
* Time-related demand trends

Target Encoding

* Smoothed target encoding for high-cardinality categorical features.
* Reduced noise while preserving category-level information.

Clustering

* K-Means clustering on location features.
* Captured region-wise traffic behavior.

Missing Value Handling

* Mode imputation for categorical variables.
* Appropriate preprocessing for model compatibility.



Models Used

XGBoost Regressor

* Gradient boosting framework optimized for structured data.

LightGBM Regressor

* Fast and efficient tree-based boosting model.

CatBoost Regressor

* Handles categorical features effectively and reduces overfitting.

---

Ensemble Strategy

A weighted ensemble of:

* XGBoost
* LightGBM
* CatBoost

was used to improve prediction robustness and generalization performance.

Additional techniques:

* K-Fold Cross Validation
* Out-of-Fold Predictions
* Pseudo Labeling using high-confidence test predictions



Tech Stack

* Python
* Pandas
* NumPy
* Scikit-Learn
* XGBoost
* LightGBM
* CatBoost



Project Workflow

1. Data Loading
2. Missing Value Treatment
3. Feature Engineering
4. Geohash Decoding
5. Target Encoding
6. Clustering
7. Model Training
8. K-Fold Validation
9. Ensemble Prediction
10. Submission Generation


Results

The ensemble approach significantly improved predictive performance compared to individual models by leveraging the strengths of multiple gradient boosting algorithms.


Repository Structure

├── dataset/
│   ├── train.csv
│   └── test.csv
├── notebooks/
│   └── Gridlock_Traffic_Demand_Prediction.ipynb
├── submission/
│   └── submission.csv
├── README.md
└── requirements.txt

Future Improvement

* Spatio-temporal deep learning models
* Graph Neural Networks (GNNs)
* Advanced geospatial feature extraction
* Automated hyperparameter optimization


