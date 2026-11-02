# Day 5 – NumPy Essentials for AI & Machine Learning

Today, I learned about **NumPy (Numerical Python)**, one of the most important Python libraries used in Artificial Intelligence and Machine Learning. NumPy is mainly used for working with numerical data, arrays, matrices, and performing mathematical operations efficiently.

In AI and Machine Learning, data is often represented in the form of numbers, such as rows in datasets, pixel values in images, and numerical features. Although Python lists can store this information, they are comparatively slower when performing large calculations. NumPy provides a special array structure that makes numerical operations faster and more efficient.

## Topics Learned

* **Introduction to NumPy Arrays:** Understood the difference between Python lists and NumPy arrays. Python lists store references to objects, whereas NumPy arrays store elements of the same data type in a continuous block of memory. This makes NumPy more efficient for numerical calculations.

* **Creating NumPy Arrays:** Learned how to create one-dimensional (1D) and two-dimensional (2D) arrays using `np.array()`. Also practised creating arrays using `np.zeros()`, `np.ones()`, and `np.arange()` to generate arrays containing zeros, ones, and sequences of numbers.

* **Array Attributes:** Learned important NumPy attributes such as `.shape`, `.dtype`, and `.ndim`. These help us understand the structure, data type, and number of dimensions of an array.

* **Vectorization:** Learned how to perform mathematical operations directly on entire NumPy arrays without using traditional `for` loops. This process is called vectorization. It makes calculations faster and reduces the amount of code required.

* **Indexing and Slicing:** Understood how to access individual elements, complete rows, and specific columns from NumPy arrays. Also learned how to extract input features (`X`) and target labels (`y`) from a dataset, which is an important step in Machine Learning.

* **Data Filtering and Cleaning:** Learned how to identify and handle invalid values, missing-value placeholders, and outliers using Boolean masking and `np.where()`. These techniques help prepare datasets before using them for model training.

* **Statistical Operations:** Practised calculating statistical values such as mean and median using NumPy functions. Also understood the use of `axis=0` for column-wise calculations and `axis=1` for row-wise calculations.

* **Broadcasting and Standardization:** Learned how NumPy performs operations between arrays of different but compatible shapes. Also understood how to standardize numerical features using their mean and standard deviation.

* **Reshaping and Flattening:** Learned how to change the shape of an array using `.reshape()` and convert a multidimensional array into a one-dimensional array using `.flatten()`. These operations are useful when preparing data for AI models.

* **Matrix Multiplication and Dot Product:** Explored matrix multiplication using `np.dot()` and the `@` operator. Understood how inputs and weights are multiplied to calculate outputs in a neural network.

## Practical Work

During the practical session, I performed different coding exercises to understand how NumPy works and how it can be used for numerical calculations and data preprocessing.

* Created 1D and 2D NumPy arrays and explored their shape, data type, and dimensions.
* Generated arrays containing zeros, ones, and numerical sequences using NumPy functions.
* Performed vectorized mathematical operations, such as adding two arrays and applying a 10% tax to multiple product prices at once.
* Compared the execution time of normal Python loops and NumPy vectorized operations using a dataset of 10 million elements to understand the performance difference.
* Practised indexing and slicing by extracting individual values, complete rows, and specific columns from a sample customer dataset.
* Separated input features (`X`) and target labels (`y`) from datasets to understand how data is prepared for Machine Learning models.
* Used Boolean masking to filter values based on conditions, such as identifying cold and hot temperature readings.
* Practised data cleaning by identifying invalid salary and age values and replacing them using `np.where()`.
* Calculated mean, median, row-wise mean, and column-wise mean using NumPy statistical functions.
* Reshaped a one-dimensional array into a two-dimensional matrix and converted it back into a one-dimensional array using flattening.
* Performed matrix multiplication using input values and weight matrices to understand the basic calculations involved in neural networks.
* Completed a Celsius-to-Fahrenheit conversion using vectorization without writing any `for` loops.
* Normalized a feature matrix using column-wise mean and standard deviation to understand feature standardization.

## Learning Outcome

By the end of this session, I developed a better understanding of NumPy and its importance in numerical computing for Artificial Intelligence and Machine Learning. I learned how to create and manipulate arrays, perform mathematical operations efficiently, extract useful information from datasets, and handle invalid values during data cleaning.

I also understood important concepts such as vectorization, broadcasting, slicing, reshaping, and matrix multiplication. The practical exercises helped me understand how NumPy can be used in real-world data preprocessing tasks.

Overall, this session provided a strong foundation for working with numerical datasets and preparing data for Machine Learning algorithms and neural networks.
