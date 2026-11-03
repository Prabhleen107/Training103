# Day 20 – Model Building and Training Using Random Forest

## Introduction

In this session, I learned how to build and train a Machine Learning classification model using a healthcare dataset. In the previous session, I performed Exploratory Data Analysis (EDA) to understand the patient data, examine health measurements and identify relationships between different features.

Now, the main objective was to develop a model that can predict a patient's health risk category based on their vital signs.

For this practical, I used a **Random Forest Classifier** to classify patients into two categories: Healthy (0) and At Risk (1). I also learned how to evaluate the model, understand feature importance and save the trained model for future use in a Streamlit web application.

## Topics Learned

### 1. Introduction to Model Building

Model building is the process of training a Machine Learning algorithm using available data so that it can learn patterns and make predictions on new data.

In this project, the model uses patient health measurements to predict their health risk category.

### 2. Creating the Target Variable (risk_level)

The dataset contained patient health measurements but did not have a final health risk category. Therefore, I created a target variable called `risk_level`.

Five health risk indicators were considered:

* **High Glucose:** Fasting glucose greater than 130 mg/dL.
* **High Blood Pressure:** Blood pressure greater than 135 mmHg.
* **High Cholesterol:** Total cholesterol greater than 200 mg/dL.
* **Obesity:** BMI greater than 28.
* **Older Age:** Age greater than 60 years.

Each condition was converted into a binary value (0 or 1). The risk indicators were added together to calculate the total risk score.

Based on the total score:

* **0 – Healthy:** Fewer than two risk factors.
* **1 – At Risk:** Two or more risk factors.

This created the target variable required for binary classification.

### 3. Understanding Overfitting and Deterministic Rules

I learned why a model may initially achieve very high accuracy when its target labels are created directly using fixed rules.

When the same rules are used to generate labels and the model is trained on the same features, the model can easily learn those patterns. This can result in very high accuracy that may not represent performance on real-world health data.

The lesson also introduced the idea of adding realistic noise to make the classification problem more challenging.

### 4. Separating Features and Target

Before training the model, I separated the dataset into two parts:

* **Features (X):** Input columns containing patient health information.
* **Target (y):** The `risk_level` column that the model needs to predict.

This separation helps the algorithm learn the relationship between patient measurements and their assigned health risk categories.

### 5. Training and Testing Split

I divided the dataset into two parts using `train_test_split()`:

* **80% Training Data:** Used to train the model.
* **20% Testing Data:** Used to evaluate the model on unseen records.

This helps check how well the trained model performs beyond the data it learned from.

### 6. Training a Random Forest Classifier

Random Forest is an ensemble learning algorithm that combines multiple Decision Trees to make predictions.

Instead of depending on a single tree, it collects predictions from several trees and uses majority voting to determine the final classification.

I trained the model using:

* `n_estimators=100`: Creates 100 Decision Trees.
* `max_depth=6`: Limits the depth of each tree to control model complexity.
* `random_state=42`: Helps produce reproducible results.
* `n_jobs=-1`: Uses available processing cores to speed up training.

### 7. Model Evaluation

After training, I used the testing data to generate predictions and evaluate the model.

I learned about the following evaluation measures:

* **Accuracy:** Measures the percentage of correct predictions.
* **Precision:** Measures how many predicted positive cases were actually positive.
* **Recall:** Measures how many actual positive cases were correctly identified.
* **F1-Score:** Combines precision and recall into a single measure.

I used `accuracy_score()` and `classification_report()` from Scikit-Learn to evaluate the model's performance.

### 8. Feature Importance

Feature Importance helps identify which input features contribute most to the predictions made by a Random Forest model.

I extracted feature importance scores using `model.feature_importances_` and arranged them in a DataFrame.

I also created a bar chart using Seaborn to compare the importance of different patient health measurements.

This helps understand which health features the trained model relies on most when predicting patient risk categories.

### 9. Saving the Trained Model Using Pickle

After training and evaluating the model, I learned how to save it using Python's `pickle` library.

I created a folder named `model` and saved the trained model along with its feature names in a file called `healthcare_model.pkl`.

This allows the model to be loaded later without training it again.

The saved model is intended to be used by the Streamlit web application, where users can enter patient information and receive predictions.

## Practical Work

During this session, I performed the following practical tasks:

* Imported Pandas, NumPy, Matplotlib, Seaborn and Scikit-Learn libraries.
* Loaded the `test_healthcare_data.csv` dataset.
* Created five binary health risk indicators using clinical thresholds.
* Calculated the total risk score for each patient.
* Created the `risk_level` target variable with Healthy (0) and At Risk (1) categories.
* Separated the input features (X) and target variable (y).
* Divided the dataset into 80% training data and 20% testing data.
* Initialized and trained a Random Forest Classifier with 100 Decision Trees.
* Controlled model complexity using the `max_depth` parameter.
* Generated predictions using the testing dataset.
* Evaluated model performance using accuracy and a classification report.
* Extracted feature importance scores from the trained model.
* Visualized feature importance using a Seaborn bar chart.
* Created a `model` folder to store the trained model.
* Saved the model and feature names into `healthcare_model.pkl` using Pickle.

## Learning Outcome

By the end of this session, I understood the complete process of building and training a Machine Learning classification model using healthcare data. I learned how to create target labels using predefined risk conditions, separate features and targets, split the dataset and train a Random Forest Classifier.

I also gained practical knowledge of model evaluation using accuracy, precision, recall and F1-score. Additionally, I learned how to identify important features and save a trained model using Pickle.

This session helped me understand how a trained Machine Learning model can be integrated into a real application, preparing the healthcare project for the next stage of development using Streamlit.
