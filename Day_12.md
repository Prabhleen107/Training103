# Day 12 – Linear Regression: Training Our First Machine Learning Model 

On Day 12, I started working with my first Machine Learning model using **Linear Regression**. In the previous session, I learned about data preprocessing, where we prepared the house-price dataset by handling missing values, outliers, scaling and encoding categorical data.

In this session, I used the preprocessed house-price dataset to train a Machine Learning model that can predict house prices based on different features.

Linear Regression is a supervised Machine Learning algorithm used to predict continuous numerical values. For example, when the size of a house increases, its price generally increases as well. Linear Regression learns this relationship and finds the best-fit straight line through the data points. It then uses this learned relationship to predict prices for new houses.

## Topics Learned

* **Introduction to Linear Regression:** Learned how Linear Regression works and how it identifies the relationship between input features and a target variable to make predictions.

* **Importing Libraries and Loading Data:** Used Pandas, Matplotlib, Seaborn and Scikit-learn. Loaded the preprocessed house-price dataset using `pd.read_csv()`.

* **Train-Test Split:** Learned why a dataset is divided into two parts:

  * Training Data (80%): Used by the model to learn patterns from the dataset.
  * Testing Data (20%): Used to evaluate the model on data it has not seen during training.

  Used `train_test_split()` from Scikit-learn to divide the dataset.

* **Features and Target Variable:** Separated the input features (X), which contain information about houses, from the target variable (y), which contains the actual house prices. The model uses the features to predict the target.

* **Simple Linear Regression:** Trained a model using only one feature, `Scaled_size`, to predict house prices. This helped me understand how a model learns the relationship between a single input feature and the output.

* **Model Coefficient and Intercept:** Learned about the mathematical equation of a straight line:

  **y = mx + c**

  Here, `m` represents the slope or coefficient, and `c` represents the intercept. In Linear Regression, the model learns these values during training to create its best-fit line.

* **Model Visualization:** Used Matplotlib to visualize actual house prices and predicted prices. A scatter plot represented actual test houses, while a line plot showed the model's prediction line.

* **Multiple Linear Regression:** Learned how to train a model using multiple input features instead of just one. Used features such as bedrooms, bathrooms, house size, floors, waterfront status, condition and location categories to predict house prices.

* **Custom House Price Prediction:** Created a custom house record using a Pandas DataFrame and provided values for all the required features. The trained multiple regression model then predicted its house price.

* **Model Evaluation:** Learned how to measure the performance of a regression model using two important evaluation metrics:

  * **Mean Absolute Error (MAE):** Measures the average absolute difference between actual and predicted values. A lower MAE indicates better predictions.
  * **R² Score:** Measures how well the model explains the variation in house prices. A higher R² score generally indicates a better-fitting model.

## Practical Work

* Loaded the preprocessed house-price dataset, `kc_house_preprocessed.csv`, using Pandas.
* Divided the dataset into 80% training data and 20% testing data.
* Separated the input features (X) and target variable (y).
* Built and trained a Simple Linear Regression model using only the `Scaled_size` feature.
* Extracted the coefficient and intercept to understand the equation learned by the model.
* Visualized actual house prices and the best-fit prediction line using Matplotlib.
* Built a Multiple Linear Regression model using all available preprocessed features.
* Predicted house prices for the test dataset using both models.
* Created a custom house with specific features and predicted its price using the trained multiple regression model.
* Evaluated both models using MAE and R² Score.
* Compared the performance of Simple and Multiple Linear Regression models to understand the effect of using additional features.

## Learning Outcome

By the end of this session, I understood how a Machine Learning model learns from data and makes predictions. I learned the difference between Simple Linear Regression, which uses one input feature, and Multiple Linear Regression, which uses multiple input features.

I also understood the importance of splitting data into training and testing sets so that a model can be evaluated on unseen data. Working with MAE and R² Score helped me understand how to measure prediction errors and evaluate model performance.

The most important learning from this session was that providing more useful and relevant features can improve prediction performance. Features such as house size, bedrooms, bathrooms and location can help a model understand house prices more effectively.

This session was my first practical experience with training, testing, predicting and evaluating a Machine Learning model using Python and Scikit-learn.
