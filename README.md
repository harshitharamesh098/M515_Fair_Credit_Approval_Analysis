# Ensuring Fairness in Automated Credit-Card Approval Decisions

## 📘 Project Overview

This project explores the ethical evaluation and bias mitigation in an automated credit-card approval system using machine learning. The core objective is to detect and address unfairness in model predictions, particularly with respect to sensitive attributes such as gender. The work is conducted in partial fulfilment of the requirements for the M515 module: *Ethical Issues for AI*, at Gisma University of Applied Sciences.


## 🧠 Problem Statement

Credit-card approval processes often leverage historical financial and behavioural data. However, these datasets may embed societal biases which, if left unaddressed, can lead to unfair treatment of certain demographic groups. This project formulates the problem as a binary classification task and evaluates fairness using rigorous statistical metrics.

## 🔍 Dataset

Two datasets sourced from Kaggle were used:

- **application_record.csv**: Contains applicant demographic and financial details.
- **credit_record.csv**: Contains historical credit behaviour per applicant.

The datasets were merged using `Customer_ID` and engineered to create a binary target variable (`Credit_Status`) indicating creditworthiness.

## ⚙️ ML Pipeline Steps

1. **Data Loading & Cleaning**: CSV files were read, merged, and cleaned.
2. **Target Generation**: Binary target created from credit history.
3. **Balancing**: Addressed class imbalance via random undersampling.
4. **Feature Engineering**: Encoded categorical features, created age and employment features.
5. **Model Training**: Logistic Regression used for interpretability and transparency.
6. **Fairness Diagnostics**: Evaluated using `CODE_GENDER` with fairness metrics:
   - Statistical Parity Difference
   - Disparate Impact Ratio
   - Equal Opportunity Difference
7. **Results**: No significant gender bias observed. Bias mitigation was deemed unnecessary.

## 📊 Results

| Metric        | Value  |
|---------------|--------|
| Accuracy      | 0.6198 |
| Precision     | 0.6167 |
| Recall        | 0.6167 |
| F1 Score      | 0.6167 |

Fairness diagnostics confirmed equitable treatment across gender:
- **Statistical Parity Difference**: −0.0062
- **Disparate Impact Ratio**: 0.9877
- **Equal Opportunity Difference**: −0.0576

## ✅ Conclusion

The trained model demonstrates balanced performance and fairness without requiring additional mitigation. The study confirms that transparent, interpretable models can be ethically deployed when guided by systematic fairness evaluation.

## 📄 Submission Instructions

- Submitted file: `Fair_Credit_Approval_Analysis_M515.html`
- File size: under 20,000 characters
- Platform: [Canvas LMS](https://canvas.instructure.com/)
- Deadline: **3 July 2025 at 18:00 (Berlin Time)**

## 🔒 Declaration

This submission reflects original work. No generative AI tools were used to produce any component of the final deliverable, in compliance with the academic integrity policies of Gisma University of Applied Sciences.

---

© 2025 Harshita | M515 – Ethical Issues for AI
