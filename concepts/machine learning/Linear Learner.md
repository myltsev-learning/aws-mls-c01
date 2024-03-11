## Definition

A Linear Learner algorithm is a supervised machine learning algorithm. It's used to find a linear (straight line) relationship between input [[Feature|features]] (your data) and an output value. In higher dimensions it becomes a hyperplane. The goal is to accurately predict the output variable for new, unseen data.

We can use it for two main purposes:

### Regression

Predicting a continuous numerical value (e.g., predicting housing prices).

### Classification

Categorizing data into classes (e.g., classifying email as "spam" or "not spam").

## Loss function

A Linear Learner uses something called a "[[concepts/neural networks/Loss Function|loss function]]" to measure how wrong its predictions are. Popular choices are mean squared error (for regression) and logistic loss (for classification).

The goal of the algorithm is to _minimize_ this loss function. It does this by adjusting the line's position (the weights and biases that define it). This step-by-step adjustment is often done using an algorithm called [[concepts/machine learning/Gradient descent|gradient descent]].

## Learning process

1. **Initialization:** The Linear Learner starts with random parameters (the initial definition of our line).
2. **Predictions:** It makes predictions using the current line.
3. **Evaluation:** The loss function measures how far off the predictions are.
4. **Update:** Gradient descent calculates an adjustment to the parameters, hopefully making the predictions better.
5. **Repeat:** Steps 2-4 repeat over many iterations until the loss function stops improving significantly.

## Types of Linear Learner

- **Linear Regression:** The most basic type, used for predicting a continuous numerical outcome (like predicting housing prices).
- **Logistic Regression:** Despite the name, this does classification! It predicts the probability of belonging to a class (like "spam" or "not spam").
- **Ridge Regression and Lasso Regression:** These are called "regularized" linear regression. They introduce penalties that try to keep the model simpler, which can prevent overfitting (meaning the model fits the training data _too_ well and performs poorly on new data).
- **Support Vector Machines (SVMs) for Classification:** Very powerful classifiers, they can create even non-linear decision boundaries to separate the categories.


#concept 