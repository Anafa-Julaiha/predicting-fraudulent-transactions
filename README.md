#predicting fraudulent transactions project

This project focuses on predicting fraudulent transactions in a financial dataset using machine learning techniques. A **Random Forest Classifier** is employed to identify fraudulent transactions based on historical data.

## Table of Contents
1. [Overview](#overview)
2. [Dataset](#dataset)
3. [Installation](#installation)
4. [Project Structure](#project-structure)
5. [Data Preprocessing](#data-preprocessing)
6. [Model Training and Evaluation](#model-training-and-evaluation)
7. [Results](#results)
8. [Next Steps](#next-steps)

## Overview

The primary goal of this project is to detect fraudulent transactions in a large dataset of financial transactions. We used a supervised machine learning approach, with **Random Forest** as the classification model. The model was trained on a set of features extracted from the dataset, such as transaction amount, old balance, and transaction type.

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

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/predicting-fraudulent-transactions.git
   cd fraud-detection
