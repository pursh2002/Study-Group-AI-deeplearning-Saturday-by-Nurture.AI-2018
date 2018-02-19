Details

Session 1: Practical Deep Learning

Using the free and proven Fast.ai materials, this is perfect for beginners in deep learning and machine learning, with some prior Python programming experience and high school math knowledge – and it’d get you to a stage where you can implement cutting-edge deep learning models, in just 14 weeks! No worries if you have no Python programming experience, feel free to reach out and we’d be happy to advise on what you can use in the weeks leading up to the start date to prepare – you can certainly get up to speed if you work hard in these few weeks, but time is running short so get started now!

Lesson 3 : Video: https://youtu.be/9C06ZPF8Uuc Forum Wiki :http://forums.fast.ai/t/wiki-lesson-3/9401

We will watch the lectures as a group, stop the video for discussion at any point if anyone has a question, and also breakout into small groups for the in-lecture exercises – removing any obstacles along the way, making sure that you can progress through the course confidently if you stick with us – that’s our commitment to you for your time investment!

Session 2: Convolutional Neural Networks for Visual Recognition

Covering the material in Stanford’s CS231n Spring 2017 course headed by Prof Fei-Fei Li (Chief AI Scientist of Google Cloud, Director of Stanford AI Lab). This session will cover topics like image classification, object detection, image caption, visual question answering, feature visualisation and adversarial training.

Course Page: http://cs231n.stanford.edu/2017/syllabus.html Lesson 3: Video: https://www.youtube.com/watch?v=h7iBpEHGVNc Slides:http://cs231n.stanford.edu/slides/2017/cs231n_2017_lecture3.pdf Lesson 4: Video: https://www.youtube.com/watch?v=d14TUNcbn1k Slides:http://cs231n.stanford.edu/slides/2017/cs231n_2017_lecture4.pdf Course Notes : http://cs231n.github.io/ Session 3: Natural Language Processing with Deep Learning

Covering the material in Stanford’s CS224n Winter 2017 course taught by Professor Christopher Manning and Richard Socher (Chief Scientist of Salesforce). This session will cover topics like word vector representations, dependency parsing, recurrent neural networks and language models, machine translation, attention models, tree recursive neural networks, and speech processing.

Course Page: http://cs224d.stanford.edu/syllabus.html Lesson 2 : Video: https://www.youtube.com/watch?v=ERibwqs9p38 Slides: http://web.stanford.edu/class/cs224n/lectures/lecture2.pdf Lesson 3 : Video: https://www.youtube.com/watch?v=ASn7ExxLZws Slides: http://cs224d.stanford.edu/lectures/CS224d-Lecture3.pdf Course Notes : http://cs224d.stanford.edu/lecture_notes/

For ease of the facilitator in-charge’s preparation for any particular week, participants are encouraged to read the papers beforehand and post questions on specific parts of the papers using the Nurture.ai platform’s highlight-commenting function.

Assignments/Tasks

Task 1 : Multi-Class Classification : (Trashnet)

Link : https://github.com/garythung/trashnet Dataset Link: https://drive.google.com/drive/folders/0B3P9oO5A3RvSUW9qTG11Ul83TEE

Use the Dataset-Resized.zip for the dataset. Please Compare your performance with the authors performance. Write a Brief description about how you did it ?

Minutes of the Meetup : #4: Lesson 2 : Recap

Data Augmentation :  random Brightness, Rotation, Zoom,  Contrast

Pre-Compute Vs Pre-Training Differences

Learning Rate Annealing Decreasing rate  as time progress (Drop by 10 times)

Cosine Positive Half is used to Decrease the LR (Instead of Step)

Differential Learning Rates: Layer Groups 3 Groups : [Earlier middle Last]

epochs: no of iterations

Cycle_len= no of cycles or restarts (Finding the perfect spot)

cycle_mult= rate at which lr is decreased (Duration will increase)

learn.sched.plot_lr()
Lesson 3 :

Relationship between of Batch Size and Learning rate : https://miguel-data-sc.github.io/2017-11-05-first/

Download Data From Kaggle : Kaggle-cli or CurlWget Extension Method

Symbolic Link : Similar to Shortcut: usage :ln -s src dest

Minimum Steps to Build a model:

Pre-Compute vs Data Augmentation :

Batch Norm : Bigger\Large Models : Similar Dataset and Freeze layers of Batch Norm.

Keras Version on Lesson 1

Shuffle Validation : False

Dog- Breeds Challenge Very Similar to Trash Classifier

learn.TTA(is_test=True) - To do Prediction on Test Set

df.to_csv() use Compression to make size smaller

FileLink('Path to File)

Individual Prediction

Image Kernels : Otavio viz Video Please Watch (no Direct Link)

Excel Explanation

Number of Channels Vs Kernel

Activation Function : http://neuralnetworksanddeeplearning.com/chap4.html

Multiple Labels on single: Softmax dont use - picks only single thing

Multi Label : Sigmoid

traditionally use from_csv approach coz same file cannot exist in multiple folders

top_down: All possible transformation 8 symmetric rotation

shift +tab ; Gives you function details

Start from small images and then upscale it (When using images different from image net)

F2 Score : https://en.wikipedia.org/wiki/F1_score (Mentioned by Kaggle)

When Resizing we transform to required size and do a center crop

For More Detailed Notes : http://forums.fast.ai/t/deeplearning-lecnotes3/7866

***Cs231n : ***

Lesson 3 :

Revisit : Linear Classifier :

Loss Function: Quantitatively determine how Bad the Weights ?

How Loss changes : W small : Loss min : no of Classes-1.

Regularisation : Extra term added to loss to pick simple Weigths(Smaller and Better)

Hingle Loss

Softmax: Cross Entropy

Lesson 4:

Back Prop : Recursively use Chain Rule to compute gradient wrt to all variable

How is Backprop is computed?

Numeric Gradient vs Analytic gradient

Code Implementation of Backprop (If Interested )

Cs224d:

Lesson 2 :

Meaning of a Word: Defined by what it signifies in real world (What it Denotes)

Using Taxonomic Resources ..  As new words come in or different kind of usage occurs then many meaning will be missing.

One Hot Representation : No inherent notion of relationship between words (Orthogonal to each other)

Distributional Similarity :  Find all occurrence of the words with its surrounding to understand the context (Different from Distributed Representation)

Objective is to find out a vector(Preferably Dense)

Embedding is the vector representation of words. Eg :Word2Vec

Define a model to predict the center word /surrounding words when the surrounding words/center word are given

define loss how close to the context

Skip Gram : Predict center word when surrounding word is given. Maximize the probability of Center word Loss : Cross entropy loss
Lesson 3 :

What is Glove ?

Advantages of Glove ?

Understanding the performance and working of glove
