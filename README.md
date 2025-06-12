# 🏢 Employee Attrition Prediction with Semi-Supervised Learning

Predicting which employees are likely to leave is crucial for organizations, as hiring and training new staff is resource-intensive. This project tackles the challenge of employee attrition prediction using a semi-supervised approach, making the most of limited expert (SME) labeling capacity.

---

## 🚀 Project Overview

- **Dataset:** 50,000+ employee records with engineered features
- **Labeling Constraint:** SME can only provide labels for 500 records (returns "yes" or "no" for attrition)
- **Goal:** Accurately predict employee attrition, prioritizing recall to minimize missed true attrition cases

---

## 🧠 Methodology

### 1. Feature Engineering
- Extracted and engineered features relevant to employee behavior, performance, and engagement.

### 2. K-Means Clustering for Efficient Labeling
- Trained a K-Means clustering model with **n = 500** clusters on the feature set.
- For each cluster, identified the record **closest to the cluster center**.
- Queried the SME for labels on these 500 central records.

### 3. Label Propagation
- Propagated the SME-provided label from each cluster center to all members of that cluster.
- Result: All 50,000+ records are now labeled, leveraging only 500 SME queries.

### 4. Supervised Model Training
- Trained multiple supervised learning models (e.g., Logistic Regression, Random Forest, XGBoost) on the fully labeled dataset.

### 5. Model Selection & Evaluation
- **Model Selected**- Logistic Regression
- **Primary Metric:** Recall  
  High recall is prioritized because missing a potential attrition case is costlier than a false positive.
- Compared models and selected the one with the highest recall on a held-out test set.

---

## ⚙️ Workflow

Raw Employee Data
↓
Feature Engineering
↓
K-Means Clustering (n=500)
↓
Select Cluster Centers
↓
SME Labeling (500 queries)
↓
Label Propagation to Clusters
↓
Supervised Model Training
↓
Model Evaluation (Recall)


---

## 📊 Results

- Efficiently labeled a large dataset with minimal SME involvement
- Achieved high recall, ensuring most employees likely to leave are identified
- Reduced labeling cost and SME workload by 99%

---

## 🏆 Key Takeaways

- **Semi-supervised learning** can dramatically reduce expert labeling requirements in large datasets
- **Clustering + label propagation** is a practical strategy when SME time is limited
- **Recall-focused evaluation** aligns the model with real business priorities

---

## 💡 Future Work

- Explore more advanced label propagation techniques (e.g., graph-based methods)
- Incorporate active learning to further optimize SME queries
- Deploy the model as an internal HR tool for real-time attrition risk monitoring

## 🤝 Contributions

Questions or suggestions? Open an issue or submit a pull request!

---

> **Data-driven insights for smarter HR decisions.**
