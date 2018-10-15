# Fastai DL1 - Lesson 1 Notes
 
## Practical gotchas
* Train the model for as many epochs as the accuracy of the **validation** set keeps improving. 
  * if the error of the test is getting lower faster than the validation it it overfitting

* On time-series data, use the newer data for the validation set (http://www.fast.ai/2017/11/13/validation-sets/)

 
## Theory

* Pusue for:
    * Infinitely flexible function: **neural network**
      * Simple linear functions + simple non-linear functions
    * All-purpose parameter fitting: **gradient descent**
      * change parameters and apply a **loss function** to fi8nd the minimum error
    * Fast and scallable
      * Gpus
      * _Deep learning_: neural network + **hidden layers**
        * hidden layers make scalability possible because provides linear scaling, otherwise increasing the number of parameters would exponentially increase training time
* How Convolutional Neural Net works
  * Convolution is not matrix multiplication
  * The linear part of a convolutional layer is the kernel/convolution - a matrix that will _multiply_ parts of the data _sequencially_
  * The non-linear part creates complex shapes
    * Some non linear functions:
      * ** ReLu ** (Rectified Linear Function): `y = max(0, x)`
        * what is negative becames 0, positives passes as they are.
        * ![ReLu Function](https://www.zerotosingularity.com/img/fast-ai-part-1-lesson-1-annotated-notes/relu.png "ReLu Function") 
      * ** Sigmoid **: Relu(x) = max(0, x)
          * big positives became 1, big negatives became 0
	    * 0 corresponds to 0.5
        * small negatives are distributed between 0 and 0.5 and small positives arre distributed between 0.5 and 1
        * ![Sigmoid Function](https://www.zerotosingularity.com/img/fast-ai-part-1-lesson-1-annotated-notes/sigmoid.png)

## Concepts

### Transfer learning

Use of pretrained models

### Reinforcement Learning

Machine learns from its own state and the surrounding enviroment

### Convolutional Neural Network

Processes data that could be represented in a _grid_. It could be a 1D grid (time series).

