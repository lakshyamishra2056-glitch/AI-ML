<div align="center">

# 🍷 Predicting Wine Quality with Machine Learning

### Can chemistry tell you if a wine is actually good?

*An end-to-end ML pipeline that turns 11 chemical measurements into a GOOD/BAD verdict.*

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat&logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-F7931E?style=flat&logo=scikitlearn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data-150458?style=flat&logo=pandas&logoColor=white)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)
![License](https://img.shields.io/badge/License-MIT-yellow)

</div>

---

## 🔍 The Idea

Winemakers have always relied on taste and instinct. This project asks a different question: **do the numbers agree?**

Using acidity, sulphates, alcohol content, and 8 other physicochemical properties, this project builds a classifier that predicts whether a wine is **GOOD** or **BAD** — no tasting required.

---

## 🧪 What's Inside

| Stage | What Happens |
|---|---|
| 🔎 **EDA** | Explore distributions, correlations, and what actually moves the needle on quality |
| 🎯 **Label Engineering** | Convert raw quality scores (0–10) into a binary target — `GOOD` if quality ≥ 7 |
| ⚖️ **Scaling Experiment** | Train Logistic Regression *before* and *after* scaling to prove it actually matters |
| 🥊 **Model Showdown** | Logistic Regression vs. KNN vs. Decision Tree — head to head |
| 🛠️ **Tuning** | GridSearchCV squeezes out extra performance from the best model |
| 🔑 **Feature Importance** | Which chemical properties really drive a great wine? |

---

## 🏆 Key Findings

> 🍾 **Alcohol content and sulphates** are the strongest predictors of a good wine — the data backs up what winemakers have known for years.

> ⚖️ **Scaling isn't optional.** Logistic Regression's performance shifted noticeably once features were put on the same scale — proof that preprocessing decisions matter as much as model choice.

> 🎯 **Accuracy lies (a little).** With good wines as the minority class (~14%), a model that guesses "BAD" every time would still look ~86% accurate. Precision, recall, and F1-score tell the real story.

---

## 📁 Project Structure

```
├── wine_quality_prediction.ipynb   # Full analysis, fully executed with outputs
├── winequality-red.csv             # Dataset (UCI Red Wine Quality)
├── requirements.txt                # Dependencies
└── README.md
```

---

## 🚀 Getting Started

```bash
# Clone the repo
git clone https://github.com/<your-username>/wine-quality-classifier.git
cd wine-quality-classifier

# Install dependencies
pip install -r requirements.txt

# Launch the notebook
jupyter notebook wine_quality_prediction.ipynb
```

---

## 🧰 Tech Stack

`Python` · `Pandas` · `NumPy` · `Matplotlib` · `Seaborn` · `scikit-learn`

---

## 🔮 What's Next

- 🌲 Try ensemble methods (Random Forest, Gradient Boosting, XGBoost)
- ⚖️ Handle class imbalance explicitly (`class_weight="balanced"`, SMOTE)
- 🥂 Extend the analysis to white wine and compare what drives quality across types

---

<div align="center">

*If chemistry can predict quality, maybe your next favorite bottle is just a dataset away.* 🍇

</div>
