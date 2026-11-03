# Day 10 – Exploratory Data Analysis: Data Visualization and Correlation Analysis

On Day 10 of my AI and Machine Learning training, I continued working on Exploratory Data Analysis using the King County House Prices dataset. After understanding the structure and basic statistics of the dataset, I focused on studying relationships between different house features and their prices.

I used different visualizations such as scatter plots, box plots, bar plots, and heatmaps with Seaborn. These visualizations helped me understand how different factors are related to house prices and identify unusual values in the dataset.

## Topics Learned

* **Bivariate Analysis:** Learned how to study the relationship between two variables to understand how one feature is associated with another.

* **Scatter Plot:** Used scatter plots to understand the relationship between living area and house price. Each point represents a house, making it easier to identify patterns between the two features.

* **Box Plot:** Learned how box plots display the median, spread, quartiles, and possible outliers in numerical data. Used them to compare prices of waterfront and non-waterfront houses.

* **Bar Plot:** Used bar plots to compare the average house price for different house condition ratings.

* **Outlier Detection:** Learned how to identify unusual observations in a dataset, such as houses with an extremely high number of bedrooms. These values may require further investigation before model training.

* **Correlation:** Understood how correlation measures the relationship between numerical features. Its value ranges from -1 to +1. Positive correlation indicates that two variables tend to increase together, while negative correlation indicates an opposite relationship.

* **Correlation Heatmap:** Learned how to use heatmaps to represent correlations between multiple numerical features through different colours and numerical values.

* **Missing Value Checking:** Used `isnull().sum()` to check the number of missing values in each column.

* **Saving the Dataset:** Learned how to save a selected dataset into a CSV file using `to_csv()` so that it can be used in future practical work.

## Practical Work

* Created a scatter plot to study the relationship between house living area and price, using different colours for waterfront and non-waterfront houses.
* Created a box plot to compare house prices based on waterfront availability.
* Used a bar plot to visualize the average house price for different house condition ratings.
* Identified houses with more than 10 bedrooms to investigate extreme values in the dataset.
* Calculated the correlation matrix using `df.corr()`.
* Created a correlation heatmap using Seaborn to visualize relationships between numerical features.
* Checked missing values in the selected columns using `df.isnull().sum()`.
* Saved the simplified dataset as `kc_house_filtered.csv` for further use.

## Learning Outcome

By the end of Day 10, I understood how to use different visualizations to study relationships between features in a dataset. I learned how to identify possible outliers, compare categories, and understand correlations between numerical variables.

Through the House Prices dataset, I observed that living area had a strong positive correlation with house price, approximately +0.70. I also observed that waterfront houses generally had higher prices in the dataset.

Finally, I learned how to check for missing values and save the selected dataset for future work. This practical improved my understanding of EDA and prepared me for the next stage of data preprocessing before machine learning model training.
