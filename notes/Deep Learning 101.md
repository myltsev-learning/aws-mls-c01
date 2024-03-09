---
cssclasses:
  - cornell-note
---

Deep Learning 101

Basically, we are just trying to mimic our brains structure.

<aside>Neuron</aside>

Neuron is a small cell that "fires" signals to the neurons it's connected to when enough of its input signals are activated.

Very simple at the individual neuron level, but layers of neurons connected in this way can yield learning behavior. 

<aside>Cortical column</aside>

Neurons in the cortex seem to be arranged into many stacks or "columns" that process information in parallel. Small columns of around 100 neurons are organized into larger columns. There are 100 million mini-columns in the cortex.

> While GPUs share some similarities with the parallel processing nature of the cortex, the comparison is not entirely accurate. GPUs are designed for efficient graphics processing, and their architecture differs significantly from the biological structure of the brain.

While GPUs can accelerate deep learning computations due to their parallel processing capabilities, not all GPUs used for video games are equally suitable for machine learning tasks. Specific features and optimizations are crucial for efficient deep learning training.

<aside>Artificial Neural Network</aside>

We have translated all we have about our brains into artificial neural networks.

<aside>Arificial Neuron</aside>

Still works on the same basis as a biological one.

They are connected, they have activation function (or signal). They are layered.

![[Deep Learning 101 (1)]]

<aside>Weight</aside>

During the learning ANN configure weight of connections between neurons to get the right answers at the top.

The job of ANN is to learn the appropriate weights and biases.

<aside>Deep Learning</aside>

It's called deep learning because there are more than one hidden layers of neurons.

<aside>Tensorflow, Keras</aside>

Tensorflow and Keras - frameworks we use to train ANNs. It can use GPU for papalized computation.

<aside>Feedforward NN</aside>

Feedforward Neural Network - we just have a bunch of layers on top of each other, we feed features at the bottom and get the prediction at the top.

<aside>Convolutional (CNN)</aside>

Convolutional Neural Network (commonly used for image classification). Convolution -  involves sliding a small matrix (called a filter or kernel) over a larger matrix (like an image) and performing element-wise multiplication and summation. This helps identify specific features within the data.

**CNNs and Convolution:** In CNNs, these filters are used to scan images, extracting essential features like edges, lines, and shapes. By applying convolution repeatedly with different filters, the network progressively learns to recognize complex patterns and ultimately classify or understand the image content.

<aside>Recurrent NN (RNN)</aside>

RNN is useful for dealing with sequences.

1. **Recurring Connections:** Unlike traditional feedforward neural networks where information flows in one direction, RNNs have connections that loop back to themselves. This allows the network to **"remember" information** from previous inputs and incorporate it into processing the current input.
3. **Sequential Processing:** RNNs are specifically designed to handle **sequential data** like text, speech, or time series data. They process each element in the sequence one after another, **taking into account the context** of previous elements to make predictions about the current element.
5. **Maintaining State:** The recurrent connections essentially create a **"memory"** within the network, allowing it to maintain an internal state that reflects the processing history. This state is then used to influence the processing of subsequent elements in the sequence.

<aside>Activation function and why we need non-linear activation functions?</aside>
It's a function that defines the output of a neuron given its input signals.

1. **Linear activation function**, for example, 
		![[Deep Learning 101 (2)]]
		It doesn't really do anything, it's just an example. Function in math match input and output using some rule.
1. **Binary step function** - Next almost meaningless example:
		![[Deep Learning 101 (3)]]
		It's just on or off. Can't handle multiple classification. Doesn't work well with calculus.

That's why we need **non-linear activation functions**

Because they can:
1. Create a complex mapping between inputs and outputs
2. Allow backpropagation
3. Allow for multiple layer (linear degenerate to a single layer, because each layer gives the same result)

Backpropagation is an algorithm that calculates<mark style="background: #FF5582A6;"> the gradients of the loss function </mark>with respect to the network's weights, allowing them to be adjusted in the right direction during training.

<aside>Sigmoid/Logistic/TanH</aside>

![[Deep Learning 101 (4)]]
Smooth function, scales everything from 0-1 or -1 to 1. 
But computationally expensive.

<aside>Rectified Linear Unit (ReLU)</aside>
Very popular choice, easy & fast to compute (because it's linear), but it degenerates to linear function when inputs are negative.

![[Deep Learning 101 (5)]]

The solution to the "Dying ReLU" issue is to not go flat when input is negative

<aside>Leaky ReLU</aside>
This function called Leaky ReLU, it introduces negative slope below 0:

![[Leaky ReLU]]

<aside>Parametric PReLU</aside>
It's a ReLU, but slope in the negative part is learned via backpropagation

![[PReLU]]

<aside>Other ReLU</aside>

- Exponential ReLU (exponentinal for inputs below 0)
- Swish (something from Google)
- Maxout (it's just outputs the max of the inputs)

<aside>Softmax</aside>

It's an activation function as well (often used as a final layer before output). Basically converts outputs to probabilities of each classification

<aside>Use cases</aside>

1. For multiple classification use softmax on the output layer
2. RNN's do well with TanH
3. For everything else:
		1. Start with ReLU
		2. If you need do better -> Leaky ReLU
		3. Last resort: PreLU, Maxout
		4. Swish for really deep networks (40+ layers)

---

<summary>Write a concise summary here</summary>

Deep Learning is an attempt to mimic how our brain learns. We have neurons - basically just activation functions. Those neurons connected together and organized into layers and network in broader sense. We send signal to the network through the input layer, neurons should adjust weights of the connections so that we can get expected result from the output layer. There are few types of activation functions.  While linear functions are computationally efficient, they lack the expressiveness needed for complex learning tasks. Non-linear activation functions are essential for deep learning models to capture intricate relationships in the data. Though linear functions are useless, most popular ones are ReLU (Rectified Linear Unit). Sigmoid and softmax can be used for classification problems.