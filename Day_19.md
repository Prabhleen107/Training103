# Day 19 – Exploratory Data Analysis (EDA) on Healthcare Data

## Introduction

In this session, I learned about **Exploratory Data Analysis (EDA)** using a healthcare dataset. EDA is an important step in Machine Learning because it helps us understand the data before training a model.

It involves analyzing, summarizing and visualizing data to identify patterns, detect unusual values, check missing information and understand relationships between different features.

In this practical, I worked with the `test_healthcare_data.csv` dataset, which contains patient health information. The main objective was to explore different health metrics and understand their distributions and correlations before building a Machine Learning classification model.

## Topics Learned

### 1. Introduction to Exploratory Data Analysis

EDA helps us understand the structure and characteristics of a dataset before applying Machine Learning algorithms.

It mainly involves:

* Understanding the dataset and its features.
* Checking the number of rows and columns.
* Identifying missing values.
* Calculating basic statistical information.
* Visualizing data distributions and relationships.

### 2. Loading the Healthcare Dataset

I used Pandas to load the `test_healthcare_data.csv` dataset.

I also imported the required Python libraries:

* **Pandas:** For loading and handling tabular data.
* **NumPy:** For mathematical and numerical operations.
* **Matplotlib:** For creating different types of graphs.
* **Seaborn:** For creating statistical visualizations.

### 3. Inspecting the Dataset

After loading the dataset, I explored its structure to understand the available information.

I used `df.shape` to check the number of rows and columns and `df.head()` to display the first five records.

This helped me get an initial understanding of the patient data and its features.

### 4. Checking Missing Values

Missing values are empty entries in a dataset that may create problems during Machine Learning model training.

I used `df.isnull().sum()` to check the number of missing values in each column.

The dataset contained no missing values, so no additional imputation or missing-value treatment was required.

### 5. Statistical Summary

I used the `describe()` function to generate a statistical summary of the numerical columns.

It provided important information such as:

* **Count:** Number of available values.
* **Mean:** Average value.
* **Standard Deviation:** Measures how spread out the values are.
* **Minimum and Maximum:** Smallest and largest values.
* **Quartiles:** Divide the data into four equal parts.

This helped me understand the general range and distribution of patient health measurements.

### 6. Data Visualization

I created different visualizations to understand the distribution of patient metrics and relationships between health features.

**A. Age Distribution**

I created a histogram with a KDE curve to understand how patient ages were distributed in the dataset.

**B. Glucose vs. Cholesterol Levels**

I used a scatter plot to study the relationship between fasting glucose and total cholesterol levels. This visualization helped examine how these two health measurements were distributed together.

**C. Correlation Matrix Heatmap**

I created a correlation matrix using `df.corr()` and visualized it with a Seaborn heatmap.

Correlation values range from -1 to +1:

* **+1:** Strong positive correlation.
* **-1:** Strong negative correlation.
* **0:** No linear correlation.

The heatmap helped visualize relationships between different numerical health metrics.

## Practical Work

During this session, I performed the following practical tasks:

* Imported Pandas, NumPy, Matplotlib and Seaborn libraries.
* Loaded the `test_healthcare_data.csv` dataset using `pd.read_csv()`.
* Checked the dataset dimensions using `df.shape`.
* Displayed the first five records using `df.head()`.
* Checked missing values using `df.isnull().sum()`.
* Generated statistical summaries using `df.describe()`.
* Created an age distribution histogram with a KDE curve.
* Created a scatter plot to visualize glucose and cholesterol levels.
* Calculated correlations between numerical health features.
* Created a correlation matrix heatmap using Seaborn.

## Learning Outcome

By the end of this session, I understood how Exploratory Data Analysis helps us examine and understand a dataset before building a Machine Learning model.

I gained practical experience in loading healthcare data, checking its structure, identifying missing values, calculating statistical summaries and creating different visualizations.

I also learned how histograms, scatter plots and correlation heatmaps help us understand patterns and relationships between health measurements.

This session prepared me for the next step, where I will define health risk guidelines, assign labels to patients and train a Machine Learning classification model.
