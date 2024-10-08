# Multi-Layer Perceptron Neural Networks

```mermaid
graph TD
    %% Input Layer
    A1(Input 1) -->|Weight 1| H1
    A2(Input 2) -->|Weight 2| H1
    A3(Input 3) -->|Weight 3| H1
    A1 -->|Weight 4| H2
    A2 -->|Weight 5| H2
    A3 -->|Weight 6| H2
    A1 -->|Weight 7| H3
    A2 -->|Weight 8| H3
    A3 -->|Weight 9| H3

    %% Hidden Layer
    H1 -->|Weight 10| O1
    H1 -->|Weight 11| O2
    H2 -->|Weight 12| O1
    H2 -->|Weight 13| O2
    H3 -->|Weight 14| O1
    H3 -->|Weight 15| O2

    %% Output Layer
    O1(Output 1)
    O2(Output 2)

    %% Styling
    classDef inputLayer fill:#f9f,stroke:#333,stroke-width:2px;
    classDef hiddenLayer fill:#ccf,stroke:#333,stroke-width:2px;
    classDef outputLayer fill:#cfc,stroke:#333,stroke-width:2px;

    class A1,A2,A3 inputLayer;
    class H1,H2,H3 hiddenLayer;
    class O1,O2 outputLayer;
```

## Legend

| **Element**        | **Description**                                                                 |
|--------------------|---------------------------------------------------------------------------------|
| **Input Neurons**  | Neurons in the input layer representing features or data points.                |
| **Hidden Neurons** | Neurons in the hidden layer performing intermediate processing and feature extraction. |
| **Output Neurons** | Neurons in the output layer providing the final predictions or classifications.  |
| **Weights**        | Parameters that adjust the strength of the connections between neurons.         |
| **Activation Functions** | Functions applied to the weighted sum of inputs and bias to introduce non-linearity. |

#### Building Blocks of Neural Networks

1. **Neurons**:
   - **Description**: The fundamental units of a neural network, inspired by biological neurons. Each neuron receives input, processes it, and passes it on to the next layer.
   - **Components**:
     - **Input**: Signals from previous neurons or raw data.
     - **Weights**: Parameters that adjust the strength of the input signals.
     - **Bias**: An additional parameter that shifts the activation function.
     - **Activation Function**: A function applied to the weighted sum of inputs and bias to introduce non-linearity.

2. **Weights**:
   - **Description**: Parameters that are learned during training. They represent the strength of the connections between neurons. Each connection between neurons has an associated weight that adjusts as the network learns.

**Activation Functions**:
- **Purpose**: Activation functions introduce non-linearity into a neural network model, which allows the network to learn and represent complex patterns. Without them, the model would only be able to learn linear relationships, severely limiting its ability to solve complex problems.

- **Common Functions**:
  - **Sigmoid**: 
    - **Formula**: \\( \sigma(x) = \frac{1}{1 + e^{-x}} \\)
    - **Explanation**: The sigmoid function takes any real-valued number and maps it to a value between 0 and 1. 
      - **Key points**: 
        - As the input \\( x \\) becomes large and positive, the output approaches 1.
        - As the input becomes large and negative, the output approaches 0.
        - At \\( x = 0 \\), the output is 0.5.
      - **Use case**: It's often used in the final layer of a neural network for binary classification, where the output represents a probability.

  - **ReLU (Rectified Linear Unit)**:
    - **Formula**: \\( \text{ReLU}(x) = \max(0, x) \\)
    - **Explanation**: The ReLU function outputs the input directly if it's positive; otherwise, it outputs zero. 
      - **Key points**: 
        - For any positive input, ReLU returns that same value.
        - For any negative input or zero, ReLU returns zero.
      - **Use case**: ReLU is very popular because it is simple and helps prevent issues like vanishing gradients, making it effective for deep networks.

  - **Tanh**:
    - **Formula**: \\( \text{tanh}(x) = \frac{e^x - e^{-x}}{e^x + e^{-x}} \\)
    - **Explanation**: The tanh function maps the input to a value between -1 and 1.
      - **Key points**: 
        - Like the sigmoid function, but centered around 0. 
        - For large positive inputs, tanh approaches 1.
        - For large negative inputs, tanh approaches -1.
        - At \\( x = 0 \\), the output is 0.
      - **Use case**: Tanh is often used when you want to ensure that the output of a neuron is centered around zero, which can help in faster convergence during training.

  - **Gelu (Gaussian Error Linear Unit)**:
    - **Formula**: \\( \text{GELU}(x) = x \cdot \sigma(\text{tanh}(x)) \\)
    - **Explanation**: GELU is a more advanced activation function that combines aspects of both ReLU and sigmoid/tanh. 
      - **Key points**:
        - It smoothly blends the behavior of the input, with a probabilistic aspect coming from the sigmoid function.
        - Unlike ReLU, which sharply changes at 0, GELU makes this transition smoother.
        - It can be thought of as scaling the input by a factor that depends on the value of the input itself.
      - **Use case**: GELU is used in some of the latest neural networks, such as transformers, due to its ability to model complex, non-linear behaviors more effectively.

#### Layers in Neural Networks

1. **Input Layer**:
   - **Description**: The first layer that receives the raw input data. Each neuron in this layer represents one feature of the input.

2. **Hidden Layers**:
   - **Description**: Intermediate layers between the input and output layers. These layers perform computations and feature extraction. Each hidden layer consists of multiple neurons.
   - **Types**:
     - **Fully Connected Layer**: Every neuron is connected to all neurons in the previous layer.
     - **Convolutional Layer**: Used in convolutional neural networks (CNNs) to process spatial hierarchies in data.

3. **Output Layer**:
   - **Description**: The final layer that produces the output of the network. The number of neurons in this layer corresponds to the number of classes or values to be predicted.

#### Impact of Noise on Prediction Quality

1. **Definition of Noise**:
   - **Description**: Random or irrelevant information in the data that can distort the learning process of the neural network. Noise can come from various sources, such as measurement errors, data entry mistakes, or irrelevant features.

2. **Effects on Prediction Quality**:
   - **Overfitting**: Noise can cause the model to learn irrelevant patterns specific to the training data, leading to poor generalization to new data.
   - **Reduced Accuracy**: The presence of noise can lower the accuracy of the predictions, as the model may misinterpret noisy data as meaningful.
   - **Increased Variance**: Models trained on noisy data may exhibit high variance, meaning their performance can vary significantly across different datasets.

3. **Mitigation Strategies**:
   - **Data Preprocessing**: Clean and preprocess data to remove or reduce noise before training.
   - **Regularization**: Techniques like L1/L2 regularization can help prevent overfitting by adding a penalty for large weights.
   - **Cross-Validation**: Use cross-validation to assess the model's performance on different subsets of the data, helping to ensure robustness.
   - **Noise Robust Models**: Employ algorithms and architectures that are less sensitive to noise, such as ensemble methods or robust loss functions.

### Conclusion

Multi-Layer Perceptron (MLP) neural networks are powerful tools for learning complex patterns in data. Understanding the building blocks such as neurons, weights, and activation functions, and how they are organized into layers, is crucial for designing and training effective neural networks. Additionally, addressing the impact of noise on prediction quality is essential for developing robust models that perform well on real-world data.
