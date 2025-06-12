# DS 602 Final Project – Notebook Overview

Notebook Title: DS602_Final_Gelareh V_Yatharth K.ipynb  
Authors: Gelareh Vakili & Yatharth Kumar  
Course: DS 602 – Intro to Data Analysis and Machine Learning  
Purpose: This notebook demonstrates the full pipeline for predicting employee attrition using both a semi-supervised approach and a fully supervised approach. It includes data cleaning, feature engineering, clustering with SME simulation, label propagation, model tuning, evaluation, and .pkl model export.

## Contents
- SME simulation and label propagation using KMeans
- Preprocessing pipelines with imputation, scaling, and encoding
- Logistic Regression and Random Forest models
- GridSearchCV for hyperparameter tuning
- Model evaluation using classification report
- Export of trained models

## Required Libraries
Make sure to install the following libraries:
```bash
pip install pandas numpy scikit-learn joblib
```

## How to Run
1. Run all cells sequentially from top to bottom.
2. Two .pkl models will be generated for downstream use:
   - logreg_sme_model.pkl
   - attrition_model_pipeline.pkl
