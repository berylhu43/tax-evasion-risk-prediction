# tax-evasion-risk-prediction
# Tax Evasion Detection with Machine Learning

## 📌 Project Overview

This project aims to identify companies with a higher probability of default or tax evasion using three classification models:

- Linear Probability Model (LPM)
- K-Nearest Neighbors (KNN)
- Logistic Regression

The evaluation uses cross-validation, confusion matrices, and ROC curves to compare predictive power and error rates, with a focus on minimizing false negatives (i.e., companies that actually cheat but are predicted as non-cheaters).

## 📊 Key Findings

- **Linear Probability Model (LPM)**  
  - Threshold 0.5: Error rate = 9.5%, False Negative Rate = 18.24%  
  - Threshold 0.6: Error rate = 11.08%, False Negative Rate = 24.53%

- **KNN Model (Best Performance)**
  - Without Standard Scaler: Error rate = 5.7%, FNR = 9.43%
  - With Standard Scaler: Error rate = 3.6%, FNR = 6.92%
  - Optimal K = 1

- **Logistic Regression**
  - Error rate = 3.86%, False Negative Rate = 4.3%

## 🔍 Model Selection

We chose **KNN with K=1 and standard scaling** for its superior performance. Logistic regression also performed well and provides interpretability.

## ⚠️ Limitations

The data only contains **audited firms**, introducing **selection bias**. Models may not generalize well to unaudited companies or detect emerging fraud patterns.

## 🛠️ How to Run

1. Clone the repository
2. Install required dependencies:
   ```bash
   pip install -r requirements.txt
