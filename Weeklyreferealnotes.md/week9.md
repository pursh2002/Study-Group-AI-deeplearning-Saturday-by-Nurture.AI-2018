Agenda for Upcoming Meetup :  (Might Change)

CS231n : Convolutional Neural Networks for Visual Recognition: Revisited :

1 ) Introduction to Vision and Common Computer Vision Problems. :
2 ) Naive Approach to Build Images Classifier:
3 ) Loss Functions and Optimization : 
4 ) Introduction to Neural Networks : Back Propagation : 
5 ) Convolutional Neural Networks : 
6 ) Training Neural Networks : Activation functions, initialization, dropout, batch normalization

Hands on :

2 Layer Neural Network using Numpy : Without any Libraries and with Libraries like Keras, Tensorflow and Pytorch
(1 or 2 of the frameworks)
# Naive Approach to Build Images Classifier



# Softmax normalization
* http://cs231n.github.io/linear-classify/

Sigmoidal or Softmax normalization is a way of reducing the influence of extreme values or outliers in the data without removing them from the dataset. It is useful given outlier data, which we wish to include in the dataset while still preserving the significance of data within a standard deviation of the mean. The data are nonlinearly transformed using one of the sigmoidal functions.

The logistic sigmoid function:

1/1+e

Limits the range of the normalized data to values between 0 and 1

 Soft max vs The hyperbolic tangent function:
tanh, limits the range of the normalized data to values between −1 and 1.
softmax Limits the range of the normalized data to values between 0 and 1

# loss function or cost function
https://web.stanford.edu/class/cs221/lectures/learning1.pdf

In mathematical optimization, statistics, econometrics, decision theory, machine learning and computational neuroscience, a loss function or cost function is a function that maps an event or values of one or more variables onto a real number intuitively representing some "cost" associated with the event.

An optimization problem seeks to minimize a loss function.

In statistics, typically a loss function is used for parameter estimation, and the event in question is some function of the difference between estimated and true values for an instance of data. 
