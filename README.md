# Trust Prediction Using Machine Learning and Explainable AI

## Project Overview

This project predicts consumer trust based on user reviews, ratings, and behavioural features.
The study applies machine learning models and explainable AI to understand how trust is formed and how it can be measured from real-world data.

The dataset consists of 23,465 records with both structured and unstructured data.
The main goal is to classify user trust into two categories: high trust and low trust.

---

## Objectives

* Identify factors influencing consumer trust
* Build a classification model for trust prediction
* Compare multiple machine learning models
* Apply explainable AI techniques to interpret results
* Analyse the role of text and behavioural features

---

## Dataset Description

Dataset Link: 

https://www.kaggle.com/datasets/nicapotato/womens-ecommerce-clothing-reviews  

The dataset includes:

* Age
* Rating
* Review Text
* Title
* Positive Feedback Count
* Product Category (Division, Department, Class)

Target variable:

* **Trust Label**

  * 1 = High Trust
  * 0 = Low Trust

Class distribution:

* High Trust: 77.51%
* Low Trust: 22.49%

---

## Data Preprocessing

* Removed duplicates
* Handled missing values in text fields
* Combined title and review text
* Cleaned text (lowercase, punctuation removal)
* Created features:

  * Review length
  * Title length

---

## Feature Engineering

Features used:

**Numerical**

* Age
* Positive Feedback Count
* Review Length
* Title Length

**Categorical**

* Division Name
* Department Name
* Class Name

**Text**

* Combined review text (TF-IDF representation)

---

## Machine Learning Models

The following models were implemented:

* Logistic Regression
* Random Forest
* XGBoost

---

## Model Performance

| Model               | Accuracy | Precision | Recall | F1 Score | ROC-AUC |
| ------------------- | -------- | --------- | ------ | -------- | ------- |
| Logistic Regression | 0.8788   | 0.8899    | 0.9626 | 0.9248   | 0.9255  |
| Random Forest       | 0.8536   | 0.8565    | 0.9744 | 0.9116   | 0.8983  |
| XGBoost             | 0.8585   | 0.8630    | 0.9717 | 0.9141   | 0.8997  |

**Best Model:** Logistic Regression

---

## Key Findings

* Trust can be predicted with high accuracy
* Text features are the strongest predictors
* Product category has moderate impact
* Demographic features have weak influence
* Models show bias toward high trust

---

## Explainable AI (SHAP)

* SHAP used for feature interpretation
* Text features dominate model decisions
* Individual predictions can be explained
* Trust is influenced by language and sentiment

---

## Ablation Study

* Removing text features reduces accuracy significantly
* Numerical and categorical features have limited impact

Conclusion:
Text is the most important feature for trust prediction

---

## Tools and Technologies

* Python
* Pandas
* NumPy
* Scikit-learn
* XGBoost
* SHAP
* Matplotlib / Seaborn

---

## Project Structure

```
trust-prediction-ml-project/
│
├── data/                # Dataset files
├── notebooks/           # Jupyter notebooks
├── src/                 # Python scripts
├── outputs/             # Charts and results
├── report/              # Final report
└── README.md
```

---

## How to Run

1. Clone repository
2. Install dependencies:

```
pip install -r requirements.txt
```

3. Run notebook:

```
jupyter notebook
```

---

## Conclusion

The project shows that consumer trust can be predicted using machine learning.
Text data plays a key role in capturing trust signals.
Explainable AI helps understand model decisions and improves transparency.

---

## Future Work

* Use domain-specific datasets (e.g., fintech)
* Apply deep learning models (BERT, transformers)
* Improve class imbalance handling
* Include behavioural and interaction data

---

## Author

Cheshta Narang
Master’s Dissertation Project
