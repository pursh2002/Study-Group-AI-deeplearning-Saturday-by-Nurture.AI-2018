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
# CNN 

http://cs231n.stanford.edu/slides/2017/cs231n_2017_lecture5.pdf

# Naive Approach to Build Images Classifier
https://machinelearningmastery.com/naive-bayes-classifier-scratch-python/
https://en.wikipedia.org/wiki/Naive_Bayes_classifier
https://www.analyticsvidhya.com/blog/2017/09/naive-bayes-explained/
https://web.stanford.edu/~jurafsky/slp3/6.pdf
http://scikit-learn.org/stable/modules/naive_bayes.html
http://www.cs.cmu.edu/afs/andrew/course/15/381-f08/www/lectures/Classify.pdf
http://sebastianraschka.com/Articles/2014_naive_bayes_1.html


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

# batch (re-)normalization
tries to get the mean and median each dimension 
https://medium.com/luminovo/a-refresher-on-batch-re-normalization-5e0a1e902960

# Back Propagation

http://neuralnetworksanddeeplearning.com/chap2.html
http://cs231n.github.io/optimization-2/
http://cs231n.stanford.edu/slides/2017/cs231n_2017_lecture4.pdf


# Activation function  
# Hyperparameter Optimization

In biologically inspired neural networks, the activation function is usually an abstraction representing the rate of action potential firing in the cell

http://cs231n.stanford.edu/slides/2017/cs231n_2017_lecture6.pdf
https://en.wikipedia.org/wiki/Activation_function

