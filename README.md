# Credit Card Fraud Detection Analysis  
  
This repository contains an analysis of the credit card transactions dataset. The dataset was originally loaded from `creditcard.csv` and consists of 284,807 rows and 31 columns. The analysis focused on exploring the data, class distribution, feature significance, and applying machine learning techniques to detect fraudulent transactions.  
  
## Table of Contents  
- [Overview](#overview)  
- [Data Exploration](#data-exploration)  
- [Handling Class Imbalance](#handling-class-imbalance)  
- [Modeling](#modeling)  
- [Conclusions](#conclusions)  
- [Repository Structure](#repository-structure)  
- [References](#references)  
  
## Overview  
The dataset includes features `V1` through `V28` which have been transformed using PCA for confidentiality and the `Amount` and `Time` features. The target feature is `Class`, where a value of 1 indicates a fraudulent transaction and 0 otherwise.  
  
We began our analysis by checking the shape of the dataset and the distribution of the `Class` label. For example, one of the early outputs can be referenced as:    
(284807, 31)  
  
&nbsp;  
 ## Data Exploration  
- **Dataset Shape:** The dataset contains 284,807 transactions and 31 columns.    
- **Class Distribution:** The class imbalance was significant. This was verified with the value counts (e.g., see output:
  Handling Class Imbalance
Due to the extreme imbalance in the class distribution, multiple approaches such as oversampling (using SMOTE) and the use of boosting was attempted. Ultimately, the Logistic Regression model was trained with balanced class weights to better handle the skewed data distribution.

## Modeling
A Logistic Regression model was implemented, and its performance was evaluated on the test set. The classification report and ROC-AUC scores were computed for further evaluation. The classifier was also boosted to exhibit robust performance despite the imbalanced classes.

## Conclusions
The dataset shows significant imbalance which was addressed via class weighting.
The XGBOOST model provided decent performance in detecting fraudulent transactions.
Feature importance analysis is critical to understand the underlying factors influencing fraud

## Repository Structure
README.md : This file.
creditcard.csv : The dataset.
analysis_notebook.ipynb : Jupyter Notebook containing the analysis.
Additional scripts or notebooks as needed.
## References
The outputs and intermediate steps can be referenced from the outputs stored during the analysis such as:
Dataset shape: (284807, 31)
