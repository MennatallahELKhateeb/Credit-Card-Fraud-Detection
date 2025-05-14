# Credit-Card-Fraud-Detection
About the Dataset
This dataset contains credit card transactions made by European cardholders in September 2013.
It includes transactions over two days, with 492 fraudulent cases out of 284,807 total transactions.
The dataset is highly imbalanced, and all features are numerical due to a PCA transformation for confidentiality.

Target Variable: Class — 0 = Not Fraud, 1 = Fraud

Total Records: 284,807

Fraudulent Transactions: 492 (approximately 0.17%)

Project Goal
To build a machine learning model capable of detecting fraudulent transactions with high accuracy despite significant class imbalance, helping prevent financial loss and protect customer accounts.

Insights
Severe Class Imbalance

Only 0.17% of the data represents fraud. Without balancing, most models would default to predicting non-fraud and appear highly accurate while missing real frauds.

Feature V14 is Highly Predictive

Based on feature importance from the trained model, V14 shows a strong ability to distinguish fraudulent from legitimate transactions.

Model Performance (Random Forest + SMOTE):

AUC Score: 0.97
![image](https://github.com/user-attachments/assets/3ee3fa0b-36ce-4982-b967-3580c2536795)

Precision (Fraud): 83%

Recall (Fraud): 83%

Very few false negatives, indicating strong fraud detection capability

Techniques Used
Data Cleaning (dropna)

Handling Class Imbalance using SMOTE

Model Training with RandomForestClassifier

Evaluation with Confusion Matrix, Classification Report, and ROC Curve

Feature Importance Analysis and Distribution Plots
![image](https://github.com/user-attachments/assets/c6eda341-87f2-4aca-bf2f-e5879c98806c)
![image](https://github.com/user-attachments/assets/2785ad6b-cc61-4648-9906-2c7e58133b3f)

Recommendations
Closely monitor key features like V14 in real-time systems to flag high-risk transactions.
![image](https://github.com/user-attachments/assets/ac275aaf-554e-4649-b445-b51bc3b6942e)

Regularly retrain and validate the model to adapt to new fraud behaviors and data drift.

Integrate model predictions into fraud detection pipelines with manual review for edge cases.

Consider further optimization using models like XGBoost or LightGBM.

