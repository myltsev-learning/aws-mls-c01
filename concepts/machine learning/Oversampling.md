## Idea

Oversampling involves replicating examples from the minority [[concepts/machine learning/Classes|class]] (those who churned in our example) to increase its representation in the dataset. This helps balance the classes and forces the model to pay more attention to the minority class.
    
## Pros
    
- Simple to implement: Oversampling can be done with a few lines of code in most programming languages.
- Improved minority class identification: By increasing the representation of the minority class, the model is exposed to more examples and has a better chance of learning the patterns that differentiate churners from non-churners.

## Cons
    
- Overfitting: A potential downside of oversampling is that it can lead to overfitting, especially if we simply duplicate examples without any variation. Overfitting happens when the model memorizes the specific examples in the training data and performs poorly on unseen data. To mitigate this risk, we can use techniques like random oversampling with replacement, where we randomly select examples from the minority class to replicate, or SMOTE (Synthetic Minority Oversampling Technique), which creates new synthetic data points for the minority class. We'll discuss SMOTE in a later block.

#concept 