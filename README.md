# Fraud Detection Using Ensemble Learning and Deep Learning

## Overview
This project focuses on fraud detection using multiple machine learning and deep learning approaches. The dataset contains transaction information along with anomaly scores generated from XGBoost, LightGBM, and CatBoost models.

Several neural network architectures were trained and evaluated to classify fraudulent transactions.

## Models Implemented

1. Feed Forward Neural Network
2. Autoencoder
3. CNN
4. LSTM
5. Autoencoder + Isolation Forest
6. Ensemble Neural Network

## Dataset

The dataset contains:

- Transaction features
- Card information
- Address information
- Product information
- Engineered anomaly scores:
  - xgb_anomaly_score
  - lgbm_anomaly_score
  - catboost_anomaly_score

Target Variable:

```text
isFraud
