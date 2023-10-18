# credit-card-fraud-detection
A credit card is one of the most used financial products to make online purchases and payments. The Credit card can be a convenient way to manage your finances, it can also be risky. Credit card fraud is the unauthorized use of someone else's credit card or credit card information to make purchases or withdraw cash.

It is important that credit card companies are able to recognize fraudulent credit card transactions so that customers are not charged for items that they did not purchase. 
Detecting fraudulent transactions is challenging due to the high volume and variety of transactions, the imbalance between fraud and non-fraud cases, and the adaptive nature of fraudsters.

[Download the dataset](https://kh3-ls-storage.s3.us-east-1.amazonaws.com/DS%20Project%20Guide%20Data%20Set/creditcard.csv) that will be used for this project

The dataset contains transactions made by credit cards in September 2013 by European cardholders. This dataset presents transactions that occurred in two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly unbalanced, the positive class (frauds) account for 0.172% of all transactions.

The dataset has 31 features, 28 of which are numerical and have been transformed using principal component analysis (PCA) for confidentiality purpose. The features that were not transformed are Time (the seconds elapsed between each transaction and the first transaction in the dataset) and Amount (the transaction amount). The target variable is Class, which is 1 for fraudulent transactions and 0 for non-fraudulent transactions.

The aim of this project is to develop and evaluate classification machine learning models that can identify and predict fraudulent credit card transactions using the dataset provided.

Exploratory Data Analysis was carried out to check for missing values, correlation between features and target variable. Feature scaling was performed on the Amount columns with standard scaler as it was not transformed with PCA with other features in the dataset.

As this is a classification problem, 5 Machine Learning Algoriths were applied : Logistice Regression, Decision Tree, Random Forest, Support Vector Machine and XGBoost. Resampling techniques such as random undersampling and SMOTE (synthetic minority oversampling technique) to balance the classes were applied. Each model was evaluated using various metrics such as accuracy, precision, recall, f1-score, and confusion matrix.

Random Forest Classifier achieved the best performance among all models, with an accuracy of 0.9999, a precision of 0.9998, a recall of 1.0, an f1-score of 0.9999 after using oversampling technique to balance the imbalanced dataset.

This project demonstrates how machine learning can be used to detect and prevent credit card fraud, which is a critical and costly issue for both consumers and businesses. However, this project also has some limitations, such as:
  o	The dataset used is from 2013, which may not reflect the current trends and patterns of credit card fraud

  o	The dataset used from Europe, which may not generalize to other regions or countries

  o	The dataset used has been anonymized and transformed using PCA (for reasons of confidentiality), which may reduce the interpretability and explainability of the features and models

  o	The models used in this project may not be robust to new or unseen data, as fraudsters may constantly change their strategies and behaviors

Possible future work for this project are:

o	Use more recent and diverse datasets to train and test the models

o	Use more interactive and user-friendly tools such as dashboards or web applications to deploy and monitor the models
