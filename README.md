# ML-PROJECT-
Credit Card Fraud Detection System 

1. Introduction 

Credit card fraud is a major financial problem in today’s digital economy. Millions of transactions occur every day and manually monitoring them is not possible. Fraudulent transactions are very rare compared to legitimate ones, but they can cause huge financial losses if not detected in time. Therefore, an automatic and intelligent fraud detection system is required. 

This project implements an end-to-end Machine Learning based Credit Card Fraud Detection System. The system can learn from historical transaction data and predict whether a new transaction is fraudulent or legitimate. The project also includes handling of class imbalance, proper evaluation, and an automatic testing mechanism for easy demonstration. 

 

2. Project Objective 

The main objectives of this project are: 

To detect fraudulent credit card transactions using Machine Learning 

To handle the highly imbalanced nature of fraud datasets 

To train a robust classification model for fraud detection 

To evaluate the model using appropriate performance metrics 

To provide an easy-to-use testing interface without manual feature entry 

This project is designed to demonstrate an end-to-end ML pipeline, from data preprocessing to model deployment-style testing. 

 

3. Dataset Description 

The dataset used in this project is creditcard.csv, which contains real-world anonymized credit card transaction data. 

Dataset Characteristics: 

Total transactions: 284,807 

Fraudulent transactions: 492 

Legitimate transactions: 284,315 

Target column: Class 

0 = Legitimate Transaction 

1 = Fraudulent Transaction 

Features: 

Time: Time elapsed between transactions 

V1 – V28: Anonymized numerical features (PCA transformed) 

Amount: Transaction amount 

The dataset is highly imbalanced, making it unsuitable for direct training without imbalance handling. 

 

4. System Architecture and Pipeline 

This architecture ensures that the system is scalable, accurate, and suitable for real-world fraud detection scenarios. The overall system follows the pipeline shown below: 

Raw Transaction Data 
       ↓ 
Data Preprocessing & Scaling 
       ↓ 
SMOTE (Class Imbalance Handling) 
       ↓ 
Random Forest Model Training 
       ↓ 
Model Evaluation 
       ↓ 
Automatic Transaction Testing 
 

 

5. Data Preprocessing 

1. Feature and Target Separation 

The target variable Class is separated from the feature set. All remaining columns are used as input features. 

2. Feature Scaling 

Since the dataset contains features with different ranges (e.g., Amount and PCA features), StandardScaler is used to normalize the data. This improves model stability and performance. 

5.3 Handling Class Imbalance using SMOTE 

Due to extreme class imbalance, SMOTE (Synthetic Minority Oversampling Technique) is applied. SMOTE generates synthetic fraud samples to balance the dataset, allowing the model to learn fraud patterns effectively. 

 

6. Model Design 

Random Forest Classifier 

A Random Forest Classifier is used as the main prediction model. 

Reasons for choosing Random Forest: 

Works well with tabular data 

Handles non-linear relationships 

Reduces overfitting using ensemble learning 

Provides high accuracy and robustness 

Model parameters: 

Number of trees: 100 

Random state set for reproducibility 

 

7. Model Evaluation 

The trained model is evaluated using multiple metrics to ensure reliable fraud detection. 

Evaluation Metrics: 

Accuracy 

Precision 

Recall 

F1-score 

Confusion Matrix 

Special emphasis is placed on Recall, as missing a fraud transaction is more costly than falsely flagging a legitimate one. 

Confusion Matrix 

The confusion matrix visually represents: 

True Positives (Correctly detected frauds) 

True Negatives (Correctly detected legitimate transactions) 

False Positives 

False Negatives 

This provides a clear understanding of model performance. 

 

8. Automatic Transaction Testing Interface 

To improve usability and demonstration speed, an automatic transaction testing mechanism is implemented. 

Key Features: 

No need to manually enter 30 transaction values 

Random transaction selection from dataset 

Fraud-only and smart mixed testing options 

Real-time prediction output 

This makes the system user-friendly and suitable for live demonstrations. 

 

9. Input and Output Description 

Input: 

A single credit card transaction (automatically selected from dataset) 

Output: 

Legitimate Transaction 

Fraudulent Transaction Detected 

The system clearly displays both the actual class and the model prediction. 

 

10. Challenges and Limitations 

Challenges: 

Extremely imbalanced dataset 

Risk of overfitting after oversampling 

Fraud patterns may evolve over time 

Limitations: 

Model trained on historical data only 

Real-world deployment would require continuous retraining 

Dataset features are anonymized, limiting interpretability 

 

 

 

11. Ethical Considerations 

No real customer identities are used 

The system is intended for decision support, not as a replacement for human judgment 

False positives may inconvenience customers, so model thresholds should be chosen carefully 

 

12. Conclusion 

This project successfully demonstrates an end-to-end Credit Card Fraud Detection System using Machine Learning. By handling class imbalance with SMOTE and using a Random Forest classifier, the system achieves high performance in detecting fraudulent transactions. The inclusion of an automatic testing interface and confusion matrix visualization makes the project practical, professional, and suitable for real-world applications. 
