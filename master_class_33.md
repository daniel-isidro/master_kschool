# Deep Learning
## Juan Arévalo, Cepsa

### Deep learning

W = weight matrix, on every layer it evolves and improves

Lineal transformations are equivalent to vector rotations. To make non-linear transformations, we use activation functions
  
Most used activation function is * rectifier linear unit * or relu
  
Relu returns 0 if input is negative, and returns x if input is positive
  
We decide how many layers have the model, but the weight matrices are selected automatically
  
Every layer decides what parts of its input are relevant or not, to resolve the problem
  
Reinforced learning: At the end of the process we tell the model whether the output was correct or not
  
Neurons are the components of the output y. b and y have the same size
  
Every layer changes the size of the input. A neural network is a series of layers. y is the dense layer

Every layer usually has less neurons than the previous one
  
Training process: backpropragation algorythm, specifically gradient descent algorythms

Keras would be the equivalent to pandas, tensorflow to numpy

**Always use linear activation for linear  problems**

**To avoid overfitting, normalize the train data set**

We cannot use activation relu as it removes the negative values. We have to use elu

An even better activation is selu
  
```
activations.elu -> exponential linear units
```

In the last layer of Neural Networks, usually softmax activation is used to force a normalized output (so the sum of all outputs is 1)

Deep learning automatizes the feature engineering (in ML it's manual)

When models don't work, it's better to reduce the number of neurons and to increase the number of layers

### Regularization techniques

* **Dropout**

On every iteration random neurons are turned off, so smaller models get trained, and later they are put together. This helps reducing the overfitting

Better to use Dropout near the last layers. Also use it after the first layer with highest number of parameters

Dropout rate = 0.3 -> turns off 30 % of neurons

When the error of the validation set is less than the one of the training set, it means that we have used regularization too much

### DL Takeaways

* What matter is to learn **representations**, not DL itself

* DL is well suited for **high dimensionality** problems

* **Outside DL world:**
  * Interventions, actions, etc.
  * Imagination, reasoning, causality, etc.
  
### Optimization

Optimizing the cost function is usually very difficult.

* **Stochastic Gradient Descent**

The word 'stochastic' means a system or a process that is linked with a random probability. Hence, in Stochastic Gradient Descent, a few samples are selected randomly instead of the whole data set for each iteration

In keras, never use pure SGD, all the rest of the optimizers are quicker (RMSProp, Adam, etc.)

* **Learning rate**

Default is 0.001, put it higher (e.g. 0.005) to increase the learning speed

* **Batch size**

If batch size is too small, learning is very slow. If it's too big, we are near the dataset size, and it stops being stochastic. **Never use batch size over 1000.**

### Convolutional Neural Networks

Filters are used to look for a pattern in the input

Filters measure the overlapping between the input and the pattern

Most used fiters are 5x5 pixels

In CNNs the layers are groups of filters
