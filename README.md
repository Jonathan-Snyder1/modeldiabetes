# Diabetes (3-Class) Prediction — Random Forest vs Gradient Boosting

This project builds and evaluates multiclass machine learning models to predict diabetes status using health indicators.

**Classes (target: `Diabetes_012`)**
- 0 = No diabetes
- 1 = Prediabetes
- 2 = Diabetes

## Dataset
Source: Kaggle — Diabetes Health Indicators Dataset (BRFSS 2015)  
(Download from Kaggle and place the CSV in a local `data/` folder — dataset is not committed to this repo, due to kaggle data distribution policies)
https://www.kaggle.com/datasets/alexteboul/diabetes-health-indicators-dataset

## Models
- Random Forest Classifier
- Gradient Boosting Classifier

## Evaluation
Because this is a **3-class classification** problem, evaluation uses:
- Confusion matrix (counts + normalized)
- Precision / Recall / F1 (macro + weighted)
- Accuracy
 <img width="807" height="713" alt="gb boost" src="https://github.com/user-attachments/assets/392a4202-76c3-4c74-a065-abe50d74864d" />
 <img width="722" height="739" alt="rf" src="https://github.com/user-attachments/assets/31873a56-09b7-4ba1-99be-d869b72b5c4d" />


## Key Findings
- Gradient Boosting collapsed the **Prediabetes** class (no predictions for class 1).
- Random Forest produced **non-zero predictions for Prediabetes**, but recall remained low, reflecting overlap in risk factors.

## How to Run
### 1) Install dependencies
```bash
pip install -r requirements.txt
