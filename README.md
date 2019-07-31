# CNN-Training_an_MLP_on_MNIST
Convolutional Neural Network -Training an MLP on MNIST
A multilayer perceptron (MLP) is a class of feedforward artificial neural network. A MLP consists of at least three layers of nodes: an input layer, a hidden layer and an output layer. Except for the input nodes, each node is a neuron that uses a nonlinear activation function. MLP utilizes a supervised learning technique called  backpropagation for training. Its multiple layers and non-linear activation distinguish MLP from a linear perceptron. It can distinguish data that is not linearly separable.

## About the project : 
Let's begin by investigating how deep learning can be used to recognize handwritten numerical digits.
We'll design in image classification algorithm that takes pictures of handwritten numbers and identifies the numbers represented in the images.
To do this, we'll use the MNIST Database which Each depicts one of the numbers zero through nine.
his database is perhaps one of the most famous databases in the field of machine learning.
After importing the necessary python module,it's only one line of code to get our train and test images along with their corresponding labels.
When we look at the first six training images,we immediately notice that some digits are more legible than others.
It will need to attain some level of understanding for what makes a hand-drawn one look like a one,and how images of ones differ from images of twos or threes.

These discovered patterns can then be used to decipher the digits in images that it hasn't seen before.
Any grayscale image is interpreted by the computer as a matrix with one entry for each image pixel.Each image in the MNIST Database is 28 pixels high and 28 pixels wide,and so understood by the computer as a 28 by 28 matrix.
White pixels are encoded as 255.
Black pixels are encoded as 0.
And gray pixels appear in the matrix as an integer somewhere in between.

As a quick preprocessing step,we'll rescale each image to instead have values in the range from 0 to 1.To do this, we'll divide every pixel in every image by 255.
Before supplying the data to a deep network in Keras,we'll also need to preprocess the labels.
Currently, each image has a label that's integer valued.We'll need to convert this to a one-hot encoding.
Each label will be transformed to a vector with mostly zeros.If the label was originally a 7, we'll put a 1 in the seventh entry of the vector.
So in order to use an MLP with images,which you've seen are encoded as matrices,we have to first convert all of our matrices to vectors.We'll illustrate this conversion process on the toy example depicted here. In the case of a 4 by 4 image we can construct a vector with 16 entries. Where the first four entries of our vector correspond to the first row of our old matrix. The second four entries correspond to the second row and so on.

In the case of our 28 by 28 matrices, will flatten them to a vector with 784 entries.
After encoding our images as vectors, they can be fed into the input layer of an MLP.











 


