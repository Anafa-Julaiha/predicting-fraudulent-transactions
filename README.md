# Predicting Fraudulent Transactions Project

This project focuses on predicting fraudulent transactions in a financial dataset using **machine learning techniques**. A **Random Forest Classifier** is employed to identify fraudulent transactions based on historical data.

## Table of Contents
1. [Overview](#overview)
2. [Dataset](#dataset)
3. [Installation](#installation)
4. [Project Structure](#project-structure)
5. [Data Preprocessing](#data-preprocessing)
6. [Model Training and Evaluation](#model-training-and-evaluation)
7. [Results](#results)

## Overview

The primary goal of this project is to detect fraudulent transactions in a large dataset of financial transactions. We used a **supervised machine learning** approach, with **Random Forest** as the classification model. The model was trained on a set of features extracted from the dataset, such as **transaction amount**, **old balance**, and **transaction type**.

## Dataset

The dataset consists of over **6 million** financial transactions, including various transaction types such as **PAYMENT**, **TRANSFER**, **CASH_OUT**, etc. Each row represents a transaction and contains the following columns:

- `step`: Step of transaction (represents time)
- `type`: Type of transaction
- `amount`: Amount of transaction
- `oldbalanceOrg`: Original balance before the transaction
- `newbalanceOrig`: New balance after the transaction
- `oldbalanceDest`: Destination balance before the transaction
- `newbalanceDest`: Destination balance after the transaction
- `isFraud`: Whether the transaction is fraudulent (1 for fraud, 0 for non-fraud)
- `isFlaggedFraud`: Whether the transaction is flagged as fraud by the system

## Installation

To run this project, you will need to install the required dependencies. Follow these steps:

## 4. Project Structure

**fraud_detection.py**: Main script for **data processing**, **model training**, and **evaluation**.  
**Fraud.csv**: The dataset used in the project (if shared).  
**README.md**: Project documentation.

## 5. Data Preprocessing

Before training the model, the dataset requires several **preprocessing steps**. The **data_preprocessing.py** script handles all **data cleaning** and **feature engineering** tasks.

**Key Steps**:
- **Handling Missing Values**: We checked for and imputed missing values where necessary.
- **Removing Irrelevant Columns**: Columns like **nameOrig** and **nameDest** were dropped as they don't contribute meaningfully to predicting fraud.
- **Feature Encoding**: The **type** column, which is categorical (e.g., CASH_OUT, PAYMENT), was **one-hot encoded** to transform it into numerical values for modeling.
- **Feature Scaling**: Numeric features were scaled using **StandardScaler** to ensure all features have equal importance during model training.
- **Outlier Removal**: We applied the **Interquartile Range (IQR)** method to detect and remove outliers, especially for columns like **amount** and **oldbalanceOrg**.

## 6. Model Training and Evaluation

### Model Selection:
We used **Random Forest Classifier** for this project because it is well-suited for **large datasets** and provides interpretable **feature importance**.

### Steps:
- **Data Splitting**: The dataset was split into **training (70%)** and **test (30%)** sets.
- **Model Training**:  
  - A **Random Forest Classifier** was trained using **100 trees (estimators)**.
  
### Evaluation Metrics:
- **Accuracy**: Measures how often the classifier correctly identifies fraud.
- **ROC AUC Score**: Balances the trade-off between true positives and false positives.
- **Confusion Matrix**: Visualizes performance with counts of **true/false positives** and **negatives**.

## 7. Results

The model achieved the following results:
- **Accuracy**: 0.9996594701355309
- **ROC AUC Score**: 0.8802311189948779

A **confusion matrix** and **classification report** were also generated to further evaluate the performance of the model.




1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/predicting-fraudulent-transactions.git
   cd fraud-detection
