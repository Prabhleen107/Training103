# Day 17 – Decision Trees and Random Forests

## Introduction

In this session, I learned about two important classification algorithms: **Decision Trees** and **Random Forests**. We continued working on the Titanic Passenger Survival Prediction project, where the goal was to predict whether a passenger survived or did not survive.

Previously, we used Logistic Regression for classification. In this session, we explored tree-based models, which can learn non-linear relationships and automatically identify interactions between different features.

We also learned how to control overfitting, compare different classifiers, and understand which features have the greatest influence on predictions.

## Topics Learned

### 1. Introduction to Decision Trees

A Decision Tree is a supervised machine learning algorithm that makes predictions by dividing data into smaller groups using conditions.

For example, it can ask questions such as:

* Is the passenger's age less than or equal to 6.5?
* Is the passenger female?
* What was the passenger's ticket class?

Each answer leads to another branch until the model reaches a final prediction.

### 2. Gini Impurity

Gini Impurity is used by a Decision Tree to measure how mixed the classes are in a particular node.

* **Gini = 0:** The node is completely pure, meaning all samples belong to one class.
* **Gini = 0.5:** The node has maximum impurity for a binary classification problem, with both classes equally represented.

The Decision Tree selects splits that reduce Gini Impurity and make the resulting groups more uniform.

### 3. Training and Visualizing Decision Trees

I trained an unrestricted Decision Tree and compared its training accuracy with its testing accuracy. The model could memorize the training data but did not perform equally well on unseen data, demonstrating the problem of overfitting.

I also trained a shallow Decision Tree with a maximum depth of 3 and visualized its splitting decisions using `plot_tree()`.

The visualization helped me understand:

* Split conditions at each node.
* Left and right branches.
* Number of samples in each node.
* Predicted classes and class distribution.

### 4. Regularization in Decision Trees

Regularization helps control the growth of a Decision Tree and reduces overfitting.

I learned about three important hyperparameters:

* **max_depth:** Controls the maximum depth of the tree.
* **min_samples_split:** Specifies the minimum number of samples required to split a node.
* **min_samples_leaf:** Specifies the minimum number of samples required in a leaf node.

I experimented with different values of `max_depth` and compared training and testing accuracy to understand the bias-variance trade-off.

### 5. Introduction to Ensemble Learning and Random Forests

Random Forest is an ensemble learning algorithm that combines multiple Decision Trees to make more reliable predictions.

It works using three main ideas:

* **Bootstrap Aggregation (Bagging):** Each tree is trained on a randomly selected sample of the training data.
* **Feature Subspace Sampling:** Each tree considers a random subset of features while making splits.
* **Majority Voting:** All trees make predictions, and the class receiving the majority of votes becomes the final prediction.

Random Forest generally provides more stable results than a single Decision Tree because it combines the predictions of multiple trees.

### 6. Training and Evaluating Random Forest

I trained a Random Forest Classifier using 100 decision trees and a maximum depth of 5.

I evaluated its performance using:

* Training and testing accuracy.
* 5-fold cross-validation.
* Precision, recall and F1-score.
* Confusion matrix.

The confusion matrix helped me understand the number of correct and incorrect survival predictions made by the model.

### 7. Feature Importance

Feature Importance helps identify which input features contribute most to a model's predictions.

I compared two approaches:

* **Random Forest Gini Importance:** Measures how much a feature helps reduce impurity across the trees.
* **Logistic Regression Coefficients:** Show the direction and strength of the relationship between a feature and the predicted outcome in the model.

An important difference is that Gini importance is non-directional, while Logistic Regression coefficients can be positive or negative.

### 8. Comparing Classification Models

I compared three classification algorithms on the Titanic dataset:

1. Logistic Regression
2. Tuned Decision Tree
3. Random Forest

I compared their testing accuracy and cross-validation accuracy using a summary table and bar chart.

This helped me understand how different classification algorithms perform on the same dataset.

## Practical Work

During this session, I performed the following practical tasks:

* Loaded and preprocessed the Titanic dataset using Pandas.
* Handled missing values in the `Age` and `Embarked` columns.
* Converted the `Sex` column into a numerical feature named `IsFemale`.
* Selected features such as `Pclass`, `Age`, `Fare`, `SibSp`, `Parch` and `IsFemale`.
* Divided the dataset into 80% training data and 20% testing data.
* Trained an unrestricted Decision Tree and checked overfitting.
* Visualized a shallow Decision Tree using `plot_tree()`.
* Tested different `max_depth` values to improve model performance.
* Trained a Random Forest Classifier using 100 trees.
* Evaluated the Random Forest using accuracy, classification report and confusion matrix.
* Compared Random Forest feature importance with Logistic Regression coefficients.
* Compared Logistic Regression, Decision Tree and Random Forest performance.
* Experimented with different numbers of trees and `min_samples_leaf` values.
* Calculated permutation feature importance to understand the contribution of individual features.
* Visualized decision boundaries using Age and Fare to compare Decision Tree and Random Forest predictions.

## Learning Outcome

By the end of this session, I understood how Decision Trees make predictions by splitting data into smaller groups and how Gini Impurity helps select the best splits. I also learned that an unrestricted tree can overfit the training data and that hyperparameters such as `max_depth` and `min_samples_leaf` help control this problem.

I gained practical knowledge of Random Forests and how combining multiple trees can produce more stable predictions. I also learned to compare classification algorithms, evaluate their performance, and identify important features using different feature importance techniques.

This session improved my understanding of tree-based classification models and their applications in real-world machine learning problems.
