# Day 16 – Multiclass Classification Using Logistic Regression 

On Day 16, I continued learning about Classification in Machine Learning, focusing on **Multiclass Classification**.

In the previous session, I trained a Logistic Regression model to predict whether a Titanic passenger survived or not. This was a Binary Classification problem because it had only two possible outcomes.

In this session, I learned how classification models can also predict between three or more categories. For practical implementation, I continued working with the Titanic dataset and trained a model to predict the passenger class: First Class, Second Class or Third Class.

## Topics Learned

* **Introduction to Multiclass Classification:** Learned that multiclass classification is used when the target variable contains three or more possible categories. For example, predicting whether a passenger belongs to First, Second or Third Class.

* **Difference Between Binary and Multiclass Classification:** Understood that binary classification has exactly two output categories, whereas multiclass classification has three or more output categories.

* **Logistic Regression for Multiple Classes:** Learned how Logistic Regression can be used for multiclass problems through different approaches.

* **One-vs-Rest (OvR):** Understood that this approach trains a separate binary classifier for each class against all the remaining classes. The class with the highest predicted probability is selected.

* **Multinomial Classification (Softmax):** Learned that the Softmax function calculates probabilities for all classes together. The model selects the class with the highest probability.

* **Feature Selection:** Selected Survived, Age, Fare, SibSp, Parch and IsFemale as input features to predict the passenger's class.

* **Model Training and Prediction:** Learned how to train a multiclass Logistic Regression model using training data and predict categories for unseen testing data.

* **Confusion Matrix for Multiclass:** Understood that a multiclass classification problem uses an N × N confusion matrix, where N represents the number of classes. For three classes, the confusion matrix has a 3 × 3 structure.

* **Classification Report:** Used Accuracy, Precision, Recall and F1-Score to understand the performance of the multiclass model.

## Practical Work

* Continued working with the Titanic dataset after completing the preprocessing steps.
* Selected Survived, Age, Fare, SibSp, Parch and IsFemale as input features (X).
* Selected Pclass as the target variable (y), containing three possible classes.
* Divided the dataset into 80% training data and 20% testing data using `train_test_split()`.
* Created a multiclass Logistic Regression model using `LogisticRegression(max_iter=1000)`.
* Trained the model using the training dataset with `fit()`.
* Predicted passenger classes using `predict()`.
* Calculated model accuracy using `accuracy_score()`.
* Generated a 3 × 3 Confusion Matrix to compare actual and predicted passenger classes.
* Visualized the Confusion Matrix using a Seaborn heatmap.
* Generated a Classification Report to evaluate the model using Precision, Recall and F1-Score.
* Compared Binary and Multiclass Classification based on the number of classes, output probabilities, functions used and confusion matrix structure.

## Exercises and Additional Practice

* **Adding Pclass to Binary Classification:** Added the Pclass feature to the binary survival prediction model to observe whether including passenger class improves prediction accuracy.

* **Changing the Decision Threshold:** Experimented with increasing the survival prediction threshold from 0.5 to 0.7. Used `predict_proba()` to obtain survival probabilities and created new predictions based on the changed threshold.

* **Confusion Matrix Comparison:** Generated a new confusion matrix after changing the threshold to understand how the number of predicted survivors and classification errors changed.

## Learning Outcome

By the end of this session, I understood how Logistic Regression can solve multiclass classification problems in addition to binary classification. I learned the working concepts of One-vs-Rest and Multinomial Classification and understood how the Softmax function helps predict probabilities across multiple categories.

I also gained practical experience in training and evaluating a multiclass model using the Titanic dataset. Working with a 3 × 3 Confusion Matrix helped me understand how actual and predicted categories are compared in multiclass problems.

This session strengthened my understanding of classification algorithms and showed me how the same Machine Learning technique can be applied to solve problems involving two or multiple categories.
