# DS 602 – Production Notebook Overview

Notebook Title: Production_Notebook.ipynb  
Authors: Yatharth Kumar & Gelareh Vakili 
Purpose: This notebook demonstrates how to use a trained attrition prediction model to make predictions on new, unlabeled production data. It simulates realistic constraints, including limited SME queries and cluster-based label propagation.

## Contents
- SME class for limited-label querying
- Preprocessing and feature engineering
- KMeans clustering and representative selection
- Label propagation from SME responses
- Model loading and prediction
- Final evaluation against ground truth labels

## Required Libraries
Make sure to install the following libraries:
```bash
pip install pandas numpy scikit-learn joblib
```

## How to Run
1. Place the desired model .pkl file (attrition_model_pipeline.pkl or logreg_sme_model.pkl) in the working directory.
2. Run the notebook from top to bottom.
3. The notebook will print a classification report comparing predictions to the true labels.
