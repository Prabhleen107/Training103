# Day 13 – Polynomial Regression: Understanding Curved Relationships 

On Day 13, I learned about **Polynomial Regression**, another supervised Machine Learning algorithm used for predicting continuous numerical values.

In the previous session, I trained a Linear Regression model that used a straight line to predict house prices. However, not every relationship between input features and output values is perfectly straight. Sometimes, data follows a curved pattern. In such situations, Polynomial Regression can help the model capture more complex relationships.

Polynomial Regression works by adding polynomial features, such as squared values, to the original input features. This allows the model to fit a curve instead of only a straight line.

For this practical, I continued working with the preprocessed house-price dataset, `kc_house_preprocessed.csv`, and trained a Polynomial Regression model of degree 2.

## Topics Learned

* **Introduction to Polynomial Regression:** Learned that Polynomial Regression is used when the relationship between input features and the target variable follows a curved pattern rather than a straight line.

* **Difference Between Linear and Polynomial Regression:** Understood that Linear Regression fits a straight line, whereas Polynomial Regression adds polynomial features to capture curved relationships in the data.

* **Polynomial Features:** Learned how original features can be transformed into higher-degree features. For example, a degree 2 model includes squared features, which help the model learn a curved relationship.

* **Polynomial Regression Degree:** Understood the role of degree in Polynomial Regression. In this practical, I used degree 2 to create a quadratic relationship.

* **Scikit-learn Pipeline:** Used `make_pipeline()` to combine `PolynomialFeatures` and `LinearRegression` into a single workflow. This makes it easier to transform the input data and train the regression model together.

* **Model Training and Prediction:** Trained the Polynomial Regression model using training data and used it to predict house prices for the test dataset.

* **Model Evaluation:** Used two evaluation metrics:

  * **Mean Absolute Error (MAE):** Measures the average absolute difference between actual and predicted house prices. A lower MAE indicates smaller prediction errors.
  * **R² Score:** Measures how well the model explains the variation in the target values. A higher score generally indicates better model performance.

* **Training and Testing Performance:** Calculated R² scores for both training and testing data to understand how the model performs on data it has learned from and unseen data.

* **Data Visualization:** Used Matplotlib to display actual house-price data points and the curved prediction line learned by the Polynomial Regression model.

## Practical Work

* Imported NumPy, Pandas, Matplotlib and required Scikit-learn libraries.
* Loaded the preprocessed house-price dataset using `pd.read_csv()`.
* Selected a random sample of 80 houses using `df.sample()` to make the visualization easier to understand.
* Separated the input features (X) and target variable (y), where price was the target.
* Divided the dataset into 80% training data and 20% testing data using `train_test_split()`.
* Created a Polynomial Regression model of degree 2 using `PolynomialFeatures(degree=2)` and `LinearRegression()`.
* Combined both steps using `make_pipeline()` and trained the model using `fit()`.
* Predicted house prices for the testing and training datasets using `predict()`.
* Evaluated the model using Mean Absolute Error and R² Score.
* Compared training and testing R² scores to understand the model's performance.
* Created a visualization using Matplotlib to show actual house data points and the curved prediction line.

## Learning Outcome

By the end of this session, I understood how Polynomial Regression works and why it is useful when data follows a curved relationship. I learned that by transforming original features into polynomial features, a regression model can capture patterns that a simple straight-line model may not represent properly.

I also gained practical experience with Scikit-learn pipelines, model training, prediction and evaluation using MAE and R² Score. Visualizing the results helped me understand how a Polynomial Regression model fits a curve to the given data.

This session helped me understand that choosing the right regression technique depends on the relationship between the input features and the target variable.
