A company is observing low accuracy while training on the default built-in image classification algorithm in Amazon SageMaker. The Data Science team wants to use an Inception neural network architecture instead of a ResNet architecture.  
Which of the following will accomplish this? (Choose two.)  

A. Customize the built-in image classification algorithm to use Inception and use this for model training.
B. Create a support case with the SageMaker team to change the default image classification algorithm to Inception.
C. Bundle a Docker container with TensorFlow Estimator loaded with an Inception network and use this for model training.
D. Use custom code in Amazon SageMaker with TensorFlow Estimator to load the model with an Inception network, and use this for model training.
E. Download and apt-get install the inception network code into an Amazon EC2 instance and use this instance as a Jupyter notebook in Amazon SageMaker.

My answer: A, D

---
## Correct Choices

You have correctly identified the following options as the right choices:

**D. Use custom code in Amazon SageMaker with TensorFlow Estimator to load the model with an Inception network, and use this for model training.**

This option allows you to use the TensorFlow Estimator in your custom code to load and train an Inception network model within Amazon SageMaker.

## Incorrect Choices

However, your choice of **A. Customize the built-in image classification algorithm to use Inception and use this for model training** is incorrect.

Amazon SageMaker provides built-in algorithms for various tasks, including image classification. These built-in algorithms are pre-configured and cannot be customized to use different architectures like Inception. The built-in algorithms are designed to be used as-is, without modifications.

## Explanation

To use an Inception neural network architecture instead of the default ResNet architecture for image classification in Amazon SageMaker, you need to bring your own custom code and model. This can be achieved by using the TensorFlow Estimator or any other deep learning framework supported by SageMaker.

**The correct options are C and D**, which involve bundling a Docker container with TensorFlow Estimator loaded with an Inception network or using custom code in Amazon SageMaker with TensorFlow Estimator to load the Inception network model.

#Claude3-sonnet