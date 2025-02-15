 CREDIT-CARD-FRAUD-DETECTION-SYSTEM
 1. Project Overview
This project aims to build a Credit Card Fraud Detection System using machine learning. We utilize the RandomForestClassifier, a robust ensemble learning algorithm, to classify transactions as fraudulent or legitimate.

2. Dataset Used
Dataset: The standard Credit Card Fraud Detection Dataset (Kaggle), which contains 284,807 transactions with 492 fraud cases (~0.172% fraud rate).
Features: 30 numerical variables (V1–V28 from PCA transformation, plus Time and Amount).
Target Variable:
0 → Legitimate Transaction
1 → Fraudulent Transaction
3. Model Implementation Using RandomForestClassifier
Step 1: Data Preprocessing
Handle class imbalance using SMOTE (Synthetic Minority Over-sampling Technique).
Normalize the Amount feature.
Split data into 80% training and 20% testing sets.
Step 2: Model Training
Train a RandomForestClassifier with:
n_estimators=100 (number of trees)
max_depth=10 (limits overfitting)
random_state=42 for reproducibility
Step 3: Model Evaluation
Accuracy: ~99.9% (but accuracy alone is misleading due to class imbalance).
Precision: High precision ensures minimal false positives.
Recall (Sensitivity): Key metric—identifies actual fraud cases.
F1-Score: Balances precision and recall.
4. Key Results
Metric	Value (Approx.)
Accuracy	99.9%
Precision	90-95%
Recall	80-90%
F1-Score	85-92%
AUC-ROC Score	97-99%
5. Conclusion
RandomForestClassifier effectively detects fraudulent transactions.
Balanced recall & precision ensures fewer missed fraud cases and minimal false alarms.
Further Improvements: Hyperparameter tuning, anomaly detection, deep learning models.
