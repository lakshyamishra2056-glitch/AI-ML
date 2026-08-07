# Predicting Wine Quality with Machine Learning

An end-to-end binary classifier that predicts whether a wine is **GOOD** or **BAD** quality based on its physicochemical properties.

## Dataset
`winequality-red.csv` — UCI Red Wine Quality dataset (1,599 samples, 11 physicochemical features + a quality score from 0–10, rated by wine tasters).

## Problem Framing
The original `quality` score is converted into a binary label:
- **GOOD (1):** quality ≥ 7
- **BAD (0):** quality < 7

This creates an imbalanced classification problem (~14% GOOD), which is why the project leans on precision, recall, and F1-score rather than accuracy alone.

## Workflow
1. **EDA** — distributions, missing values, correlation heatmap
2. **Label engineering** — binary GOOD/BAD target
3. **Scaling impact test** — Logistic Regression trained before vs. after `StandardScaler`
4. **Model comparison** — Logistic Regression vs. KNN vs. Decision Tree
5. **Hyperparameter tuning** — `GridSearchCV` (5-fold CV, optimized for F1-score)
6. **Feature importance** — which physicochemical properties matter most

## Key Results
- **Alcohol content and sulphates** were the strongest predictors of wine quality.
- **Scaling changed Logistic Regression's results measurably** — a clean demonstration of why preprocessing choices matter for gradient-based, scale-sensitive models.
- **Accuracy was misleading** on this imbalanced dataset; F1-score gave a much more honest read on model performance.

## How to Run
```bash
pip install -r requirements.txt
jupyter notebook wine_quality_prediction.ipynb
```

## Files
- `wine_quality_prediction.ipynb` — full analysis, fully executed with outputs and plots
- `winequality-red.csv` — dataset
- `requirements.txt` — dependencies

## Possible Extensions
- Ensemble models (Random Forest, XGBoost, Gradient Boosting)
- Explicit imbalance handling (`class_weight="balanced"`, SMOTE, threshold tuning)
- Extend to the white wine dataset for a cross-type comparison
