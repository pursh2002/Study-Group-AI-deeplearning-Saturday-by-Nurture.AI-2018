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


Minute of the Meetup 8: Feb 24 2018

CS231 : CNN for Vision
 
Lesson 1 :
History of Computer Vision :
Traditional CV Methods:How it Evolved?
Computer Vision : Evolution
Modern Computer Vision Tasks : Captioning, Segmentation , Completion, Generation ,SuperResolution, Style Transfer.

Lesson 2 :
Classification Pipeline
Challenges in Computer Vision:
Nearest Neighbor Classifier : Demo at Stanford Page : http://vision.stanford.edu/teaching/cs231n-demos/knn/
BAD: K = 1 always works and perfectly fits on training data (No Generalization )
KNN Disadvantages: Slow and Distance metrics not reliable
Curse of Dimensionality : As the number of dimensions increases, ML Algorithms find it difficult to approximate complex functions as data becomes sparse.
Linear Classification :
Interpretation of Linear Classifier
Short comings of Linear Classifier

Lesson 3 :
Revisit : Linear Classifier :
Loss Function: Quantitatively determine how Bad the Weights ?
How Loss changes : W small : Loss min : no of Classes-1.
Regularization : Extra term added to loss to pick simple Weights(Smaller and Better)
Hinge Loss
Softmax: Cross Entropy

Lesson 4:
Back Prop : Recursively use Chain Rule to compute gradient wrt to all variable
How is Backprop is computed?
Numeric Gradient vs Analytic gradient
Code Implementation of Backprop (Will be Dealt in Hands on Session)
Lesson 5:
History of Neural Networks :
Perceptron: Rosenblatt
CNN : Current State and Application
How CNN's Work : ?
Activation Map :
Kernel Size :
No of Kernels:
Stride :
Padding :
To preserve Size : (Kernel Size -1)/2
Output Size : (Input Image Size-Kernel Size)/Stride+1
Pooling : Pooling Vs Stride

Lesson 6:
Setting up the model: initialization regularization
Why 0 Centered is desired in Activation Function : Gradient is going to be all positive or all negative
Bad/dead Relu : Caused due to bad initialization : Learning rate too high
Normalizing data : all feature same range : all feature contribute equally
Images we don't normalize much as in other ML

Note : Please Go through the course notes page for detailed notes: Link : http://cs231n.github.io/ :

Hands on Session :

Documentation :
Keras: https://keras.io/getting-started/sequential-model-guide/
Tensorflow: https://www.tensorflow.org/api_docs/python/
Pytorch: http://pytorch.org/docs/0.3.1/

Activity : https://goo.gl/9enZdN ( Please Sacve your own local Copy and Work)

Solution : https://goo.gl/sMBEHv (Refer Only when Needed)

