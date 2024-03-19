## Introduction

The k-Nearest Neighbor (KNN) algorithm is a non-parametric, lazy learning algorithm used for classification and regression tasks. It is one of the simplest and most fundamental algorithms in machine learning. <mark style="background: #FFF3A3A6;">The core idea behind KNN is to classify a new data point based on the majority vote of its k nearest neighbors from the training dataset.</mark>

## How KNN Works

The KNN algorithm follows these steps:

1. **Load the data**: Load the training dataset, which consists of labeled examples.
2. **Choose the value of k**: Select the number of nearest neighbors (k) that will be used for classification or regression.
3. **Calculate the distances**: For a new data point, calculate the distance between that point and all the training examples using a distance metric (e.g., Euclidean distance, Manhattan distance, or others).
4. **Find the nearest neighbors**: Select the k training examples that are closest to the new data point based on the calculated distances.
5. **Classify or predict**: For classification tasks, assign the [[concepts/machine learning/Classes|class]] label that is most frequent among the k nearest neighbors. For regression tasks, take the average or median of the target values of the k nearest neighbors.

## Distance Metrics

The choice of distance metric is crucial in the KNN algorithm as it determines how the "closeness" or "similarity" between data points is measured. Some commonly used distance metrics are:

1. **Euclidean Distance**: The straight-line distance between two points in n-dimensional space.

```python
import numpy as np

def euclidean_distance(x1, x2):
    return np.sqrt(np.sum((x1 - x2)**2))
```

2. **Manhattan Distance**: The sum of absolute differences between coordinates of two points.

```python
def manhattan_distance(x1, x2):
    return np.sum(np.abs(x1 - x2))
```

3. **Minkowski Distance**: A generalization of Euclidean and Manhattan distances.

```python
import math

def minkowski_distance(x1, x2, p):
    return (sum(abs(x1 - x2)**p))**(1/p)
```

## Choosing the Value of k

The value of k is a [[entities/general/Hyperparameters of ANN|hyperparameter]] that needs to be tuned for optimal performance. A small value of k can lead to [[concepts/machine learning/Overfitting|overfitting]] , while a large value of k can lead to [[concepts/machine learning/Underfitting|underfitting]]. There is no definitive rule for choosing the best value of k, but some common techniques include:

- Cross-validation: Split the data into training and validation sets, and try different values of k to find the one that minimizes the validation error.
- Domain knowledge: Use prior knowledge about the problem to guide the choice of k.
- Square root rule: Set k to the square root of the number of training examples.

## Advantages and Disadvantages

**Advantages**:

- Simple and easy to understand
- Effective for small and medium-sized datasets
- No assumptions about the underlying data distribution
- Can handle multi-class classification problems

**Disadvantages**:

- Computationally expensive for large datasets
- Sensitive to the choice of distance metric and the value of k
- Susceptible to the [[concepts/machine learning/Curse of Dimentionality|Curse of Dimentionality]]
- Does not work well with high-dimensional sparse data

## Applications

The KNN algorithm has been widely used in various domains, including:

- Pattern recognition
- Image classification
- Recommender systems
- Anomaly detection
- Data compression
- Text categorization

## Example Implementation in Python

Here's a simple implementation of the KNN algorithm in Python using scikit-learn:

```python
from sklearn.neighbors import KNeighborsClassifier
from sklearn.model_selection import train_test_split
from sklearn.datasets import load_iris
import numpy as np

# Load the iris dataset
iris = load_iris()
X, y = iris.data, iris.target

# Split the data into training and testing sets
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Create a KNN classifier with k=5
knn = KNeighborsClassifier(n_neighbors=5)

# Train the classifier
knn.fit(X_train, y_train)

# Make predictions on the test set
y_pred = knn.predict(X_test)

# Calculate the accuracy
accuracy = np.sum(y_pred == y_test) / len(y_test)
print(f"Accuracy: {accuracy * 100:.2f}%")
```

This example loads the iris dataset, splits it into training and testing sets, creates a KNN classifier with k=5, trains the classifier on the training data, makes predictions on the test data, and calculates the accuracy.

## Conclusion

The k-Nearest Neighbor algorithm is a simple yet powerful algorithm for classification and regression tasks. Its simplicity and ability to handle multi-class problems make it a popular choice in many applications. However, it is important to carefully choose the distance metric and the value of k to achieve optimal performance. With the rise of more complex algorithms and deep learning techniques, KNN remains a valuable tool in the machine learning toolkit, especially for small and medium-sized datasets.