In order to cater to a diverse audience, there will be 2 sessions every Saturday – you can attend both, 
one of them or none, it’s totally up to you! If you don’t want to attend the sessions, throughout the 
day there will be open hacking on creating open-source code implementations of the top research paper 
pre-prints that week. Or use that time to catch-up on lectures and readings (Afternoon sessions will be more
focused towards demo and hands on Coding !) while discussing with peers.
[http://forums.fast.ai/t/wiki-lesson-2/9399

# Session 1: Video Lecture Synopsis and Discussion
## 1) Practical Deep Learning (Fast.ai) : Lecture 2
Video : [https://youtu.be/JNxcznsrRb8
Wiki : [http://forums.fast.ai/t/wiki-lesson-2/9399

## 2) CS231n : (Mandatory for guys interested in Computer Vision)

Lect 1 : [https://www.youtube.com/watch?v=vT1JzLTH4G4 (Recommended for Beginners)
Lect 2 : [https://www.youtube.com/watch?v=OoUX-nOEjG0
Lect 3 : [https://www.youtube.com/watch?v=h7iBpEHGVNc

## 3) CS224d : (Mandatory for guys interested in NLP)
[https://github.com/pursh2002/CNN-for-Sentence-Classification-in-Keras
Lect 1 : [https://www.youtube.com/watch?v=OQQ-W_63UgQ ( Recommended for Beginners)
Lect 2 : [https://www.youtube.com/watch?v=ERibwqs9p38

## 4) Reinforcement Learning: Will be discussed based on the response from the upcoming meetup. For ease of the facilitator 
in-charge’s preparation for any particular week, participants are encouraged to watch the lectures beforehand and post 
questions on specific parts of the lectures using the Nurture.ai platform’s highlight-commenting function.

# Assignments/Tasks

Task 1 : Multi-Class Classification : (Trashnet)

Link : [https://github.com/garythung/trashnet
Dataset Link: [https://drive.google.com/drive/folders/0B3P9oO5A3RvSUW9qTG11Ul83TEE

Use the Dataset-Resized.zip for the dataset.
Please Compare your performance with the authors performance. Write a Brief description about how you 
did it ? Task 2 : Theory Questions


1) Similarity and Difference Between Domain Adaptation and Transfer Learning?
2) What is Bias? How does it affect the performance of the model?
3) How does lr_find() work ? (If Interested)


cycle multiplyer ------

Process 

input data 
data agumentation 
find learning rate 
pre compute = true 
train last layer 

computer vision is amalgation of many domain,it works on statistical computation 

CNN --- segmentation task 

## Image classification pipeline 

challanges: view point varation , background variation 

collect a dataset of images and label


nearest neighbour classifier - distance metric to compare distance 

value of k
distance metric
l2 eculadian distance 

setting hyperparameters (not recommended)
choose hyperparameters
split train and test choose hypermeters 
split data into train val and test  choose parameter on value and evaluate on test 
cross validation  (does not work always) not good for timeseries 

k-nearest on image never used ---curse of dimensanality 

In a normal 

### parameteric approach 

image ----f(x,w)----10 numbers giving class scores 

linear classifiers 

interpreating a linear classifier -- hard 


## NLP 

use WordNET

word2vec 

king - man + women = queen 

huge splash in NLP world 
word2vec : learn word vector vm from its 

there are two vectors for every words 
input and output 

NLP usage -- chatbots(neural network RNN), google search,sentiment analysis(bag of words), question and answering(regular expression)

words are made of morphemes 
parsing for sentence structure 

earlier alg on bag of words  are discarded 

how do we reperesent the meaning of words 

how do we have usable meaning in a computer 

use wordnet a resource containing lists of synonym sets and hypernyms(its arelationship)

problem with wordnet ---

# feature engeneering for image ....
why do we do normalization ?

Whats the best activation function?
transformation with normalization 
resizing 
tunning the hyperparameter--- [http://neupy.com/2016/12/17/hyperparameter_optimization_for_neural_networks.html
How to choose hyperparameter?
  grid based approach
  split the data into train and test 80 to 20
  
  where do we use crossvalidation 
  small datasets

how do u reduce overfitting 
regularization --- add penalty to the weight 

what u do when there is underfitting?---- [https://www.geeksforgeeks.org/underfitting-and-overfitting-in-machine-learning/

add more data....

* mila labs --- pytorch ---
 https://github.com/mila-udem/welcome_tutorials/tree/master/pytorch
 https://github.com/mila-udem/welcome_tutorials/blob/master/pytorch/1.%20The%20Torch%20Tensor%20Library%20and%20Basic%20Operations.ipynb
 
 * hyperparameter-optimization----[https://ai6forums.nurture.ai/t/best-practices-for-hyperparameter-optimization/42

# summary 

1)Lesson 1 Recap: Major Takeaways : 
    Setting Up Environment: Paperspace, Crestle
    Gradient Descent - Analogy Using U Curve
    Deep Visualization : Interpretation of Layers 

2)Lesson 2 : 

    Data Augmentation :  random Brightness, Rotation, Zoom,  Contrast
    Pre-Compute Vs Pre-Training Differences
    Learning Rate Annealing Decreasing rate  as time progress (Drop by 10 times) 
    Cosine Positive Half is used to Decrease the LR (Instead of Step)
    Differential Learning Rates: Layer Groups 3 Groups : [Earlier middle Last]
    epochs: no of iterations 
    Cycle_len= no of cycles or restarts (Finding the perfect spot)
    cycle_mult= rate at which lr is decreased (Duration will increase) 
    learn.sched.plot_lr()
    Recommended Fit Configuration 
    3 cycles 2 mult
    3 epochs 1 cycle 2 mult 
    Test Time Augmentation : TTA() average of augmented images

    Confusion Matrix : Understating performance 
    Some Dataset come as Train and test Zip with corresponding CSV files 
    use ImageClassiferData.from_csv to load the data  . No Validation Folder is Created Can Pass Suffix(Format of images)
    When Validation Set is small then tuning becomed difficult.
    Increase Image size and use better models if possible 

***Cs231n : ***

Lesson 1 :  Till Slides 39
    History of Computer Vision : 
    Traditional CV Methods:How it Evolved?
    CNN : Evolution 
    Modern Computer Vision Tasks

Lesson 2 :
    Classification Pipeline 
    Challenges in Computer Vision:
    Nearest Neighbor Classifier : Demo at Stanford Page : http://vision.stanford.edu/teaching/cs231n-demos/knn/
    BAD: K = 1 always works and perfectly fits on training data (No Generalization )
    KNN Disadvantages: Slow and Distance metrics not relaible
    Curse of Dimensionality : As the number of dimensions increases, ML Algorithms find it difficult to approximate complex functions as data becomes sparse. 
    Linear Classification :
    Interpretation of Linear Classifier 
    Short comings of Linear Classifier 


***Cs224d:***

1)Lesson 1 : Introduction to NLP :
    NLP Levels : Discourse -- More with Context and Semantic -- Meaning 
    Where Industry is Headed 
    Human Language is Complex (Symbolic Signaling) communicate Continuously using Gesture Sound and Images(written) 
    Because Symbolic as the vocabulary grows large -- data becomes sparse 
    Manually hand Craft Features - Conventional ML
    Deep Learning - Learn Representation (UnSup/Supervised)
    NLP - Challenges ?
    Representation is complex as vocab grows. Ambiguous depends on hearer and situation common sense
    NLP Advances and domains :
    Comparison how it was done before and with DL

2)Lesson2 :

    Meaning of a Word: Defined by what it signifies in real world (What it Denotes)
    Using Taxonomic Resources ..  As new words come in or different kind of usage occurs then many meaning will be missing.
    One Hot Representation : No inherent notion of relationship between words (Orthogonal to each other)
    Distributional Similarity :  Find all occurrence of the words with its surrounding to understand the context (Different from Distributed Representation) 
    Objective is to find out a vector(Preferably Dense)
    Embedding is the vector representation of words. Eg :Word2Vec
    Define a model to predict the center word /surrounding words when the surrounding words/center word are given 
    define loss how close to the context
    Skip Gram : Predict center word when surrounding word is given. Maximize the probability of Center word Loss : Cross entropy loss

Misc Resources : 
    Optimsers an Overview : http://ruder.io/optimizing-gradient-descent/
    Tensorflow Playground : playground.tensorflow.org
    Overfitting and Underfitting: How to Avoid and Deal with them ?
Google Docs
Attendance and Feedback Form - Bangalore Chapter
This form serves to mark your attendance in the qualification for your Certificate of Completion (you have to attend at least 10 out of the 15 AI Saturdays in the cycle in order to qualify), which will allow you to enter the AI Saturdays global alumni network and Slack group with additional perks and advanced AI discussions. Further it will help us get to know more about your expectations and will further facilitate in conducting the sessions so that they are beneficial for all of us. It also helps Show more… (115 kB)
 Sebastian Ruder
An overview of gradient descent optimization algorithms
This blog post looks at variants of gradient descent and the algorithms that are commonly used to optimize them.
Jan 19th, 2016 at 7:50 PM
(edited)
 


Pinned
[11:28] 
***Next Meetup Agenda:*** UPDATED 

1)Fast.ai : Lesson 3 :

    Video: https://youtu.be/9C06ZPF8Uuc

    Forum Wiki :http://forums.fast.ai/t/wiki-lesson-3/9401 

2)cs231n : http://cs231n.stanford.edu/2017/syllabus.html

    Lesson 3:

        Video: https://www.youtube.com/watch?v=h7iBpEHGVNc

        Slides:http://cs231n.stanford.edu/slides/2017/cs231n_2017_lecture3.pdf

    Lesson 4:

        Video: https://www.youtube.com/watch?v=d14TUNcbn1k

        Slides:http://cs231n.stanford.edu/slides/2017/cs231n_2017_lecture4.pdf

    Course Notes : http://cs231n.github.io/
    

3)cs224d: http://cs224d.stanford.edu/syllabus.html

    Lesson 2 :

        Video: https://www.youtube.com/watch?v=ERibwqs9p38

        Slides: http://web.stanford.edu/class/cs224n/lectures/lecture2.pdf

    Lesson 3 :

        Video: https://www.youtube.com/watch?v=ASn7ExxLZws

        Slides: http://cs224d.stanford.edu/lectures/CS224d-Lecture3.pdf

    Course Notes : http://cs224d.stanford.edu/lecture_notes/

Pytorch : Introductions to Pytorch

    Github : https://github.com/mila-udem/welcome_tutorials
    Please get familiarised with First 2 Notebooks. 

***Note :***


1) The Wiki page will contain solution to most of the commonly faced problems. Kindly go through them before you ask any questions.

2) Please watch the videos well in advance and if possible one of the participants can summarize their understandings and findings during the Meetup (Contact me if Interested)

3) Do Sign up in Fast.ai forums (http://forums.fast.ai/) and AI Saturdays Forum (https://ai6forums.nurture.ai/)

4) Please post your questions on AI Saturdays Forum as discussed in General Channel to get faster response.

5) Try to get some ideas/problems that you are interested to work on. Preferably with corresponding dataset.

6)For people who feel there are too many videos. Please watch as many Videos possible. You need not have 100% Understanding of the videos. Please note down the points that you are not clear.

7)Gist of the Videos  will be presented followed by a discussion. Administrative Stuff and other Generic Stuff (Introductions) can be fast forwarded at your ease. Do start with Fast.ai Video and try replicating the notebook without copying the code.  













