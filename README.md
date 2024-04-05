# PCA Algorithm Implementation on IRIS Dataset

## Introduction to IRIS Dataset

The IRIS dataset is a classic dataset in the field of pattern recognition and machine learning. It consists of 150 samples of iris flowers, each with four features: sepal length, sepal width, petal length, and petal width. The dataset is commonly used for classification and clustering tasks.

## Role of Eigen Vectors and Eigen Values in PCA

Principal Component Analysis (PCA) is a dimensionality reduction technique that aims to transform the data into a new coordinate system such that the greatest variance by any projection of the data comes to lie on the first coordinate (called the first principal component), the second greatest variance on the second coordinate, and so on. Eigenvalues represent the magnitude of the variance of the data along the principal components, while eigenvectors represent the direction of these principal components.

## Implementation Details

### Data Standardization

Before applying PCA, the data is standardized to have a mean of 0 and a standard deviation of 1. This is done to ensure that all features contribute equally to the analysis.

### PCA Algorithm

1. Compute the covariance matrix of the standardized data.
2. Calculate the eigenvalues and eigenvectors of the covariance matrix.
3. Sort the eigenvalues in descending order and select the top k eigenvectors corresponding to the largest eigenvalues.
4. Project the data onto the selected eigenvectors to obtain the principal components.

### Principal Component Features

Two principal components are chosen based on the top eigenvectors, representing the dominant features of the dataset.

### K-Means Clustering

The K-Means algorithm is applied to the projected data to cluster it into groups. The centroids of these clusters are used to classify the data points.

### Accuracy Verification

The accuracy of the K-Means clustering is calculated by comparing the predicted labels with the original labels of the dataset. The majority of the data is retrieved with an accuracy of 92%, indicating that although the dimensionality of the data is reduced from 4 to 2, the essential information is preserved.
