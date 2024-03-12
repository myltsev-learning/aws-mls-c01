## The Idea

Undersampling aims to achieve balance by <mark style="background: #FFF3A3A6;">reducing the number of examples in the majority </mark>[[concepts/machine learning/Classes|class]] ("Will Not Churn"). This is often done by randomly removing samples from the majority class until it's closer in size to the minority class.
    
## Pros
    
- **Fast and easy:** Similar to [[concepts/machine learning/Oversampling]], undersampling is relatively simple to execute with a few lines of code.
- **Can reduce overfitting:** By decreasing the size of the majority class, you can reduce the chance of your model becoming too specialized to the patterns of the larger class, which can lead to overfitting. Undersampling forces the model to focus on learning the key features that differentiate the classes from a more limited set of majority class examples.

## Cons

- **Loss of Potentially Useful Information:** The main downside of undersampling is that we discard potentially useful data points from the majority class. This can decrease the overall dataset size and limit the model's ability to learn subtle patterns in the majority class. Undersampling can also introduce bias if the removed data is not representative of the entire majority class. For instance, if we remove only a specific type of "not churn" user from the dataset, the model might not generalize well to unseen data with a different distribution of "not churn" users.