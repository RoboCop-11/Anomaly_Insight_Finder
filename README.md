
---

# Version 2 — Better README

```markdown
# Hybrid Fraud Detection Framework Using Ensemble Anomaly Scores and Deep Learning

## Introduction

Financial fraud detection remains one of the most challenging problems due to severe class imbalance and constantly evolving attack patterns.

This project proposes a hybrid fraud detection framework that combines:

- Gradient Boosting based anomaly scores
- Deep Learning classifiers
- Autoencoder-based anomaly detection
- Neural Network ensembles

The objective is to improve fraud detection performance by leveraging anomaly information generated from multiple boosting algorithms.

---

## Dataset Features

The dataset consists of transaction-level information including:

### Transaction Features

- TransactionDT
- TransactionAmt
- ProductCD

### Card Features

- card1–card6

### Address Features

- addr1
- addr2

### Behavioral Features

- M1–M9

### Generated Meta Features

The following anomaly scores are generated using previously trained models:

- XGBoost Anomaly Score
- LightGBM Anomaly Score
- CatBoost Anomaly Score

These scores serve as high-level indicators of suspicious behavior.

---

## Project Architecture

```text
Transaction Data
        │
        ▼
Feature Engineering
        │
        ▼
Gradient Boosting Models
(XGB + LGBM + CatBoost)
        │
        ▼
Anomaly Scores
        │
        ▼
Deep Learning Models
        │
 ┌──────┼──────┐
 ▼      ▼      ▼
NN     CNN    LSTM
 │      │      │
 └──────┼──────┘
        ▼
 Fraud Prediction
