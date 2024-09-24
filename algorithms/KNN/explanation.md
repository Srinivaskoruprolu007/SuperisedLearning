# K-Nearest Neighbors (KNN)

## Overview:

K-Nearest Neighbors (KNN) is an instance-based learning algorithm. It is a simple, non-parametric, and lazy learning algorithm used for classification and regression tasks. In KNN, predictions are made by identifying the 'K' closest data points (neighbors) to the query point and making decisions based on these neighbors.

### 1. How it Works:

1. **Choose a value for K**: Select the number of neighbors you want to consider for making the prediction.
2. **Distance Calculation**: Compute the distance between the query point and all points in the training set.
3. **Find K-nearest neighbors**: Identify the K closest neighbors to the query point.
4. **Make a Prediction**: For classification, use a majority vote from the neighbors. For regression, use the average of the K neighbors' values.

### 2. Distance Metrics:

The most common distance metrics used in KNN are:

- **Euclidean Distance**:
  $$ d(x, y) = \sqrt{\sum\_{i=1}^{n} (x_i - y_i)^2} $$
  This is the most commonly used distance metric in KNN. It measures the straight-line distance between two points in Euclidean space.
- **Manhattan Distance**:
  $$ d(x, y) = \sum\_{i=1}^{n} |x_i - y_i| $$

  This is the sum of the absolute differences between coordinates of a pair of objects. It's often used in grid-like paths.

- **Minkowski Distance**:
  $$
  d(x, y) = \left(\sum_{i=1}^{n} |x_i - y_i|^p\right)^{1/p}
  $$
  This is a generalized form of both Euclidean and Manhattan distances.

### 3. Choosing K:

- **Small K (e.g., K=1)**: High variance, more sensitive to noise.
- **Large K**: High bias, smoother decision boundaries, but might overlook important details.

### 4. Advantages:

- **Simple to Implement**: Easy to understand and apply for both classification and regression.
- **No Assumptions**: KNN does not make any assumptions about the underlying data distribution.
- **Versatile**: Can be used for various types of problems and datasets.

### 5. Disadvantages:

- **Computationally Expensive**: The algorithm requires computing the distance between the test point and every other point in the dataset.
- **Sensitive to Noise**: KNN can misclassify data points when the dataset contains noisy data or irrelevant features.
- **Curse of Dimensionality**: In high-dimensional spaces, distance metrics become less effective.

### 6. Real-World Applications:

- **Recommendation Systems**: E.g., Amazon or Netflix recommendations based on users with similar preferences.
- **Medical Diagnosis**: Classification of diseases based on symptoms and historical patient data.
- **Fraud Detection**: Detecting fraudulent activities by comparing with past similar transactions.
