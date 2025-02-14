# Multiclass Classification for Air Quality Index Prediction

## Overview 
This project focuses on predicting the Air Quality Index (AQI) using multiclass classification based on pollutant concentrations. Given the increasing concerns regarding air pollution and its impact on public health, this study classifies AQI into three categories: Good, Moderate, and Poor.

## Dataset
1. Source: Kaggle - Publicly available air quality data from one of the most polluted cities in the world.
2. Timeframe: 2015 - 2020
3. Features:
Pollutants: PM2.5, PM10, NO, NO2, NOx, O3, CO
Meteorological factors: Temperature, Humidity, Wind Speed
4. Records: 18,205 observations

## Problem Statement
Traditional AQI forecasting methods rely on empirical formulas, which can be ineffective in predicting future conditions. This project leverages Supervised Machine Learning Classification Models to improve prediction accuracy and generate meaningful insights for public health advisories and environmental regulations.

## Models Implemented
The following multiclass classification models were explored:

| **Model** | **Accuracy** |
|-----------|-------------|
| Gaussian Naive Bayes (Baseline) | 61% |
| K-Nearest Neighbor (KNN) | **80%** |
| Logistic Regression | 67% |
| Logistic Regression with SMOTE | 70% |
| Logistic Regression with Stacking (RF+LR) | **79%** |
| Support Vector Machine (SVM) | 74% |
| SVM (Tuned with Grid Search) | 76% |

1. Best Model: KNN achieved the highest performance with an accuracy of 80%, precision of 0.86, and recall of 0.81.
2. Stacking Ensemble: A combination of Random Forest (base estimator) and Logistic Regression (final estimator) improved accuracy by 18%.

## Data Preprocessing & Feature Engineering
1. Data Imbalance Handling: Used SMOTE (Synthetic Minority Over-sampling Technique) to balance the dataset.
2. Feature Selection: Correlation matrix was used to identify the most significant features affecting AQI.
3. Hyperparameter Tuning: Grid search cross-validation was applied to optimize models.
4. Normalization & Encoding: Applied standard scaling and label encoding for categorical variables.

## Unsupervised Learning Approach
Apart from classification, K-Means Clustering was performed to analyze underlying patterns in pollutant levels:

1. **Cluster 1**: High NOx & CO – Heavy traffic areas.
2. **Cluster 2**: High PM2.5 & PM10 – Industrial zones.
3. **Cluster 3**: Low pollution – Well-regulated zones.

## Key Findings
1. KNN was the most effective classifier with 80% accuracy.
2. Stacking (RF + Logistic Regression) improved classification by 18%.
3. SMOTE helped handle class imbalance, improving performance.
4. K-Means Clustering identified distinct pollution profiles for targeted interventions.
