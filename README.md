# mnist-fully-connected-nn
This project was done for the Machine Learning course of the University of Genoa. It is coded in Python and I used Anaconda with JupyterLab.

## How to use it
In order to run the program you need install Anaconda from [https://www.anaconda.com/download/](https://www.anaconda.com/download/) and use JupyterLab or Jupyter Notebook.

## Download the dataset
You have to download the dataset from [http://yann.lecun.com/exdb/mnist/](http://yann.lecun.com/exdb/mnist/):
```
  train-images-idx3-ubyte.gz:  training set images (9912422 bytes) 
  train-labels-idx1-ubyte.gz:  training set labels (28881 bytes) 
  t10k-images-idx3-ubyte.gz:   test set images (1648877 bytes) 
  t10k-labels-idx1-ubyte.gz:   test set labels (4542 bytes) 
```
and put it in a folder called `input` inside of your working directory.

## Code explanation
The code is basically divided in 3 part:
1.	Take the data and divide the dataset into train and validation
2.	Train the network on data
3.	Analyze the prediction on test with confusion matrix and show examples of failure

In the first part I load the data into big matrixes and then I show some numbers from the training set to understand what they look like. At the end I split the dataset in train and validation set.

In the second part I build the class TwoLayerNet. This class implements the two layers neural network with one hidden layer. Here are the class specification:
1. Initialize the weight with small random numbers and the bias with a matrix of zeros. 
2. The Train function runs over a mini-batch of size batch-size (1000) and try to train the model to find the best value of weight and bias using stochastic gradient descent to update and backpropagation to compute the gradients of the functions. 
3. The Loss function is called from the Train function to compute the cross-entropy loss with L2 regularization and to compute the gradients. 4. The Predict function compute the score of each image in the dataset with the current values of weight and bias and then take the max. 
5. Relu and softmax function compute the score of the images for each label.

In the third part I build a Confusion matrix to visualize which numbers I fail more and then I show 3 example of mismatch in order to understand if also human perception can be wrong
