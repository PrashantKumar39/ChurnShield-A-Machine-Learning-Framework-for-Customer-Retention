# ChurnShield A Machine Learning Framework for Customer Retention 
--- 
[![Python](https://img.shields.io/badge/Python-3.11-blue?style=flat-square)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Handling-lightblue?style=flat-square)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/NumPy-Numerical%20Computing-orange?style=flat-square)](https://numpy.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-blueviolet?style=flat-square)](https://matplotlib.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-green?style=flat-square)](https://seaborn.pydata.org/)
[![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-lightgreen?style=flat-square)](https://scikit-learn.org/)
[![XGBoost](https://img.shields.io/badge/XGBoost-ML-lightblue?style=flat-square)](https://xgboost.readthedocs.io/)
[![Google Colab](https://img.shields.io/badge/Google%20Colab-Notebook-red?style=flat-square)](https://colab.research.google.com/)
[![EDA](https://img.shields.io/badge/EDA-Analysis-yellow?style=flat-square)](#)
[![Feature Engineering](https://img.shields.io/badge/Feature%20Engineering-ML-blue?style=flat-square)](#)
[![Data Cleaning & Preprocessing](https://img.shields.io/badge/Data%20Cleaning%20%26%20Preprocessing-Using_Pandas-orange?style=flat-square)](#)
[![Outlier Detection](https://img.shields.io/badge/Outlier%20Detection-ML-red?style=flat-square)](#)
[![MIT License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)
[![Documentation](https://img.shields.io/badge/Documentation-Notes-lightgrey?style=flat-square)](#)

--- 
### Problem Statement:
- The telecom industry faces significant revenue loss due to customer churn, where customers discontinue services. The problem is to predict which customers are likely to churn using historical customer data, enabling the company to implement targeted retention strategies. This is framed as a binary classification problem where the target variable is Churn (Yes/No).

--- 
### Project Overview:

- The Telco Customer Churn Analysis project aims to predict which customers are likely to leave using demographic, service, and account data. I performed data cleaning, exploratory analysis, and feature engineering, including one-hot encoding and tenure-based metrics. I built tree-based models like Decision Tree, Random Forest, and XGBoost, and evaluated them using accuracy, F1-score, and ROC-AUC. The project provides actionable insights for targeted retention strategies, helping reduce churn and improve customer loyalty.


---
## Dataset Information

The dataset contains demographic and service-related details of telecom customers. 
Each record represents a single customer with features describing their account information, service usage, and churn behavior.

### Column Names:
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

---

##  Exploratory Data Analysis (EDA)

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

--- 
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
  
## Technologies & Libraries Used

- **Programming Language:** Python  
- **Libraries:**
  - Data Handling: `Pandas`, `NumPy`
  - Visualization: `Matplotlib`, `Seaborn`
  - Machine Learning: `Scikit-learn`, `XGBoost`
  - Model Evaluation: `classification_report`, `roc_auc_score`, `confusion_matrix`
  - Google Colab for analysis and documentation


---

## Future Work

- Implement **hyperparameter tuning** for optimal model performance.  
- Explore **deep learning models** (e.g., ANN) for enhanced accuracy.  
- Deploy the model as a **web app using Flask or Streamlit**.  
- Incorporate **real-time churn prediction** from live customer data.  
- Add **explainability (SHAP / LIME)** to interpret feature impact.

---
## Conclusion

The analysis successfully identified key drivers of customer churn.  
Customers with **month-to-month contracts**, **higher monthly charges**, and **no online security or tech support** showed a significantly higher likelihood of leaving the service.  
In contrast, **long-term customers** with **annual contracts** and **value-added services** tend to stay loyal.

Among all tested models, the **Random Forest Classifier** demonstrated the highest accuracy and robust generalization across metrics, making it the most reliable for churn prediction.

Overall, this study highlights that **service quality, contract stability, and pricing structure** are critical factors in customer retention.  
Telecom companies can leverage these insights to design **targeted retention campaigns** and **personalized offers**, reducing churn and increasing lifetime value.




---

## **10. Author Information (Optional)**
```md
## Author

Prashant Kumar 
[LinkedIn Profile](https://www.linkedin.com/in/prashant-kumar-ai/)  
📧 Email: prashantkumaryt53@gmail.com.com  

