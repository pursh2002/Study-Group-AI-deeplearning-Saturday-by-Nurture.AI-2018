[http://setosa.io/ev/image-kernels/
[https://en.wikipedia.org/wiki/Convolutional_neural_network

in cnn is always a matrix 3*3, multiply every element of the matrix and add them together to get the convolution at one point

[http://forums.fast.ai/t/lesson-3-otavios-viz-not-officially-available/7890

digit word lens , when u focus a camera on any forigin langage on it 
recognise digits e.g letters A which is  grid of numbers
first take out convolution filters assuming already learnt , black rep -ve and white rep +ve in a 3*# matrix -ve -1 -1 0 +ve 1 2
1 , multiplying by 3*3 matrix product which shows red the -ve and green the +ve --- i.e the result of first kernal 

2nd kernal scan it through 3*3 part of the matrix to get red or green asssuming two filters 

next step add a nonlineraity relu to throw away the negeatives 

layer 4 max pool replace by 2 *2 part of grid replace by maximum same thing but half the size 

again repeat the same process 

input ---layer + - -------= relu----maxpool ---repeat = and compare it with a templet A,B,C,C,D and see which closely matches 

multiply by 4 * 8 matrix and add and coverted to giv perc prob

https://github.com/fastai/fastai/tree/master/courses/dl1/excel

single lable --- softmax

multilabel --sigmoid
