
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



```markdown
# Optimized Neural Network Classification Framework for Scalable Fraud Detection Using Ensemble Anomaly Scores

![Python](https://img.shields.io/badge/Python-3.11-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Latest-green)
![Status](https://img.shields.io/badge/Research-Active-success)

## Abstract

Traditional fraud detection systems often struggle with extreme class imbalance and rapidly evolving fraud patterns. To address these limitations, this project introduces a hybrid anomaly-aware deep learning framework that integrates gradient boosting anomaly scores with multiple neural architectures.

The proposed framework leverages anomaly information extracted from XGBoost, LightGBM, and CatBoost models and feeds these meta-features into deep neural networks for enhanced fraud discrimination.

The study evaluates six architectures:

- Feed Forward Neural Network
- Convolutional Neural Network (CNN)
- Long Short-Term Memory Network (LSTM)
- Autoencoder
- Autoencoder-Based Reconstruction Detector
- Multi-Branch Ensemble Neural Network

---

## Research Motivation

Fraudulent transactions represent only a small fraction of financial activity, making traditional classification models susceptible to majority-class bias.

This work explores whether:

> Ensemble-generated anomaly scores can act as high-level fraud indicators and significantly improve downstream neural network performance.

---

## System Architecture

```text
Raw Transaction Data
         │
         ▼
Data Cleaning & Encoding
         │
         ▼
Feature Scaling
         │
         ▼
Gradient Boosting Layer
 ┌────────┬─────────┬─────────┐
 ▼        ▼         ▼
XGBoost LightGBM CatBoost
 └────────┴─────────┴─────────┘
         │
         ▼
Anomaly Score Generation
         │
         ▼
Enhanced Feature Space
         │
         ▼
Deep Learning Models
 ┌──────┬──────┬──────┬────────┐
 ▼      ▼      ▼      ▼
NN     CNN    LSTM  Ensemble
         │
         ▼
 Fraud Classification
