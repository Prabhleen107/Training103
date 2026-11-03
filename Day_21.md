# Day 21 – Building a Healthcare Risk Prediction App Using Streamlit

## Introduction

After completing Exploratory Data Analysis (EDA) and training a Random Forest model, the next step is to make the machine learning model usable through an application.

A trained model normally works in the Python environment, but users cannot easily interact with it. To solve this problem, we can use **Streamlit**, a Python library that helps us create simple and interactive web applications without requiring advanced frontend development.

In this lesson, I continued the Healthcare Risk Prediction project by creating a web application using Streamlit. The application allows users to enter basic health information and receive a prediction from the previously trained machine learning model.

## Topics Learned

### 1. Introduction to Streamlit

Streamlit is an open-source Python library used to create interactive web applications, especially for Data Science and Machine Learning projects.

It allows us to convert Python scripts into web applications using simple commands.

Some important Streamlit features are:

* `st.title()` – Displays the main heading of the application.
* `st.header()` – Adds a section heading.
* `st.write()` – Displays text and other information.
* `st.number_input()` – Takes numerical input from users.
* `st.button()` – Creates a clickable button.
* `st.success()` – Displays a success message.
* `st.warning()` – Displays a warning message.

### 2. Loading the Trained Machine Learning Model

In the previous lesson, the Random Forest model was trained and saved using the Pickle library.

In this lesson, I learned how to load that saved model into the application.

The saved file is located at:

`model/healthcare_model.pkl`

The Pickle library helps us save and load Python objects, including trained machine learning models.

This allows us to use an already trained model without training it again whenever the application runs.

### 3. Taking Input from Users

The application collects health-related information from users through input fields.

The inputs can include:

* Age
* Glucose level
* Blood pressure
* Cholesterol level
* BMI

Streamlit input components make it easy for users to enter these values.

### 4. Making Predictions

After collecting the user's information, the application prepares the input data in the same feature order used during model training.

The loaded Random Forest model receives these values and predicts the patient's risk category.

The output is based on the model trained in the previous lesson:

* **0 – Healthy:** The model predicts a lower risk category.
* **1 – At Risk:** The model predicts a higher risk category.

The prediction is displayed on the application screen.

### 5. Displaying Results

Streamlit provides different methods to display prediction results in an understandable format.

For example:

* `st.success()` can display a lower-risk prediction.
* `st.warning()` can display a higher-risk prediction.
* `st.write()` can display additional information.

This makes the application simple and easy to understand for users.

### 6. Running the Streamlit Application

After creating the `app.py` file, the application can be started through the terminal.

The command used is:

`streamlit run app.py`

This starts a local web server and opens the application in a browser.

## Practical Work

During this lesson, I focused on developing the frontend of the Healthcare Risk Prediction project.

The main practical tasks included:

* Installing and importing the Streamlit library.
* Creating an `app.py` Python file.
* Loading the previously trained healthcare prediction model using Pickle.
* Creating a title and sections for the application.
* Adding input fields for age, glucose, blood pressure, cholesterol and BMI.
* Collecting user inputs through Streamlit components.
* Passing the input values to the trained Random Forest model.
* Displaying the predicted risk category.
* Running the application locally using the Streamlit command.

## Learning Outcome

In this lesson, I learned how to convert a trained machine learning model into an interactive web application using Streamlit. I understood how to load a saved model, collect user inputs, pass data for prediction and display the results through a simple interface.

This lesson helped me understand how machine learning models can be connected with real-world applications. It also brought the Healthcare Risk Prediction project closer to becoming a complete application.

**Note:** This application is an educational project and its predictions should not be treated as medical diagnoses or professional medical advice.
