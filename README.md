# ChurnShield-A-Machine-Learning-Framework-for-Customer-Retention

- This project analyzes the Telco customer churn dataset to identify the key factors driving customer churn. The main objective is to build a machine learning model that predicts which customers are most likely to churn. Understanding these factors enables the telecommunications company to implement targeted strategies to improve retention and reduce revenue loss. The project includes data cleaning, exploratory data analysis, feature engineering, and evaluation of multiple classification models to determine the most accurate predictor of churn.


## Dataset

The dataset contains information about **customer demographics**, **account details**, and **service usage behavior**.  
It helps analyze factors contributing to **customer churn** and **retention strategies**.

**Key Features:**

- **CustomerID:** Unique identifier for each customer.  
- **Gender:** Gender of the customer.  
- **SeniorCitizen:** Indicates whether the customer is a senior citizen.  
- **Partner:** Whether the customer has a partner.  
- **Dependents:** Whether the customer has dependents.  
- **Tenure:** Number of months the customer has stayed with the company.  
- **PhoneService:** Whether the customer has phone service.  
- **MultipleLines:** Whether the customer has multiple lines.  
- **InternetService:** Type of internet service.  
- **OnlineSecurity:** Whether the customer has online security.  
- **OnlineBackup:** Whether the customer has online backup.  
- **DeviceProtection:** Whether the customer has device protection.  
- **TechSupport:** Whether the customer has tech support.  
- **StreamingTV:** Whether the customer has streaming TV service.  
- **StreamingMovies:** Whether the customer has streaming movie service.  
- **Contract:** Type of contract (Month-to-month, One year, Two year).  
- **PaperlessBilling:** Whether the customer uses paperless billing.  
- **PaymentMethod:** Customer’s preferred payment method.  
- **MonthlyCharges:** Monthly charges billed to the customer.  
- **TotalCharges:** Total amount charged during the customer’s tenure.  
- **Churn:** Indicates whether the customer churned (Yes/No).  


##  Methodology

- The project follows these steps:
- Data Loading and Initial Exploration: The dataset is loaded and an initial assessment is performed to understand its structure, data types, and basic statistics.
- Data Cleaning and Preprocessing: The TotalCharges column is converted to a numeric data type, and missing values are handled by filling them with the median of the column.
- Exploratory Data Analysis (EDA): A detailed analysis of the data is performed to identify patterns and relationships between different features and customer churn.
- Model Building and Evaluation: Several machine learning models are trained on the data to predict customer churn. The performance of these models is then evaluated to select the best one.


## Column-wise Correlation with Churn_Yes


<img width="2969" height="1770" alt="Column-wise Correlation with Churn_Yes" src="https://github.com/user-attachments/assets/71c59e9c-8a67-47c7-a4fd-aadf217b6848" />

## Pairwise Relationships by Churn Status

<img width="1067" height="986" alt="Pairwise Relationships by Churn Status" src="https://github.com/user-attachments/assets/0fda849b-6c72-4170-aab2-3297c1d943df" />


