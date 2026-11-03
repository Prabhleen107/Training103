# Day 24 – Customer Churn Prediction: EDA and NLP Analysis

## Introduction

In this lesson, I started an end-to-end Machine Learning and NLP project called **Customer Churn Prediction**.

Customer churn refers to a situation in which customers stop using a company's products or services. Businesses use customer churn prediction to identify customers who may leave so that they can take steps to improve customer retention.

In this project, I explored how Machine Learning and Natural Language Processing (NLP) can work together to predict customer churn. I used customer details such as tenure, monthly charges and support tickets, along with written customer feedback.

The main objective was to understand customer behaviour and identify patterns that may indicate whether a customer is likely to leave a company.

## Topics Learned

### 1. Introduction to Customer Churn

Customer churn means the loss of customers when they discontinue a company's services.

For example, if a customer stops using an internet service because of poor network quality, expensive plans or unsatisfactory customer support, it is considered customer churn.

Churn prediction helps businesses:

* Identify customers who may leave.
* Understand customer dissatisfaction.
* Improve customer service.
* Develop customer retention strategies.
* Reduce the loss of existing customers.

### 2. Dataset Loading and Understanding

For this project, I worked with a customer churn dataset containing different types of information.

The dataset included:

* **Tenure:** Number of months a customer has used the company's services.
* **MonthlyCharges:** Monthly amount paid by the customer.
* **SupportTickets:** Number of complaints or support requests.
* **Contract:** Type of customer contract, such as monthly, one-year or two-year.
* **CustomerFeedback:** Written reviews or feedback provided by customers.
* **Churn:** Target variable representing whether the customer left the company or continued using its services.

The target variable contained two values:

* `0` – Customer retained.
* `1` – Customer churned.

I used Pandas to load the dataset and inspect its structure, number of rows, columns and sample records.

### 3. Exploratory Data Analysis (EDA)

Exploratory Data Analysis helps us understand a dataset before applying machine learning algorithms.

In this project, I analysed customer information to understand the factors related to customer churn.

The main analysis included:

**Churn Distribution:**
Used count plots and pie charts to understand the number and percentage of retained and churned customers.

**Tenure Analysis:**
Used box plots to compare how long retained and churned customers had been associated with the company.

**Monthly Charges Analysis:**
Compared monthly charges between retained and churned customers to understand possible relationships between pricing and customer behaviour.

**Support Tickets Analysis:**
Used count plots to examine the number of support tickets raised by customers and compare them with churn status.

**Contract Analysis:**
Compared different contract types to understand how customer contracts relate to churn.

These visualizations helped in understanding customer behaviour and identifying possible patterns in the dataset.

### 4. Introduction to Natural Language Processing (NLP)

Natural Language Processing is a branch of Artificial Intelligence that allows computers to understand, process and analyse human language.

In this project, NLP was used to analyse written customer feedback.

Numerical information can help us understand customer behaviour, but written feedback can provide additional information about customer experiences and complaints.

For example:

* Negative feedback: "The internet is slow and the service is expensive."
* Positive feedback: "The connection is smooth and customer support is helpful."

Analysing such feedback helps identify words and expressions that may be useful for predicting customer churn.

### 5. Understanding TF-IDF

TF-IDF stands for **Term Frequency-Inverse Document Frequency**.

It is a text-processing technique used in NLP to convert written text into numerical values that machine learning models can understand.

It measures the importance of a word in a document compared with how frequently that word appears across the complete collection of documents.

For example, words such as:

* Expensive
* Disconnect
* Slow
* Helpful
* Service

may provide useful information about customer experiences.

TF-IDF helps convert these words into numerical features so they can be used during machine learning model training.

### 6. Analysing Customer Feedback

I explored sample feedback from both retained and churned customers.

The purpose was to understand how customers express their satisfaction or dissatisfaction through written reviews.

This helped me understand how text-based information can be combined with numerical customer information to improve the analysis of customer behaviour.

## Practical Work

During this lesson, I performed the following practical tasks:

* Imported Pandas, NumPy, Matplotlib and Seaborn.
* Imported the required Scikit-learn libraries for NLP and Machine Learning.
* Loaded the customer churn dataset using Pandas.
* Checked the dataset shape and displayed sample records.
* Analysed the distribution of retained and churned customers.
* Created count plots and pie charts to visualize churn distribution.
* Used box plots to compare tenure and monthly charges.
* Analysed support tickets and different contract types.
* Displayed sample feedback from retained and churned customers.
* Explored how TF-IDF can extract useful information from customer reviews.

## Learning Outcome

In this lesson, I learned about customer churn and its importance in business decision-making. I understood how to explore customer datasets using EDA techniques and visualizations.

I also learned the basics of Natural Language Processing and how TF-IDF converts written customer feedback into numerical features.

This lesson helped me understand how both numerical data and human language can provide useful information for solving real-world business problems.
