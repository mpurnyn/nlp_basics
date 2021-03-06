# Introduction to Tensorflow

## Defining arrays in numpy
- define an array, but make sure to define the type of data in the array as well
    - x = np.array([-1.0,  0.0, 1.0, 2.0, 3.0, 4.0], dtype=float)

## Important Terms
**Tensorflow**
- a library for Machine Learning
**Keras**
- an api in tensorflow
**Neural Networks**
**Layers**
- Dense(units=1, input_shape=[1])
    - the simplest possible network with 1 neuron
**loss functions**
- the function based on next data to see how good a guess is.
- **optimizers**
    - a function that calculates the next guess to try and be better than the last
- **convergence**
    - when the guess gets better and better and the guess accuracy approaches 100%
**Model.fit()**
- trys to fit the model to the data
**Model.predict()**
- produces a guess using the model based on an input 

**stocastic gradient descent**
**mean squared error**