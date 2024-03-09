<mark style="background: #FFF3A3A6;">Hyperparameters are variables that determine the structure and training of a neural network. They are set before training and include variables related to network structure, such as the number of hidden layers and units, and variables related to the training algorithm, such as learning rate and batch size.</mark> Hyperparameters can be tuned to improve a neural network's accuracy and efficiency, and methods for tuning include manual search, grid search, and random search. The number of hidden units is an important hyperparameter that should be between the size of the input layer and the size of the output layer. Hyperparameters are different from model parameters, which are configuration variables that a model learns on its own.

Some common hyperparameters in neural networks include:

1. **Learning rate**: The speed at which the network adjusts its weights during training.
2. **Epochs**: The number of times the entire training dataset is passed through the network during training.
3. **Mini-batch size**: The number of samples used for updating the network's weights in each iteration.
4. **Momentum**: A technique to help the network avoid getting stuck in local minima by maintaining the direction of the gradient.
5. **Regularization**: Methods to prevent overfitting, such as L1 and L2 regularization, dropout, and weight decay.
6. **Number of hidden layers**: The number of layers between the input and output layers.
7. **Number of hidden units per layer**: The number of neurons in each layer.
8. **Activation functions**: Functions that introduce nonlinearity to the network, such as ReLU, Sigmoid, and Tanh.
9. **Loss function**: The function that measures the performance of the network.
10. **Optimizer**: The algorithm used to update the network's weights, such as SGD, Adam, and RMSprop.
11. **Dropout**: A regularization technique that randomly sets a fraction of neurons to zero during training to prevent overfitting.
12. **Weight initialization**: The method used to initialize the weights of the network.
13. **Network architecture**: The structure of the network, including the number of layers and the connections between them.

These hyperparameters can be tuned to improve the performance and efficiency of neural networks.
