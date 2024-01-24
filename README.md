# Machine Learning using BigQuery on GCP

This is a GCP Qwiklabs project. The data used in this project is the "data-to-insights" ecommerce web analytics public data available on BigQuery. It essentially consists of Google Analytics logs for an ecommerce website with fields lik visitorId, date, time, total visits, screen views, total transaction revenue, referral path etc. The data has almost a million records.

The project aims at creating a Machine Learning model in BigQuery to predict whether or not a new user is likely to purchase in the future. This can help the marketing team target high-value users with special promotions and ad campaigns. For this project, the two features being used are - bounces (whether the visitor left the website immediately)
and timeOnSite (how long the visitor was on the website).

### Creating a BigQuery dataset to store models

<img width="905" alt="1" src="https://github.com/Abhishek-Dxt/BigQuery_ML/assets/71979171/0cb8980c-c0d4-41d5-9e89-02bec60c6378">

### Creating a Logistic Regression model on BigQuery using GoogleSQL

On the query editor in BigQuery, ML models can be created using GoogleSQL (Google Standard SQL).

<img width="869" alt="2" src="https://github.com/Abhishek-Dxt/BigQuery_ML/assets/71979171/4cff0ba4-3dad-4c63-894a-8f4b2221a635">

<img width="576" alt="3" src="https://github.com/Abhishek-Dxt/BigQuery_ML/assets/71979171/bb8b5622-3440-498a-a3da-f70463e2679e">

<img width="397" alt="4" src="https://github.com/Abhishek-Dxt/BigQuery_ML/assets/71979171/0515125f-2eab-486a-8204-98e155960a93">

### Evaluating the Classification model against unseen data

For classification problems we minimize the False Positive Rate (predict that the user will return and purchase and they don't) and maximize the True Positive Rate (predict that the user will return and purchase and they do). Model can be evaluated using ML.EVALUATE.

<img width="286" alt="5" src="https://github.com/Abhishek-Dxt/BigQuery_ML/assets/71979171/beb9533f-e9a9-4035-b260-0189cbc4f7e3">

### Improve model performance with feature engineering 

The model is then improved by adding some crucial features into the list of independednt variables. With this new model you now get a roc_auc of 0.91 which is significantly better than the first model.

<img width="248" alt="6" src="https://github.com/Abhishek-Dxt/BigQuery_ML/assets/71979171/976b908c-e398-4b23-b37d-7ecf0242deb5">

### Making predictions whether a user will return or not using the trained model utilizing ML.Predict

The model outputs 1 for users who are predicted to make a vist and 0 for those who won't.

<img width="410" alt="7" src="https://github.com/Abhishek-Dxt/BigQuery_ML/assets/71979171/9215833a-52fe-444e-acbc-7318b970daee">

The model can be further improved using advanced classifiers like the XGBoost Classifier.



