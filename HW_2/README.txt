Fruit_Prediction
Introduction
Construct a 2D convolution and pooling model for predicting fruit images, which should be classified as "Carambula", "Lychee", "Pear".

There are 4 python files: Conv.py, Network.py, fruit_model.py, fruit_predict.py

Requirements: numpy

1. Conv.py:

Consists of some classes which are necessary to build an overall neural network for prediction.

(1) Convolution(kernel_size, channels, out_channels, strides, padding)
CLASS
-- function:
    (a) filter: The function which generates filters for convolution
    (b) __call__(inputs): The forward pass including convolution & padding process

(2) Pooling(size)
CLASS
-- function:
    (a) __call__(inputs, pooling="max"): Pooling methods include "aax" (default) for maxpooling & "average" for average-pooling


(3) net(n_linear, activation_list, batch_size)
CLASS
--function:
    (a) Conv_2d(inputs): Construct several convolution and pooling layers with activation function operations.
    (b) fit(inputs, outputs, x_val, y_val, epochs): Training the model by input training data and validation data through iterations
    (c) eval(X_test, y_test, model): Evaluate the model with testing data

2. Network.py:

Backbone of neural network

3. fruit_model.py

Read and augment images from training data

(1) shuffle(X, Y): Shuffle the datasets by random index

(2) split(X, Y, rate): Splitting data into training data and validation data

4. fruit_predict.py

Read and predict images from testing data by constructed model, and visualized the results.