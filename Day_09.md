# Day 9 – Introduction to Exploratory Data Analysis (EDA)

On Day 9 of my AI and Machine Learning training, I started learning about **Exploratory Data Analysis (EDA)** using a real-world House Prices dataset from King County, USA. The dataset contained information about more than 21,000 houses, including their prices, bedrooms, bathrooms, living area, floors, and other features.

The main purpose of this practical was to explore the dataset and understand its structure and important features. I used Python libraries such as Pandas, NumPy, Matplotlib, and Seaborn to examine the data, calculate statistical information, and create visualizations.

EDA is an important step in machine learning because it helps us understand the data before applying machine learning algorithms.

## Topics Learned

* **Introduction to EDA:** Learned how to explore and understand a dataset using statistical methods and visualizations before building a machine learning model.

* **Loading Python Libraries:** Used Pandas for data manipulation, NumPy for numerical operations, Matplotlib for creating graphs, and Seaborn for statistical visualizations.

* **Loading the Dataset:** Learned how to load a CSV file using `pd.read_csv()` and store the data in a Pandas DataFrame.

* **Dataset Inspection:** Used functions like `head()`, `info()`, `describe()`, `shape`, and `columns` to understand the structure, size, column names, data types, and statistical summary of the dataset.

* **Feature Selection:** Learned how to select important columns from a large dataset. Selected eight features: price, bedrooms, bathrooms, sqft_living, floors, waterfront, yr_built, and condition.

* **Statistical Analysis:** Used `describe()` to calculate important statistical values such as mean, standard deviation, minimum, maximum, and quartiles.

* **Univariate Analysis:** Learned how to analyze one variable at a time to understand its distribution and frequency.

* **Histogram:** Used a histogram with a KDE curve to understand how house prices were distributed and identify the general pattern of the data.

* **Count Plot:** Learned how to visualize the frequency of different categories, such as the number of houses having different bedroom counts.

## Practical Work

* Imported Pandas, NumPy, Matplotlib, and Seaborn libraries.
* Loaded the King County House Prices dataset containing more than 21,000 house records.
* Checked the number of rows and columns using `shape`.
* Inspected column names and selected eight important features for analysis.
* Used `head()` to view the first few records.
* Used `info()` to understand column data types and dataset structure.
* Used `describe()` to generate the statistical summary of numerical columns.
* Created a histogram using Seaborn to visualize the distribution of house prices.
* Created a count plot to understand the distribution of bedrooms among houses.

## Learning Outcome

By the end of Day 9, I understood the basic concept and importance of Exploratory Data Analysis. I learned how to load a real-world dataset, inspect its structure, select relevant features, and calculate statistical summaries.

I also learned how to use histograms and count plots to understand the distribution of numerical and categorical data. This practical helped me understand how data scientists explore datasets and identify useful information before starting the machine learning process.
