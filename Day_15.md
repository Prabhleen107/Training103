# Day 15 – Introduction to Classification and Binary Logistic Regression 

On Day 15, I learned about **Classification**, an important type of supervised Machine Learning used to predict categories or labels instead of continuous numerical values.

In previous sessions, I worked with regression algorithms to predict house prices. However, many real-world problems require us to predict categories, such as whether an email is spam or not, or whether a passenger survived or did not survive.

For this practical, I used the famous **Titanic dataset (`train.csv`)** to understand classification and train my first Logistic Regression model for predicting passenger survival.

## Topics Learned

* **Introduction to Classification:** Learned that classification is a supervised Machine Learning technique used to predict categories or labels based on input features.

* **Binary Classification:** Understood that binary classification predicts between exactly two possible outcomes. For example, predicting whether a Titanic passenger survived (1) or did not survive (0).

* **Introduction to Logistic Regression:** Learned that Logistic Regression is a classification algorithm that calculates a weighted combination of input features and passes the result through the Sigmoid function to produce a probability between 0 and 1.

* **Sigmoid Function:** Understood that the Sigmoid function converts numerical values into probabilities between 0 and 1. In binary classification, a probability of 0.5 or higher is generally classified as 1, while a value below 0.5 is classified as 0.

* **Data Exploration:** Learned how to load and inspect the Titanic dataset using Pandas. Used functions such as `shape` and `head()` to understand the dataset.

* **Data Preprocessing:** Handled missing values in the Age and Embarked columns. Filled missing Age values using the median and missing Embarked values using the mode.

* **Feature Encoding:** Converted the Sex column into numerical values using mapping, where female was represented by 1 and male by 0.

* **Feature Selection:** Selected important features such as Age, Fare, SibSp, Parch and IsFemale to train the binary classification model.

* **Model Evaluation:** Learned about important classification evaluation metrics:

  * **Accuracy:** Measures the percentage of correctly predicted results.
  * **Confusion Matrix:** Shows correct and incorrect predictions by comparing actual and predicted labels.
  * **Precision:** Measures how many positive predictions were actually correct.
  * **Recall:** Measures how many actual positive cases were correctly identified.
  * **F1-Score:** Represents the balance between Precision and Recall.

* **Decision Threshold:** Understood how the probability threshold affects classification predictions. The default threshold is 0.5, but it can be changed depending on the problem.

## Practical Work

* Imported NumPy, Pandas, Matplotlib, Seaborn and required Scikit-learn libraries.
* Loaded the Titanic dataset (`train.csv`) and explored its structure.
* Handled missing values in the Age and Embarked columns using median and mode.
* Converted the Sex column into numerical values using mapping.
* Selected Age, Fare, SibSp, Parch and IsFemale as input features (X).
* Selected Survived as the target variable (y).
* Divided the dataset into 80% training data and 20% testing data using `train_test_split()`.
* Created and trained a Logistic Regression model using `LogisticRegression(max_iter=1000)`.
* Predicted passenger survival using the trained model.
* Calculated model accuracy using `accuracy_score()`.
* Generated a Confusion Matrix to compare actual and predicted results.
* Visualized the Sigmoid function using Matplotlib.
* Generated a Classification Report to understand Precision, Recall and F1-Score.
* Experimented with changing the survival prediction threshold from 0.5 to 0.7 using `predict_proba()`.

## Learning Outcome

By the end of this session, I understood the basic concept of Classification and how it differs from Regression. I learned how Logistic Regression uses the Sigmoid function to generate probabilities and classify data into two categories.

Working with the Titanic dataset helped me gain practical experience in data preprocessing, feature selection, model training and prediction. I also understood how Accuracy, Precision, Recall, F1-Score and Confusion Matrix help evaluate a classification model.

This session introduced me to classification problems and helped me understand how Machine Learning can be used to make predictions based on different categories.
