# 🍷 Predicting-Youth-Alcohol-Use-A-Decision-Tree-Approach

This project explores how social, behavioral, and demographic factors contribute to alcohol use among youth. Using a real-world survey dataset, we apply decision trees and ensemble learning techniques to predict binary, multiclass, and continuous outcomes of alcohol consumption.

---

## 📁 Project Overview

This project was developed as part of a graduate-level machine learning course focused on tree-based modeling. We aim to:

- Predict whether a youth has consumed alcohol (binary classification)
- Predict frequency of alcohol consumption: Seldom / Sometimes / Frequent (multiclass classification)
- Predict number of alcohol-use days in the past year (regression)

---

## 📊 Dataset

- Source: NSDUH 2023 (National Survey on Drug Use and Health)
- Number of Youth Respondents: ~10,000
- Target Variables:
  - `ALCFLAG`: Has consumed alcohol (Yes/No)
  - `ALCYDAYS`: Frequency of alcohol use (categorical)
  - `IRALCFY`: Number of alcohol-use days (1–365)
- Predictor Categories:
  - Demographics: race, income, poverty status
  - Behavioral: peer use, family support, school engagement
  - Mental Health: emotional stability, past violence

---

## 🧠 Models Used

- Decision Tree (Pruned with `max_leaf_nodes`)
- Bagging with Decision Trees
- Random Forest
- Gradient Boosting
- (for regression) DecisionTreeRegressor, RandomForestRegressor, GradientBoostingRegressor

---

## ⚙️ Techniques & Tools

- Language: Python 3.11  
- Libraries: `scikit-learn`, `pandas`, `seaborn`, `matplotlib`
- Preprocessing:
  - Missing value handling
  - Class rebalancing with `class_weight='balanced'`
  - Feature selection based on domain knowledge and importance scores
- Hyperparameter tuning using `GridSearchCV`
- Evaluation:
  - Classification: Accuracy, F1 Score, Confusion Matrix, ROC-AUC
  - Regression: RMSE, MAE, R² Score
- Visuals:
  - Feature Importance plots
  - Error vs. Tree Size curves
  - ROC curves for binary and multiclass classification

---

## 📌 Key Findings

- **Random Forest** performed best for binary and multiclass prediction tasks.
- **Pruned Decision Tree** gave the best RMSE in regression but had poor R² performance.
- **Top predictors** across all models: grade level (`EDUSCHGRD2`), marijuana use age, peer influence, and race.
- **Challenges**:
  - Class imbalance in multiclass prediction
  - Weak regression prediction power (R² < 0)

---



## 📌 How to Run

``` bash
# Clone repo
git clone https://github.com/your-username/youth-alcohol-use-tree-models.git
cd youth-alcohol-use-tree-models

# Install dependencies
pip install -r requirements.txt

# Run models
python model_binary_classification.py
python model_multiclass_classification.py
python model_regression.py
``` 
--- 

## 📚 References
  - **NSDUH Codebook & Data** – SAMHSA.gov.
  - **Scikit-learn documentation** – https://scikit-learn.org.
  - **Stack Overflow**  – Discussions on ROC-AUC and decision tree pruning
  - **Class Notes & Lecture Slides** – Seattle University, 2025

---

## ✍️ Author

**Sanjay Ramesh Kannan**
**Graduate Student, MS in Data Science**
**Seattle University – Class of 2026**

