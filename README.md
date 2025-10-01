# ChurnShield-A-Machine-Learning-Framework-for-Customer-Retention

- This project analyzes the Telco customer churn dataset to identify the key factors driving customer churn. The main objective is to build a machine learning model that predicts which customers are most likely to churn. Understanding these factors enables the telecommunications company to implement targeted strategies to improve retention and reduce revenue loss. The project includes data cleaning, exploratory data analysis, feature engineering, and evaluation of multiple classification models to determine the most accurate predictor of churn.


## 📂 Dataset Information

The dataset contains demographic and service-related details of telecom customers. 
Each record represents a single customer with features describing their account information, service usage, and churn behavior.

### 🧱 Column Names:
- `customerID` — Unique identifier for each customer  
- `gender` — Gender of the customer  
- `SeniorCitizen` — Whether the customer is a senior citizen (1 = Yes, 0 = No)  
- `Partner` — Whether the customer has a partner  
- `Dependents` — Whether the customer has dependents  
- `tenure` — Number of months the customer has stayed with the company  
- `PhoneService` — Whether the customer has phone service  
- `MultipleLines` — Whether the customer has multiple lines  
- `InternetService` — Type of internet service (DSL, Fiber optic, None)  
- `OnlineSecurity` — Whether the customer has online security  
- `OnlineBackup` — Whether the customer has online backup  
- `DeviceProtection` — Whether the customer has device protection  
- `TechSupport` — Whether the customer has tech support  
- `StreamingTV` — Whether the customer has streaming TV  
- `StreamingMovies` — Whether the customer has streaming movies  
- `Contract` — Type of customer contract (Month-to-month, One year, Two year)  
- `PaperlessBilling` — Whether the customer has paperless billing  
- `PaymentMethod` — Customer's payment method  
- `MonthlyCharges` — Monthly amount charged to the customer  
- `TotalCharges` — Total amount charged to the customer  
- `Churn` — Target variable (Yes / No)



## 🔍 Exploratory Data Analysis (EDA)

EDA was performed to understand data patterns, distributions, and relationships between features and churn behavior.

### Key EDA Steps:
1. **Data Cleaning**  
   - Handled missing values in `TotalCharges`.  
   - Converted categorical variables to consistent formats.

2. **Univariate Analysis**  
   - Visualized distributions of `tenure`, `MonthlyCharges`, and `TotalCharges`.  
   - Examined churn percentage across gender, contract type, and internet service.

3. **Bivariate Analysis**  
   - Analyzed correlation between `tenure` and churn rate.  
   - Identified that customers with month-to-month contracts have higher churn rates.

4. **Outlier Detection**  
   - Checked for anomalies in numeric features.

5. **Feature Relationship**  
   - Explored service combinations and their effect on churn.

### Visualizations:
<img width="580" height="432" alt="Visualizing Churn Distribution (Yes vs No)" src="https://github.com/user-attachments/assets/8a0cf167-8a86-48ed-b0bd-3225e39aac77" />

- Churn Distribution (`Churn` value counts)  
- Tenure vs Churn  
- Contract Type vs Churn  
- Heatmap for Feature Correlations  
- Monthly Charges Distribution  

## Column-wise Correlation with Churn_Yes


<img width="2969" height="1770" alt="Column-wise Correlation with Churn_Yes" src="https://github.com/user-attachments/assets/71c59e9c-8a67-47c7-a4fd-aadf217b6848" />

## Pairwise Relationships by Churn Status

<img width="1067" height="986" alt="Pairwise Relationships by Churn Status" src="https://github.com/user-attachments/assets/0fda849b-6c72-4170-aab2-3297c1d943df" />


## Methodology

The project follows a structured machine learning workflow:

1. **Data Preprocessing**
   - Label encoding for categorical variables.
   - Feature scaling (StandardScaler / MinMaxScaler).
   - Train-test split (typically 80-20).

2. **Feature Engineering**
   - Derived new metrics like `AverageChargePerMonth`.
   - Removed highly correlated features to prevent multicollinearity.

3. **Model Selection**
   - Evaluated multiple classification models:
     - Logistic Regression
     - Decision Tree
     - Random Forest
     - Gradient Boosting
     - XGBoost

4. **Model Evaluation**
   - Compared models based on Accuracy, Precision, Recall, F1-score, and ROC-AUC.
   - Visualized Confusion Matrix and ROC Curve.

5. **Final Model**
   - Selected the best-performing model **Random Forest** for churn prediction.

