# Unsupervised Learning

Unsupervised learning is a type of machine learning where the model is trained on data without labeled responses. The goal is to find hidden patterns in the input data. Unsupervised learning works with input data only.

# Objective

The objective of this assessment is to evaluate your understanding and ability to apply clustering techniques to a real-world dataset.

# Dataset

Loaded Iris dataset from sklearn library

Target variables are removed by dropping species column since this is a clustering problem.

# Data Preprocessing
Performed basic EDA using functions like info(), describe(), columns, head() etc.

Renamed columns

* Dataset represented using scatter plot

To understand the distribution of the data, scatter polt is drawn.

* Feature Scaling 

Features in a dataset can have different units and scales. Scaling ensures that all features contribute equally to the clustering process.

Feature scaling is done using MinMax and standard scaler.

# Clustering with K Means Clustering

1. Elbow plot is drawn to find the number of clusters. The point where the within-cluster sum of squares (WCSS) starts to decrease more slowly (the "elbow"). In the iris dataset, number of clusters is 3.
2. K Means cluster object with 3 clusters is created.
3. Data is fit and predicted.
4. Scatter plots with and without clusters of different colours are drawn.

After feature scaling, data points are more organised with three clusters and each centroids at the centre of each clusters.

5. To check the quality of clusters, silhouette score is calculated. For the Iris dataset, the silhouette score often peaks at 2 or 3 clusters.

The Iris dataset contains three classes of iris plants, which form relatively distinct clusters. K-means aims to partition data into clusters where each data point belongs to the cluster with the nearest mean, making it effective for datasets with such natural groupings. The Iris dataset has only four features (sepal length, sepal width, petal length, and petal width). So, it has low Dimensionality making it easier for K-means to perform well without the need for dimensionality reduction techniques.

# Clustering with Hierarchical Clustering

1. Dendrogram is plotted to find the number of clusters. Inspecting the dendrogram to identify the longest vertical distance that can be cut horizontally. For the Iris dataset, this typically suggests around 3 clusters.
2. Built the model using Agglomerative clustering.
3. Clusters are visualised using sctter plot. Each cluster is of different colour.
4. Silhoutte score is calculated. It is highest at 2 clusters.

The Iris dataset is relatively small, with 150 samples, making hierarchical clustering computationally feasible even with the algorithm's higher complexity compared to K-means. The dendrogram provides a visual representation of how clusters are formed and merged, which can be more intuitive than the centroid-based representation in K-means.
