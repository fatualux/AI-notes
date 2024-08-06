# Neural Networks

A **neural network** is a **computational model** inspired by the way biological neural networks in the human brain process information.

It is a field that investigates how simple **models of biological brains** can be used to **solve difficult computational tasks** (e.g., predictive modeling tasks).

The goal is not to create realistic models of the brain but instead to develop robust algorithms and data structures that we can use to model difficult problems.

Neural networks learn mapping (any mapping function), to learn best to relate the training datasets to the output variable you want to predict.

The predictive capability of neural networks comes from the **hierarchical** or **multi-layered structure** of the networks.

It consists of interconnected layers of **nodes** (neurons), which work together to recognize patterns and make decisions based on data inputs. Here are the key aspects of neural networks:

### Structure:

[**Neurons**](./neuron.md): Basic units of a neural network, where each neuron receives input, processes it, and passes the output to the next layer.

**Layers**:
- **Input Layer**: The first layer that receives the initial data.
- **Hidden Layers**: Intermediate layers that perform computations and feature transformations. The term "deep" in deep learning refers to networks with many hidden layers.
- **Output Layer**: The final layer that produces the prediction or classification result.

### Connections and Weights:

Each connection between neurons has an associated [weight](./weights.md), which adjusts as the network learns. Neurons apply an activation function to the weighted sum of their inputs to introduce non-linearity and help the network learn complex patterns.

### Activation Functions:

Functions applied to the output of each neuron to introduce non-linear properties to the network. Common activation functions include:

- **Sigmoid**: Squashes input values to a range between 0 and 1.
- **Tanh**: Squashes input values to a range between -1 and 1.
- **ReLU (Rectified Linear Unit)**: Outputs the input if it is positive; otherwise, it outputs zero.
- **Leaky ReLU**: A variant of ReLU that allows a small gradient when the input is negative.

### Training:

- **Forward Propagation**: The process where input data passes through the network layers to generate an output.
- **Loss Function**: A function that measures the difference between the predicted output and the actual target. Common loss functions include Mean Squared Error (MSE) for regression tasks and Cross-Entropy Loss for classification tasks.
- **Backpropagation**: An algorithm used to minimize the loss function by adjusting the weights. It calculates the gradient of the loss with respect to each weight and updates the weights using an optimization algorithm (e.g., Gradient Descent).

### Types of Neural Networks:

- **Feedforward Neural Networks (FNNs)**: The simplest type where connections do not form cycles. Used for tasks like image and speech recognition.
- **Convolutional Neural Networks (CNNs)**: Designed for processing grid-like data, such as images. They use convolutional layers to detect spatial hierarchies.
- **Recurrent Neural Networks (RNNs)**: Suitable for sequential data, like time series or text. They have connections that form cycles to capture temporal dependencies.
- **Autoencoders**: Used for unsupervised learning, especially for tasks like dimensionality reduction and anomaly detection.
- **Generative Adversarial Networks (GANs)**: Consist of a generator and a discriminator, used for generating new, synthetic data samples.

### Applications:

- **Image and Video Recognition**: Identifying objects, faces, and actions in images and videos.
- **Natural Language Processing**: Text classification, translation, summarization, and generation.
- **Speech Recognition**: Converting spoken language into text.
- **Medical Diagnosis**: Analyzing medical images and data for disease detection.
- **Autonomous Vehicles**: Perception and decision-making in self-driving cars.
