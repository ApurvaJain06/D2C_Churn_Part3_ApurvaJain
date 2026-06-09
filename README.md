# D2C_Churn_Part3_ApurvaJain
# Part 3 - Customer Churn Prediction

## Objective

Build a machine learning model to predict customers likely to churn within the next 60 days.

---

## Dataset

Used:

- rfm_modeling_snapshot.csv

Target Variable:

- churn_next_60d

---

## Leakage Prevention

Only snapshot-based features were used.

The target variable and post-snapshot information were excluded from model inputs.

No future customer behavior was used during training.

---

## Models Trained

### Baseline Model

- Logistic Regression

### Final Model

- Random Forest Classifier

Reason for selection:

- Better recall
- Better F1-score
- Better churn detection capability

---

## Final Performance

Approximate Results:

- Accuracy: 0.79
- Precision: 0.76
- Recall: 0.85
- F1 Score: 0.80

Selected Threshold:

- 0.40

The threshold was chosen to prioritize identifying churn-risk customers.

---

## Important Features

Top predictors:

1. recency_days
2. last_visit_days_ago
3. monetary_180d
4. days_since_signup
5. avg_discount_pct_180d

---

## Repository Contents

- churn_model.ipynb
- model.pkl
- metrics.json
- error_analysis.md
- model_card.md
- requirements.txt

---

## Loading Saved Model

```python
import joblib

model = joblib.load("model.pkl")
