# Telecom Customer Churn Prediction

## Overview
This project aims to predict customer churn in the telecom industry by analyzing customer behavior and demographic information. The dataset includes key customer features, such as service usage, contract types, and more, to identify factors influencing customer retention. By applying machine learning techniques, including feature preprocessing and classification, the goal is to build a predictive model to determine whether a customer will churn.

## Dataset
[The dataset](https://www.kaggle.com/datasets/abdullah0a/telecom-customer-churn-insights-for-analysis), sourced from Kaggle, provides a comprehensive view of customer demographics and service usage, crucial for understanding customer retention and churn. The dataset is licensed under the MIT license.

## Key Features:
- CustomerID: Unique identifier for each customer.
- Age: Age of the customer.
- Gender: Gender of the customer (Male or Female).
- Tenure: Duration (in months) the customer has been with the service provider.
- MonthlyCharges: Monthly fee charged to the customer.
- ContractType: Type of contract (Month-to-Month, One-Year, Two-Year).
- InternetService: Type of internet service subscribed to (DSL, Fiber Optic, None).
- TechSupport: Whether the customer has tech support (Yes or No).
- TotalCharges: Total amount charged to the customer, calculated as MonthlyCharges * Tenure.
- Churn: Target variable indicating whether the customer has churned (Yes or No).

## Workflow

### 1. Data Loading
- The dataset is first loaded and explored using basic functions like info() and describe(), which provide an overview of the data's structure and summary statistics.

### 2. Data Exploration & Cleaning
- Missing values in the InternetService feature are handled by replacing them with "Unknown" to ensure completeness.
- Duplicate records are checked and confirmed as non-existent in the dataset.
### 3. Data Visualization
- Using Matplotlib, various visualizations are created to gain insights into the data:

  - Frequency of the Churn label.
  - Average charges by churn.
  - Average charges by churn and gender.
  - Average tenure by churn.
  - Tenure distribution.
  - Average age by churn.
  - Age distribution.
  - Average monthly charges by contract type.
  - Monthly charges distribution.
  - Tech support availability (No/Yes).

### 4. Outlier Detection & Handling
- Outliers in the Tenure feature are identified and visualized using box plots. As Tenure reflects how long a customer has been using the service, outliers are not removed or transformed, as they may indicate loyal customers.

### 5. Data Preprocessing
- Categorical to Numerical Conversion: The categorical features (e.g., Gender, ContractType, InternetService, TechSupport, Churn) are converted into numerical values using encoding techniques.

### 6. Data Splitting
- The dataset is split into training and test sets using an 80/20 ratio to evaluate model performance.

### 7. Scaling
- Standard scaling is applied to numerical features to standardize the range of values.

### 8. Class Imbalance Handling
- Class imbalance is addressed using RandomOverSampler to balance the classes before training the model.

### 9. Classification Model
- An XGBoost classifier is used to predict customer churn. Hyperparameter tuning is performed using GridSearchCV to find the best parameters for the model.

### 10. Evaluation
- The model is evaluated based on its accuracy, precision, recall, and F1 score, with a particular focus on handling imbalanced classes effectively.

## Conclusion
This project demonstrates the end-to-end process of predicting customer churn in the telecom industry, from data cleaning and exploration to building a machine learning model for classification. The use of advanced techniques like feature scaling, outlier handling, and class imbalance correction ensures a robust and reliable model for churn prediction.

## Technologies Used
+ Python
+ Pandas
+ Numpy
+ Scikit-learn
+ Matplotlib
+ XGBoost
+ Scikit-learn
+ GridSearchCV
+ RandomOverSampler

## License
This project is licensed under the MIT License.
