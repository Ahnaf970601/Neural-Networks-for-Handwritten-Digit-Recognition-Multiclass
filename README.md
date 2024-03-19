# Neural-Networks-for-Handwritten-Digit-Recognition-Multiclass


Here I used a neural network to recognize the hand written digits 0–9.

First I will talk about ReLU activations:-

ReLU, or Rectangular Linear Unit, is a popular activation function used in neural networks, particularly in deep learning models. The function is defined as:

ReLU(�)=max⁡(0,�)ReLU(x)=max(0,x)

This means that for any input value �x, the ReLU function outputs 0 if �x is less than or equal to 0, and it outputs �x itself if �x is greater than 0. The simplicity of this function makes it computationally efficient and helps in reducing the training time of deep neural networks.

ReLU is widely used because it introduces non-linearity into the model without affecting the receptive fields of convolution layers. This non-linearity is crucial for learning complex patterns in data. Another advantage of ReLU is that it helps mitigate the vanishing gradient problem, which is a common issue in training deep neural networks with sigmoid or tanh activation functions. The vanishing gradient problem occurs when gradients are too small for effective learning, but since ReLU has a gradient of 1 for all positive inputs, it allows for more effective backpropagation of errors through the network.

Common Activation Functions.
Moving on now I will code the Softmax Funtion:-

The softmax function, also known as the normalized exponential function, is a logistic function that turns a vector of raw scores, often called logits in the context of neural networks, into probabilities by taking the exponentials of each input value and then normalizing these values by dividing by the sum of all the exponentials. This process ensures that the output values are in the range (0, 1) and sum up to 1, making them interpretable as probabilities.

Mathematically, the softmax function for a vector �z of raw class scores from the final layer of a neural network can be defined for each element ��zi​ of �z as follows:

softmax(��)=���∑����softmax(zi​)=∑j​ezj​ezi​​

where:

�e is the base of the natural logarithm,
��zi​ is the score for class �i and
the denominator is the sum of the exponentials of all the raw class scores in the vector �z.
The softmax function is widely used in the output layer of a neural network model for multi-class classification problems. It’s especially common in models where the classes are mutually exclusive, and the output needs to represent a probability distribution across a fixed list of classes. By converting logits to probabilities, the softmax function provides a meaningful output that can be compared against the target distribution in the training data, allowing the model to be trained via a loss function like cross-entropy.

One key advantage of the softmax function is its ability to handle inputs that are on very different scales and normalize them in a way that makes them directly comparable, which is particularly useful for classification tasks where the goal is to determine the most likely class out of several possibilities.





Finally now I will implement the Softmax placement:-

The placement of the softmax function within a neural network model is typically at the output layer for tasks involving classification, especially when the classes are mutually exclusive. This strategic placement is crucial because the softmax function converts the logits — raw predictions from the neural network — into probabilities. By doing so, it provides a clear, interpretable output that represents the likelihood of each class being the correct classification for a given input.


To conclude this is my summary and implementation of Neural Networks for Handwritten-Digit Recognition Multiclass.
