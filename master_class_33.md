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
  
Training process: backpropragation algorythm, specifically gradient descent algorythms

Keras would be the equivalent to pandas, tensorflow to numpy

**Always use linear activation for linear  problems**

**To avoid overfitting, normalize the train data set**

We cannot use activation relu as it removes the negative values. We have to use elu
  
  activations.elu -> exponential linear units
  
Deep learning automatizes the feature engineering (in ML it's manual)

When models don't work, it's better to reduce the number of neurons and to increase the number of layers

### Regularization techniques

* **Dropout**

On every iteration random neurons are turned off, so smaller models get trained, and later they are put together
