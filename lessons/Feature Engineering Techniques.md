---
subject: Feature Engineering Techniques
depth: Middle
complexity: Highest
---

## Introduction to Feature Engineering

**What is Feature Engineering?**
Feature engineering is the process of transforming raw data into [[Feature|features]] that better represent the underlying problem to the predictive models, resulting in improved model accuracy on unseen data.

**Why is it important?**
- Raw data is often not in a form that is suitable for machine learning algorithms
- Feature engineering can help expose additional relevant information to the model
- It can significantly improve model performance and predictive power

**When is it needed?**
- For any supervised machine learning task (classification, regression)
- When working with structured or unstructured data
- When dealing with high-dimensional data

Let's start with a simple example. Say you have a dataset with a column for 'Age' and you want to predict something based on age groups rather than exact ages. You could create a new feature 'AgeGroup' by bucketing the ages into different ranges.

Great, let's move to the next block.

## Techniques for Feature Creation

There are several techniques we can use to create new features from existing ones. Let's go through some of the most common ones:

**Numerical Transformations**
- Log transform: Helpful when data is right-skewed
- Reciprocal: 1/x can reduce the impact of large values
- Square root: Similar effect as log transform
- Interaction terms: Multiplying two features to get a new one (e.g. Age * Income)

**Categorical Encoding**
- One-hot encoding: Encoding categorical variables as binary vectors
- Target encoding: Replacing categories with target mean for that category
- Ordinal encoding: Assigning ordered numerical values to categories

**Example**:
```python
# One-hot encoding
encoded = pd.get_dummies(data['Category'], prefix='Category')

# Target encoding 
data['Category_encoded'] = data.groupby('Category')['Target'].transform('mean')
```

### Log transform

- Applies the logarithm function to the feature values
- Useful when data is right-skewed (long tail on the positive side)
- Helps reduce the impact of outliers and large values

For example, If a feature has values

$$ [1, 2, 5, 10, 500] $$

applying logarithm function

$$A = \begin{bmatrix} 1 & 2 & 5 & 10 & 500 \end{bmatrix}  \xrightarrow{\ln()}  B = \begin{bmatrix} \ln(1) & \ln(2) & \ln(5) & \ln(10) & \ln(500) \end{bmatrix} 
$$

log transform gives

$$[0, 0.69, 1.61, 2.30, 6.21]$$
### Reciprocal Transform

- Takes the reciprocal (1/x) of the feature values
- Like log transform, it reduces the impact of large values
- Useful when you want to treat larger values as lower weights

For example, if feature has values

$$ [1, 2, 5, 10] $$

taking reciprocal ($1/x$) gives
$$ [1, 0.5, 0.2, 0.1] $$

### Square Root Transform

- Applies square root to the feature values
- Also helps reduce the impact of outliers, but not as much as log

$$
A = \begin{bmatrix} 1 & 4 & 9 & 16 \end{bmatrix}  \xrightarrow{\sqrt n}  B = \begin{bmatrix} \ln(1) & \ln(2) & \ln(3) & \ln(4) \end{bmatrix} 
$$

### Target encoding

- Replaces categories with the mean of the target for that category
- Helps capture the relationship between categories and target
- Example: If 'Red' maps to 0.7 average target, replace 'Red' with 0.7

## Techniques for Feature Selection

While creating more features can be beneficial, it can also lead to the curse of dimensionality. Feature selection helps us reduce the number of input features by selecting only the most relevant ones.

**Filter Methods**:

- Use statistical measures to score feature relevance
- Examples: Correlation coefficients, mutual information, chi-square test

**Wrapper Methods**:

- Use a model itself to evaluate and select features
- Examples: Recursive feature elimination, forward/backward selection

**Embedded Methods**:

- Perform feature selection as part of the model construction
- Examples: LASSO regression, [[Decision Trees|tree-based algorithms]]

Let's look at an example of using a filter method:

```python
from sklearn.feature_selection import mutual_info_classif

# Mutual information for classification
X = data[['Age', 'Income', 'log_income']]
y = data['Target']
mi = mutual_info_classif(X, y)

# Sort features by importance
feature_scores = pd.Series(mi, index=X.columns)
top_features = feature_scores.sort_values(ascending=False)[:2]
print(top_features)
```

This will print the top 2 most relevant features based on mutual information with the target variable.

#lesson