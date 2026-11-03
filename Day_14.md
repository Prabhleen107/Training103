# Day 14 – Ridge and Lasso Regression: Understanding Regularization 

On Day 14, I learned about **Regularization**, an important technique in Machine Learning used to control overfitting and improve model performance.

In the previous session, I learned about Polynomial Regression, which allows a model to understand curved relationships between input features and output values. However, when we use higher-degree polynomial features, the model may become too complex and start fitting even the small variations and noise in the training data. This problem is known as **Overfitting**.

To control this problem, I learned about two regularization techniques: Ridge Regression and Lasso Regression. These techniques control the model's coefficients and help prevent the model from becoming unnecessarily complex.

## Topics Learned

* **Introduction to Overfitting:** Learned that overfitting occurs when a Machine Learning model learns the training data too closely, including noise and unnecessary details. Such a model may perform well on training data but poorly on new, unseen data.

* **Regularization:** Understood that regularization is a technique used to control model complexity by adding a penalty to large model coefficients. It helps the model focus on general patterns instead of memorizing the training data.

* **Ridge Regression (L2 Regularization):** Learned that Ridge Regression adds an L2 penalty to the model. It reduces the size of coefficients by bringing them closer to zero, but generally does not make them exactly zero. It helps control large coefficient values and makes the model more stable.

* **Lasso Regression (L1 Regularization):** Learned that Lasso Regression uses an L1 penalty. It can reduce some coefficients to exactly zero, which means the corresponding features are removed from the model. This also makes Lasso useful for feature selection.

* **Difference Between Ridge and Lasso:**

  * Ridge reduces the size of coefficients but generally keeps all features.
  * Lasso can make some coefficients exactly zero and remove less useful features.

* **Alpha Parameter:** Learned about the `alpha` parameter, which controls the strength of regularization. A higher alpha applies a stronger penalty to the model coefficients.

* **Polynomial Regression with Regularization:** Understood how Ridge and Lasso can be combined with Polynomial Regression to control the complexity of higher-degree polynomial models.

* **Model Evaluation:** Used Mean Absolute Error (MAE) and R² Score to evaluate and compare the performance of different regression models.

* **Model Visualization:** Learned how to visualize multiple prediction curves together to understand how regularization affects the model's behaviour.

## Practical Work

* Imported NumPy, Pandas, Matplotlib and required Scikit-learn libraries.
* Loaded the preprocessed house-price dataset, `kc_house_preprocessed.csv`.
* Selected a random sample of 80 houses to make the visualization easier to understand.
* Selected `Scaled_size` as the input feature (X) and `price` as the target variable (y).
* Divided the dataset into 80% training data and 20% testing data using `train_test_split()`.
* Created a Degree 6 Polynomial Regression model without regularization to observe the behaviour of an unrestricted model.
* Trained a Ridge Regression model using `Ridge(alpha=0.1)` with Polynomial Features of degree 6.
* Trained a Lasso Regression model using `Lasso(alpha=100.0, max_iter=10000)` with Polynomial Features of degree 6.
* Generated predictions using all three models: Wild Model, Ridge Model and Lasso Model.
* Calculated MAE and R² Score for each model to evaluate their performance.
* Used Matplotlib to plot actual house data points and the prediction curves of all three models on the same graph.
* Compared the curves to understand how Ridge and Lasso regularization control model complexity.

## Learning Outcome

By the end of this session, I understood the problem of overfitting and why controlling model complexity is important in Machine Learning. I learned how regularization helps prevent a model from becoming too dependent on training data.

I also understood the working difference between Ridge Regression and Lasso Regression. Ridge reduces coefficient values, whereas Lasso can reduce some coefficients to exactly zero, making it useful for selecting important features.

Through practical implementation, I gained experience in training unregularized, Ridge and Lasso models using Polynomial Features. Comparing their MAE and R² scores helped me understand how different regularization techniques affect prediction performance.

This session taught me that a good Machine Learning model should not simply memorize training data; it should learn meaningful patterns and perform well on new, unseen data.
