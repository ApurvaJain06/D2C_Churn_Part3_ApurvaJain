# Model Card

## Model Name

D2C Customer Churn Prediction Model

---

## Intended Use

Predict customers likely to churn within the next 60 days.

The model is intended to support:

- Customer retention campaigns
- Marketing prioritization
- Customer success interventions

---

## Data Used

Dataset:

- rfm_modeling_snapshot.csv

Target Variable:

- churn_next_60d

Features include:

- Recency
- Frequency
- Monetary value
- Web activity
- Support behavior
- Campaign engagement

---

## Leakage Prevention

Only snapshot-based features were used.

The target variable was excluded from model inputs.

No future customer activity was used during training.

---

## Model Approach

Baseline Model:

- Logistic Regression

Final Model:

- Random Forest Classifier

Reason for selection:

- Better recall
- Better F1-score
- Ability to capture nonlinear relationships

---

## Performance

Approximate Test Performance:

- Accuracy: 0.79
- Precision: 0.76
- Recall: 0.85
- F1 Score: 0.80

Decision Threshold:

- 0.40

The threshold was selected to prioritize churn detection.

---

## Limitations

- Historical data only
- Customer behavior may change over time
- Performance may degrade if business conditions change
- False positives and false negatives remain possible

---

## Ethical Risks

Potential risks include:

- Unequal treatment of customer groups
- Excessive targeting of specific customers
- Misuse of predictions for exclusion decisions

Predictions should support business decisions rather than fully automate them.

---

## Monitoring Requirements

The model should be monitored for:

- Recall degradation
- Precision degradation
- Data drift
- Feature distribution changes
- Campaign effectiveness

Recommended monitoring frequency:

- Monthly

---

## When Not To Use

The model should not be used for:

- Credit decisions
- Employment decisions
- Identity verification
- High-stakes automated actions

Human review should remain part of the decision process.
