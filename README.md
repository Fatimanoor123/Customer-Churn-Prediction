# 📉 Customer Churn Prediction (Telco Dataset)

This project predicts whether a customer will churn (leave the service) using the Telco Customer Churn dataset from Kaggle. It includes data preprocessing, correlation analysis, feature scaling, model training, and evaluation using Python and machine learning libraries.

---

## 📁 Dataset

- **Name**: Telco Customer Churn
- **Source**: [Kaggle Dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- **Target Variable**: `Churn` (Yes/No)

---

## 🧠 Objective

To build a machine learning pipeline that:
- Handles missing values
- Encodes categorical variables
- Performs correlation analysis
- Scales numerical features
- Trains a predictive model
- Evaluates model performance

---

## ⚙️ Technologies Used

- Python 🐍
- Pandas
- NumPy
- Scikit-learn
- Seaborn
- Matplotlib

---

## 🗂️ Project Structure

```bash
.
├── Telco-Customer-Churn.csv         # Dataset file
├── churn_prediction.py              # Python script for entire project
└── README.md                        # Project documentation
```



## 🔍 Steps Performed

### 1. Load Dataset
The Telco Customer Churn dataset is loaded using `pandas`.

### 2. Handle Missing Values
- The `TotalCharges` column is converted from string to numeric using `pd.to_numeric`.
- Missing values (if any) are filled with the column's mean using `fillna()`.

### 3. Encode Categorical Variables
- The `customerID` column is dropped as it is not useful for prediction.
- Categorical features are converted to numerical format using one-hot encoding via `pd.get_dummies()` with `drop_first=True` to avoid multicollinearity.

### 4. Correlation Analysis
- Pearson correlation is computed using `.corr()` to find how each feature relates to the target variable `Churn_Yes`.
- A heatmap is visualized using `seaborn.heatmap()` to analyze feature relationships.

### 5. Feature Scaling
- Features are standardized using `StandardScaler()` from Scikit-learn to ensure that all variables contribute equally to the model.

### 6. Model Training
- The data is split into training and testing sets using `train_test_split()`.
- A Logistic Regression model is trained using the training set.

### 7. Model Evaluation
- The trained model is used to make predictions on the test set.
- The model performance is evaluated using:
  - **Confusion Matrix**
  - **Classification Report**: Includes precision, recall, F1-score, and support.













