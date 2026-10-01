# Customer Transaction Prediction

## 📌 Project Overview

This project focuses on predicting whether a customer is likely to make a transaction using machine learning classification algorithms.

The dataset contains customer-related numerical features and a binary target variable. Since the target variable is imbalanced, appropriate preprocessing and balancing techniques were applied before training the models.

The main objective is to build and compare multiple classification models and identify a candidate model for further validation and potential deployment.

---

## 🎯 Problem Statement

The goal of this project is to predict whether a customer will make a transaction based on the available customer features.

This can help businesses identify potential customers who are more likely to transact and support data-driven customer targeting strategies.

---

## 📊 Dataset

The project uses the `train(1).csv` dataset.

- Target variable: `target`
- `0` → Customer is not expected to make a transaction
- `1` → Customer is expected to make a transaction

The target variable was initially imbalanced, so the training data was balanced before model training.

---

## 🔧 Project Workflow

The project follows these major steps:

1. Import required libraries
2. Load the dataset
3. Understand the dataset
4. Check data types and missing values
5. Perform exploratory data analysis
6. Separate features and target
7. Analyze target class imbalance
8. Split data into training and testing sets
9. Balance the training data
10. Scale the features
11. Train multiple classification models
12. Evaluate model performance
13. Calculate ROC-AUC scores
14. Compare the models
15. Select a candidate model
16. Document challenges and solutions
17. Provide conclusions and future improvements

---

## 🤖 Machine Learning Models

The following classification algorithms were implemented and compared:

- Logistic Regression
- Random Forest Classifier
- XGBoost Classifier
- Linear SVM
- Decision Tree Classifier
- Gradient Boosting Classifier

---

## 📈 Model Performance

| Model | Accuracy | Class 1 Precision | Class 1 Recall | Class 1 F1-score | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Logistic Regression | 0.7827 | 0.29 | 0.77 | 0.42 | 0.8584 |
| Random Forest | 0.7494 | 0.24 | 0.70 | 0.36 | 0.8050 |
| XGBoost | 0.7824 | 0.28 | 0.72 | 0.40 | 0.8366 |
| Linear SVM | 0.7829 | 0.29 | 0.77 | 0.42 | 0.8583 |
| Decision Tree | 0.7084 | 0.17 | 0.47 | 0.25 | 0.6282 |
| Gradient Boosting | 0.7726 | 0.26 | 0.71 | 0.38 | 0.8269 |

---

## 🏆 Candidate Model

**Logistic Regression** was selected as the candidate model for further validation and potential deployment.

It achieved:

- Accuracy: **78.27%**
- Class 1 Precision: **0.29**
- Class 1 Recall: **0.77**
- Class 1 F1-score: **0.42**
- ROC-AUC: **0.8584**

Logistic Regression and Linear SVM produced very similar results. Logistic Regression was retained as the candidate model because it provides comparable predictive performance while being relatively simple and interpretable.

Further validation using unseen or real-world business data is recommended before deployment.

---

## ⚠️ Challenges & Solutions

### 1. Class Imbalance

The target variable was imbalanced, which could affect the model's ability to identify the minority class.

**Solution:**  
The training data was balanced before model training while keeping the test data representative of the original distribution.

### 2. Feature Scaling

Some algorithms such as Logistic Regression and Linear SVM are sensitive to feature scales.

**Solution:**  
Feature scaling was applied using the training data and the same transformation was applied to the test data.

### 3. Model Selection

Different models produced different performance across accuracy, recall, F1-score, and ROC-AUC.

**Solution:**  
Multiple classification algorithms were trained and evaluated using several performance metrics rather than relying only on accuracy.

---

## 📌 Evaluation Metrics

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion Matrix

Because the dataset is imbalanced, particular attention was given to **Class 1 recall, F1-score, and ROC-AUC** instead of relying only on accuracy.

---

## 🔮 Future Improvements

- Perform hyperparameter tuning
- Explore additional feature engineering techniques
- Evaluate additional ensemble models
- Perform cross-validation
- Test the candidate model on new unseen business data
- Optimize the classification threshold based on business requirements
- Deploy the validated model as an API or web application

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost
- Jupyter Notebook

---

## 📁 Project Structure

```text
Customer_transaction_prediction/
│
├── Customer_transaction_prediction.ipynb
├── train(1).csv
└── README.md
