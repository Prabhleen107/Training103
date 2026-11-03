# Day 18 – Introduction to Clustering (Unsupervised Learning)

## Introduction

In this session, I learned about **Unsupervised Learning** and the concept of clustering. Until now, I had worked with supervised learning algorithms such as Linear Regression, Logistic Regression, Decision Trees and Random Forests, where the model learns using labelled data.

In Unsupervised Learning, there are no target labels or predefined answers. The main purpose is to discover hidden patterns, similarities and natural groups within the dataset.

For practical understanding, we worked on a **Customer Segmentation for Retail Marketing** project using the Mall Customers dataset. The goal was to group customers according to their annual income and spending behaviour.

## Topics Learned

### 1. Supervised vs. Unsupervised Learning

I learned the difference between supervised and unsupervised learning.

* **Supervised Learning:** The model is trained using labelled data, where the target variable is already available.
* **Unsupervised Learning:** The model works without target labels and discovers patterns or groups from the available data.

Clustering is one of the important techniques used in Unsupervised Learning.

### 2. Introduction to Clustering

Clustering is a technique that groups similar data points together based on their features.

For example, in a shopping mall, customers can be grouped according to their income and spending habits. This helps businesses understand different types of customers and create suitable marketing strategies.

### 3. Exploring the Mall Customers Dataset

I worked with the `Mall_Customers.csv` dataset, which contained information about 200 customers.

The dataset included:

* **CustomerID:** Unique identification number of each customer.
* **Gender:** Gender of the customer.
* **Age:** Age of the customer.
* **Annual Income:** Annual income in thousands of dollars.
* **Spending Score:** Score between 1 and 100 based on customer spending behaviour.

I used Pandas to load the dataset and explored its structure, dimensions, data types, summary statistics and missing values.

### 4. Data Visualization and Exploratory Data Analysis

Before applying clustering, I explored the customer data using Exploratory Data Analysis (EDA).

I created a scatter plot between Annual Income and Spending Score to understand the distribution of customers.

The visualization showed different natural groups, such as:

* Low income and low spending.
* Low income and high spending.
* Average income and average spending.
* High income and low spending.
* High income and high spending.

This initial observation suggested that dividing customers into five clusters could be useful.

### 5. Feature Scaling

Feature Scaling is important in K-Means because it calculates distances between data points.

If features have different ranges, the feature with larger values can have a greater influence on distance calculations.

I used **StandardScaler** to scale Annual Income and Spending Score. It transforms the features so that they have a mean of 0 and a standard deviation of 1.

This helps both features contribute more equally during clustering.

### 6. K-Means Clustering Algorithm

K-Means is an unsupervised machine learning algorithm that divides data into a fixed number of clusters.

I learned its working process through the following steps:

1. **Choose K:** Decide the number of clusters required.
2. **Initialize Centroids:** Select initial cluster centres.
3. **Assign Data Points:** Assign each data point to its nearest centroid.
4. **Update Centroids:** Calculate the new centre of each cluster.
5. **Repeat:** Continue assigning points and updating centroids until the clusters become stable.

For our project, we selected **K = 5** and trained the K-Means model using the scaled customer data.

### 7. Visualizing and Interpreting Clusters

After training the model, I extracted the cluster labels and centroid positions.

I also converted the scaled centroid coordinates back to their original values using `inverse_transform()`.

I visualized the five customer groups using a scatter plot, where each cluster had a different colour and the centroids were represented using black star markers.

The five customer segments were:

* **Premium Shoppers:** High income and high spending.
* **Conservative Spenders:** High income and low spending.
* **Moderate Spenders:** Average income and average spending.
* **Impulsive Buyers:** Low income and high spending.
* **Budget Shoppers:** Low income and low spending.

These customer groups can help businesses plan different marketing strategies, offers and loyalty programs.

### 8. Elbow Method for Finding Optimal K

The Elbow Method is used to find a suitable number of clusters in K-Means.

It works by running K-Means with different values of K and calculating the **Inertia (Within-Cluster Sum of Squares)** for each value.

Inertia measures how close the data points are to their assigned cluster centroids. As the number of clusters increases, inertia decreases.

We plot the number of clusters against inertia. The point where the curve starts becoming flatter is called the **Elbow Point**.

In our project, the elbow was observed at **K = 5**, supporting our choice of five customer segments.

## Practical Work

During this session, I performed the following practical tasks:

* Imported NumPy, Pandas, Matplotlib, Seaborn and Scikit-learn libraries.
* Loaded the `Mall_Customers.csv` dataset using Pandas.
* Explored the dataset using `head()`, `info()`, `describe()` and `shape`.
* Checked missing values using `isnull().sum()`.
* Created a scatter plot of Annual Income versus Spending Score.
* Selected Annual Income and Spending Score as clustering features.
* Applied StandardScaler to scale the selected features.
* Implemented K-Means clustering with five clusters using `KMeans`.
* Extracted cluster labels and centroid positions.
* Converted scaled centroids back to their original values.
* Visualized customer segments using different colours and centroid markers.
* Interpreted the five customer groups based on their income and spending behaviour.
* Applied the Elbow Method by testing K values from 1 to 10.
* Plotted inertia values to identify the suitable number of clusters.

## Learning Outcome

By the end of this session, I understood the basic concept of Unsupervised Learning and how clustering helps discover hidden patterns in unlabelled data. I learned how the K-Means algorithm works using centroids, distance calculations and repeated updates.

I also understood why feature scaling is important for distance-based algorithms and how the Elbow Method helps select the optimal number of clusters.

Through the Mall Customer Segmentation project, I gained practical experience in grouping customers based on their income and spending behaviour. This session helped me understand how clustering can be used in real-world applications such as customer analysis, targeted marketing and business decision-making.
