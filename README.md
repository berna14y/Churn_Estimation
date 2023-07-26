# Churn_Estimation
Churn Estimation Model Using SVC,LR and RFC


The dataset used in this work  includes information about customers, their interactions with a company, and whether they have exited (churned) from the company.
It contains columns like "RowNumber," "CustomerId," "Surname," "Geography," "Gender," "Age," "CreditScore," "Balance," "NumOfProducts," "HasCrCard," "IsActiveMember," "EstimatedSalary," and "Exited."
The "Exited" column is the target variable, indicating whether a customer has churned (1) or not (0).
Other columns are likely features or attributes of customers that may be used to predict churn.

Churn estimation, also known as churn prediction or customer churn analysis, is a data analysis process used by businesses to predict and estimate the likelihood of customers leaving or discontinuing their relationship with the company, product, or service. The term "churn" refers to the phenomenon of customer attrition or the rate at which customers stop doing business with a company.

Churn estimation is a critical aspect of customer relationship management (CRM) and customer retention strategies. By accurately predicting which customers are more likely to churn, businesses can take proactive measures to retain those customers and reduce the overall churn rate. This, in turn, can have a positive impact on customer loyalty, profitability, and long-term success.


Steps of my work :

Data Preprocessing:
Loaded the dataset from the "Churn_Modelling.csv.xls" file using pandas.
Removed irrelevant columns: "RowNumber", "CustomerId", and "Surname."
Identified numerical columns in the DataFrame for further analysis.
Checked some descriptive statistical information about the numerical columns.
Explored the percentage of customers who exited (churned) based on gender and geography.
Analyzed the age distribution and percentage of people in different age groups who exited.

Data Cleaning and Transformation:
Converted the "Age" column into categorical bins (age groups) using pd.cut().
Performed one-hot encoding on categorical variables (Gender and Geography) to convert them into numerical representations.
Removed redundant columns "Geography_France" and "Gender_Female" after one-hot encoding.
Selected features and target variable for model training.
Saved the cleaned data to a new CSV file named "Clean_data.csv."

Exploratory Data Analysis (EDA):
Conducted correlation analysis using a heatmap to visualize the relationships between features.

Model Training and Evaluation:
Split the dataset into training and testing sets (70% training, 30% testing).
Applied StandardScaler to scale the numerical features for better model performance.

Performed hyperparameter tuning for two models:
Support Vector Classifier (SVC) using RandomizedSearchCV.
Logistic Regression using GridSearchCV.
Random Forest Classifier using GridSearchCV.
Evaluated the models using various performance metrics such as accuracy, precision, recall, and F1-score.
Compared the performance of the three models based on their evaluation metrics.

Conclusion:
The Random Forest Classifier demonstrated the best overall performance on the churn prediction task with the highest accuracy, precision, recall, and F1-score.
The choice of the final model should consider the specific requirements and business goals, such as the importance of precision or recall in churn prediction.
