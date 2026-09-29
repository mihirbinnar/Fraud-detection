# Credit Card Fraud Detection System

A machine learning-based credit card fraud detection system that identifies unusual customer transaction behavior using **Isolation Forest**, an unsupervised anomaly detection algorithm.

The project processes credit card customer data, scales relevant financial features, detects anomalous behavior, and provides an interactive **Gradio interface** for making fraud predictions.

## 📌 Overview

Credit card fraud can be identified by detecting transaction patterns that significantly differ from normal customer behavior.

This project uses **Isolation Forest** to detect such unusual patterns without requiring a pre-labeled fraud dataset.

The model analyzes features such as:

- Customer balance
- Purchases
- Cash advances
- Credit limit
- Payments
- Account tenure

The system classifies the input as either:

- ⚠️ **Fraud Detected**
- ✅ **Normal Transaction**

## 🚀 Features

- Unsupervised fraud/anomaly detection
- Isolation Forest machine learning model
- Missing-value handling
- Feature standardization using `StandardScaler`
- Automatic anomaly labeling
- Trained model saved using Joblib
- Interactive Gradio interface
- Real-time prediction for user-provided transaction information

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Joblib
- Gradio
- Jupyter Notebook

### Machine Learning

- `StandardScaler`
- `IsolationForest`

## ⚙️ How It Works

The project follows these steps:

1. **Load Dataset**
   - The `CC GENERAL.csv` dataset is loaded using Pandas.

2. **Data Exploration**
   - Dataset shape, data types, statistical information, and missing values are examined.

3. **Data Preprocessing**
   - `CUST_ID` is removed because it is not useful as a machine learning feature.
   - Missing numerical values are replaced with their mean.

4. **Feature Selection**
   - Six features are used for the fraud detection model:

```text
BALANCE
PURCHASES
CASH_ADVANCE
CREDIT_LIMIT
PAYMENTS
TENURE
