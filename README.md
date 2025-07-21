# 🛡️ Fraud Detection Using Machine Learning

This project implements a machine learning pipeline to detect fraudulent financial transactions using a simulated dataset of over 6 million records. The model helps financial institutions proactively identify suspicious behavior and reduce losses due to fraud.

---

## 📁 Dataset Overview

The dataset contains transactional data with the following relevant columns:

- `step`: Hour index of the transaction
- `type`: Type of transaction (PAYMENT, TRANSFER, etc.)
- `amount`: Transaction amount
- `oldbalanceOrg`, `newbalanceOrig`: Sender's balance before and after transaction
- `oldbalanceDest`, `newbalanceDest`: Recipient's balance before and after transaction
- `isFraud`: 1 if the transaction is fraudulent, 0 otherwise

---

## 🧠 Project Workflow

1. **Importing Libraries**
2. **Loading and Exploring the Dataset**
3. **Feature Engineering**
   - Calculate differences in balances
   - Extract time-based features
   - Identify merchant accounts
4. **Preprocessing**
   - Drop irrelevant columns
   - Encode categorical variables
5. **Train-Test Split**
6. **Model Training**
   - Random Forest Classifier with class balancing
7. **Evaluation**
   - Confusion Matrix, Classification Report, ROC-AUC
8. **Feature Importance Analysis**
9. **Fraud Case Extraction**
   - Display all transactions flagged as fraud
10. **Business Q&A Summary**

---

## 🔍 Key Results

- **Model Accuracy**: ~100%
- **Recall for Fraud Class**: ~95%
- **Top Features**: `errorOrig`, `balanceDiffOrig`, `isMerchant`

The model shows strong performance in identifying fraud even with a highly imbalanced dataset.

---

## 📊 Output Highlights

- **Confusion Matrix** and **Classification Report** help validate performance
- **Feature Importance Plot** shows which inputs are most predictive
- **List of Fraud Transactions** provides actionable insights

---

## 💡 Business Insights

- Most fraud occurs during `TRANSFER` and `CASH_OUT` transactions
- Transactions to merchant accounts (`nameDest` starting with "M") are less likely to be fraudulent
- Significant discrepancies between expected and actual balances are strong indicators of fraud

---

## 🧪 Requirements

- Python 3.7+
- Libraries: pandas, numpy, scikit-learn, matplotlib, seaborn

You can install the dependencies using:

```bash
pip install -r requirements.txt
