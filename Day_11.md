# Day 11 – Data Preprocessing Using Python

On Day 11 of my AI and Machine Learning training, I learned about **Data Preprocessing**, which is an important step before building a machine learning model. After performing Exploratory Data Analysis on the House Prices dataset, the next step was to understand how raw data can be cleaned, transformed, and prepared for machine learning.

Real-world datasets may contain missing values, duplicate records, incorrect entries, outliers, and different types of data. These issues can affect the performance of machine learning models. Data preprocessing helps improve data quality and makes the dataset suitable for further analysis and model training.

## Topics Learned

* **Introduction to Data Preprocessing:** Learned why raw data needs to be cleaned and transformed before applying machine learning algorithms.

* **Handling Missing Values:** Understood how to identify missing values using `isnull()` and `isnull().sum()`. Learned about filling missing values using techniques such as mean, median, and mode.

* **Removing Duplicate Records:** Learned how to identify and remove repeated records using `duplicated()` and `drop_duplicates()`.

* **Handling Outliers:** Understood how extreme values can affect data analysis and model performance. Learned about identifying outliers using statistical methods and visualizations such as box plots.

* **Categorical Data Encoding:** Learned why categorical values need to be converted into numerical form before being used by many machine learning algorithms. Explored techniques such as Label Encoding and One-Hot Encoding.

* **Feature Scaling:** Understood why numerical features with different ranges need to be brought to a similar scale. Learned about Standardization and Normalization.

* **Standardization:** Learned how to transform numerical features using their mean and standard deviation so that they have a common scale.

* **Normalization:** Understood how to scale numerical values into a fixed range, commonly between 0 and 1.

* **Train-Test Split:** Learned how to divide a dataset into training and testing sets so that a machine learning model can be trained and evaluated on separate data.

## Practical Work

* Loaded the dataset using Pandas for preprocessing.
* Checked missing values in different columns.
* Explored techniques for filling missing values using statistical methods.
* Identified and handled duplicate records.
* Studied outliers using statistical summaries and box plots.
* Explored converting categorical data into numerical values.
* Practised feature scaling techniques such as Standardization and Normalization.
* Understood how to divide data into training and testing sets using `train_test_split()`.

## Learning Outcome

By the end of Day 11, I understood the importance of data preprocessing in the machine learning workflow. I learned that a dataset must be properly cleaned and transformed before it can be used to train a model.

I also gained an understanding of missing-value handling, duplicate removal, outlier treatment, categorical encoding, and feature scaling. These techniques help improve data quality and prepare the dataset for machine learning algorithms.

This session helped me understand the transition from Exploratory Data Analysis to data preparation, which is an important stage in developing an effective machine learning model.
