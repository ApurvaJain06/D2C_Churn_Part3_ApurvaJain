# Error Analysis

## Overview

The final Random Forest model was evaluated on the test dataset using a probability threshold of 0.40.

The model achieved strong recall while maintaining reasonable precision. However, prediction errors still occur and should be understood before business deployment.

---

## False Positives

False positives are customers predicted as churn risks but who ultimately did not churn.

### Example Customers

| Customer ID | Churn Probability |
|------------|------------------|
| CUST0044 | 0.61 |
| CUST0109 | 0.54 |
| CUST0192 | 0.41 |
| CUST0250 | 0.40 |
| CUST0335 | 0.65 |

### Business Impact

False positives may receive retention offers unnecessarily.

Potential costs include:

- Discount expense
- Marketing campaign cost
- Reduced campaign efficiency

However, business risk is generally moderate because these customers remain active.

---

## False Negatives

False negatives are customers who actually churned but were not identified by the model.

### Example Customers

| Customer ID | Churn Probability |
|------------|------------------|
| CUST0184 | 0.03 |
| CUST0247 | 0.39 |
| CUST0379 | 0.39 |
| CUST0414 | 0.31 |
| CUST0438 | 0.31 |

### Business Impact

False negatives represent lost revenue opportunities.

Potential consequences:

- Customer loss
- Reduced repeat purchases
- Lower customer lifetime value
- Missed retention interventions

False negatives are considered more costly than false positives in churn prediction.

---

## Key Observation

Several false negatives had moderate purchase activity and monetary value, making them difficult to distinguish from retained customers.

Additional behavioral signals such as support interactions, browsing activity, and campaign engagement may improve future model performance.
