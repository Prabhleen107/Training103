# Day 6 – Pandas Essentials: DataFrames and Data Manipulation

Today, I learned about **Pandas**, an important Python library used for data analysis, data cleaning, and data manipulation. Pandas is built on top of NumPy and provides powerful tools to work with tabular datasets in the form of rows and columns.

In Artificial Intelligence and Machine Learning, working with datasets is an essential step before training any model. Pandas makes it easier to load data from external files, inspect records, select specific columns, filter information, handle missing values, and perform statistical analysis.

## Topics Learned

* **Introduction to Pandas:** Understood what Pandas is and why it is widely used in Data Science and Machine Learning. Learned how it combines the flexibility of Python with the numerical efficiency of NumPy and provides labelled rows and columns for working with structured data.

* **Pandas Data Structures – Series and DataFrame:** Learned about the two main data structures of Pandas. A **Series** is a one-dimensional labelled data structure, whereas a **DataFrame** is a two-dimensional tabular structure containing rows and columns. Practised creating Series from lists and DataFrames from dictionaries.

* **Reading and Loading Datasets:** Learned how to load external CSV files into Pandas using `pd.read_csv()`. Also explored loading CSV data using Python's `io.StringIO` to work with sample datasets without creating an external file.

* **Dataset Inspection:** Practised different functions used to understand the structure and contents of a dataset, such as `head()`, `tail()`, `info()`, `describe()`, `shape`, `columns`, `index`, and `dtypes`. These functions help identify the number of records, column names, data types, and basic statistical information.

* **Selecting and Slicing Data:** Learned how to select individual columns, multiple columns, and specific rows from a DataFrame. Understood the difference between `.loc[]`, which is used for label-based selection, and `.iloc[]`, which selects data using integer positions.

* **Boolean Indexing and Filtering:** Learned how to filter dataset records using conditions. Practised using comparison operators and bitwise operators such as `&` (AND), `|` (OR), and `~` (NOT) to select rows that satisfy specific conditions.

* **Handling Missing Data:** Understood that real-world datasets often contain missing values represented by `NaN`. Learned how to identify missing values using `isnull().sum()`, fill missing values using `fillna()`, and remove incomplete records using `dropna()`.

* **Groupby and Aggregation:** Learned how to group dataset records according to a particular column using `groupby()`. Also explored aggregation functions such as `mean()`, `sum()`, and `count()` to calculate useful statistical summaries for different groups.

## Practical Work

During the practical session, I performed different exercises to understand how Pandas can be used for handling and analysing real-world datasets.

* Imported Pandas and NumPy libraries and practised creating Pandas Series from Python lists.
* Created DataFrames using dictionaries containing student information such as names, courses, and roll numbers.
* Loaded customer datasets from CSV files using `pd.read_csv()` and also practised reading sample CSV data using `io.StringIO`.
* Explored dataset information using `head()`, `tail()`, `info()`, `describe()`, `shape`, `columns`, `index`, and `dtypes`.
* Practised selecting individual columns and multiple columns from a DataFrame and understood the difference between Series and DataFrame outputs.
* Used `.loc[]` and `.iloc[]` to select particular rows and columns based on labels and integer positions.
* Applied Boolean indexing to filter customer records based on conditions such as income greater than a specific value and selecting female customers with a particular income range.
* Identified missing values in customer datasets using `isnull().sum()` and calculated column averages to fill missing age and income values.
* Practised handling incomplete records using `fillna()` and `dropna()` and understood when to fill missing values and when to remove records.
* Used `groupby()` to calculate average age and income based on customer gender and purchase status.
* Completed hands-on exercises using a student evaluation dataset, including loading and inspecting records, filtering students who passed, selecting their study hours and grades, and handling missing values.
* Calculated group-wise average study hours, grades, and attendance by grouping students according to their passing status.

## Learning Outcome

By the end of this session, I developed a better understanding of Pandas and its importance in Data Science and Machine Learning. I learned how to create Series and DataFrames, load datasets, inspect their structure, and extract useful information from rows and columns.

I also gained practical experience in filtering records, handling missing values, cleaning datasets, and performing group-wise statistical analysis. The exercises helped me understand how to work with structured data and prepare it for further processing.

Overall, this session strengthened my data manipulation and preprocessing skills. These concepts will be useful in upcoming Machine Learning tasks, where clean, organised, and properly analysed datasets are required before training models.
