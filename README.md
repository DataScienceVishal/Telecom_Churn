# Telecom Churn Case Study

## Problem Statement
With 21 predictor variables, the task is to predict whether a particular customer will switch to another telecom provider or not, known as churning or not churning, respectively.

## About the Data

| Variable Name   | Meaning                                                      |
|-----------------|--------------------------------------------------------------|
| CustomerID      | The unique ID of each customer                               |
| Gender          | The gender of a person                                       |
| SeniorCitizen   | Whether a customer can be classified as a senior citizen      |
| Partner         | If a customer is married/in a live-in relationship           |
| Dependents      | If a customer has dependents (children/retired parents)       |
| Tenure          | The time for which a customer has been using the service     |
| PhoneService    | Whether a customer has a landline phone service along with internet service |
| MultipleLines   | Whether a customer has multiple lines of internet connectivity |
| InternetService | The type of internet services chosen by the customer         |
| OnlineSecurity  | Specifies if a customer has online security                  |
| OnlineBackup    | Specifies if a customer has online backup                    |
| DeviceProtection| Specifies if a customer has opted for device protection      |
| TechSupport     | Whether a customer has opted for tech support or not         |
| StreamingTV     | Whether a customer has an option of TV streaming             |
| StreamingMovies | Whether a customer has an option of Movie streaming          |
| Contract        | The type of contract a customer has chosen                   |
| PaperlessBilling| Whether a customer has opted for paperless billing           |
| PaymentMethod   | Specifies the method by which bills are paid                 |
| MonthlyCharges  | Specifies the money paid by a customer each month            |
| TotalCharges    | The total money paid by the customer to the company          |
| Churn           | Target variable indicating if a customer has churned or not  |


## Data Analysis and Modeling
Extensive exploratory data analysis (EDA), data scaling, and modeling were performed.

### Models Used:
- Logistic Regression
- Decision Tree
- Random Forest

### Results:
- Logistic Regression: Achieved 80% accuracy.
- Decision Tree and Random Forest helped identify tenure as the most significant predictor influencing churn.

## Libraries Used
- warnings
- pandas
- sklearn
- matplotlib
- seaborn
- statsmodel

