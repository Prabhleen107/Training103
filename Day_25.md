# Day 25 – Customer Churn Prediction: Model Building and Final Project

## Introduction

In the previous lesson, I explored customer churn data and learned how NLP techniques such as TF-IDF can extract useful information from customer feedback.

In this lesson, I completed the Customer Churn Prediction project by combining Machine Learning and NLP techniques.

The main objective was to prepare the dataset, train classification models, evaluate their performance and develop a function that predicts the churn probability of new customers.

This project demonstrated how different types of data can be combined to develop an intelligent prediction system.

## Topics Learned

### 1. Data Preprocessing and Feature Engineering

Before training a machine learning model, the dataset must be converted into a suitable numerical format.

In this project, I worked with three types of features:

* **Numerical Features:** Tenure, MonthlyCharges and SupportTickets.
* **Categorical Features:** Contract type.
* **Text Features:** CustomerFeedback.

Each type of data required a different preprocessing technique.

### 2. Categorical Data Encoding

Machine learning algorithms generally require numerical input.

Therefore, I used **One-Hot Encoding** to convert the Contract column into numerical columns.

I used Pandas `get_dummies()` function with `drop_first=True` to create dummy variables for different contract types.

This allowed the machine learning models to understand categorical information in numerical form.

### 3. Text Feature Extraction Using TF-IDF

I used the `TfidfVectorizer` from Scikit-learn to convert customer feedback into numerical features.

The vectorizer was configured with:

* `max_features=15` to select a maximum of 15 text features.
* `stop_words='english'` to remove common English words.
* `ngram_range=(1, 2)` to consider individual words and pairs of consecutive words.

The extracted text features were converted into a Pandas DataFrame with meaningful column names.

### 4. Feature Fusion

Feature Fusion means combining different types of features into one dataset.

In this project, I combined:

* Numerical customer information.
* Encoded contract information.
* TF-IDF text features.

These features were combined using Pandas `concat()` function to create the final feature matrix `X`.

The target variable `y` contained the Churn column.

This step helped combine customer usage information and written feedback into a single dataset for machine learning.

### 5. Train-Test Split

Before training the models, I divided the dataset into two parts:

* **80% Training Data:** Used to train the machine learning models.
* **20% Testing Data:** Used to evaluate model performance on unseen records.

I used `train_test_split()` with `stratify=y` to maintain a similar churn distribution in both datasets.

I also used `random_state=42` to make the data split reproducible.

### 6. Model Training

I trained two classification algorithms to predict whether a customer would leave the company.

**Logistic Regression**

Logistic Regression is a supervised machine learning algorithm used for classification problems.

It predicts the probability of an observation belonging to a particular class.

In this project, I used Logistic Regression as a baseline model for customer churn prediction.

**Random Forest Classifier**

Random Forest is an ensemble learning algorithm that combines multiple decision trees to make predictions.

Each tree makes its own prediction, and the final result is determined through voting.

I used a Random Forest Classifier with 100 decision trees.

Both models were trained using the prepared training dataset, and their accuracy was calculated using the testing dataset.

### 7. Model Evaluation

After training the models, I evaluated their performance using different evaluation techniques.

**Accuracy Score:** Measures the percentage of correct predictions made by the model.

**Confusion Matrix:** Shows the number of correct and incorrect predictions by comparing actual and predicted values.

It contains:

* True Positive
* True Negative
* False Positive
* False Negative

**Classification Report:** Provides important evaluation metrics such as:

* Precision
* Recall
* F1-Score
* Support

These metrics help us understand how well the model identifies retained and churned customers.

### 8. Feature Importance Analysis

Feature Importance helps identify which features contribute most to the predictions made by a machine learning model.

I used the `feature_importances_` attribute of the Random Forest model to calculate feature importance scores.

I also created a bar chart to display the top 10 important features.

This analysis helped me understand which customer details and text-based features were useful for predicting churn.

### 9. Live Customer Churn Prediction

After completing model training and evaluation, I created a reusable Python function called `predict_customer_churn()`.

This function accepts information about a new customer, including:

* Tenure
* Monthly Charges
* Support Tickets
* Contract Type
* Customer Feedback

The function performs the following operations:

1. Collects the customer's numerical and categorical information.
2. Converts customer feedback using the already fitted TF-IDF vectorizer.
3. Creates a DataFrame with the same feature columns used during training.
4. Passes the input to the trained Random Forest model.
5. Uses `predict_proba()` to calculate the churn probability.
6. Classifies the customer as high risk or low risk using a 0.5 threshold.
7. Displays the prediction and suggested retention actions.

### 10. Customer Retention Recommendations

The prediction function also provides suggested actions based on the predicted churn risk.

For a high-risk customer, the suggested actions include:

* Offering a discount on a one-year contract.
* Scheduling a priority customer support callback.

For a low-risk customer, the suggested action is to send a thank-you offer.

This demonstrates how machine learning predictions can support business decisions and customer retention strategies.

## Practical Work

During this lesson, I completed the following practical tasks:

* Converted categorical contract information using One-Hot Encoding.
* Extracted text features using TF-IDF.
* Combined numerical, categorical and text features into one feature matrix.
* Divided the dataset into training and testing sets.
* Trained a Logistic Regression model.
* Trained a Random Forest Classifier with 100 trees.
* Compared the accuracy of both models.
* Created a confusion matrix and classification report.
* Analysed the top 10 important features using Random Forest.
* Created the `predict_customer_churn()` function.
* Tested the function with two customer examples: one high-risk and one low-risk.
* Displayed churn probability scores and suggested retention actions.

## Final Project Outcome

Through this project, I developed an end-to-end Customer Churn Prediction system that combines Machine Learning and Natural Language Processing.

The project demonstrated how customer usage metrics, contract information and written feedback can be combined to predict customer churn.

It also showed how a trained machine learning model can be used to analyse new customer information and generate predictions that may help businesses improve customer retention.

## Conclusion – My 25-Day AI/ML Learning Journey

Completing these 25 days of AI/ML training has helped me build a strong foundation in Artificial Intelligence, Machine Learning and Data Science.

During this journey, I started with Python programming and gradually moved towards important libraries, data analysis techniques, machine learning algorithms and Generative AI concepts.

Some of the major areas I explored include:

* **Python Programming:** Variables, data types, operators, loops, functions and data structures.
* **Data Analysis:** NumPy, Pandas and Exploratory Data Analysis.
* **Data Visualization:** Matplotlib and Seaborn.
* **Data Preprocessing:** Handling missing values, encoding, feature scaling and preparing datasets.
* **Machine Learning:** Linear Regression, Polynomial Regression, Ridge, Lasso, Logistic Regression, Decision Trees and Random Forests.
* **Unsupervised Learning:** Clustering and K-Means.
* **Model Evaluation:** Accuracy, MAE, R² score, confusion matrix, precision, recall and F1-score.
* **Deep Learning:** Introduction to neural networks and their important concepts.
* **Generative AI:** Large Language Models, Prompt Engineering and Groq API.
* **Practical Projects:** Healthcare Risk Prediction and Customer Churn Prediction.

The most important part of this journey was understanding how theoretical concepts can be applied to practical projects.

I learned that developing an AI/ML project involves much more than training a model. It also requires understanding the problem, collecting and preparing data, selecting suitable algorithms, evaluating results and making the model useful through an application.

