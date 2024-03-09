A **feedforward network** is a type of [[concepts/neural networks/Deep Learning|Deep Learning]] architecture where information flows in **one direction**, from the **input layer** through **hidden layers** to the **output layer**, without any loops or cycles. Here's a breakdown of its key characteristics:

**Structure:**

- **Layers:** A feedforward network consists of multiple layers of interconnected neurons. The first layer receives the input data, and subsequent layers process the information progressively through the network.
- **Information flow:** Information flows **unidirectionally** from the input layer to the output layer. Each neuron in a layer receives input from the previous layer, applies an activation function, and sends its output to the next layer.
- **No cycles:** Unlike recurrent neural networks, feedforward networks do not have any recurrent connections or loops within the network.

**Advantages:**

- **Simpler architecture:** Feedforward networks are relatively simpler to design and implement compared to recurrent networks.
- **Efficient training:** They can be efficiently trained using algorithms like gradient descent due to the straightforward information flow.
- **Wide range of applications:** Feedforward networks are versatile and can be applied to various tasks, including image recognition, natural language processing, and regression problems.

**Examples:**

- **Multi-layer perceptron (MLP):** A basic type of feedforward network commonly used for classification and regression tasks.
- **Convolutional neural networks (CNNs):** A specialized type of feedforward network designed for image recognition and processing.

**In essence, feedforward networks are fundamental building blocks in deep learning, offering a straightforward architecture for various tasks where information processing can be modeled as a one-directional flow.**

#entity 
