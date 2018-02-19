Next Meetup Agenda:

1)Fast.ai : Lesson 4 : Deep Learning on Structured Dataset

Video: https://youtu.be/gbceqO8PpBg

Forum Wiki: http://forums.fast.ai/t/wiki-lesson-4/9402
2)cs231n : http://cs231n.stanford.edu/2017/syllabus.html

Lesson 5:

    Video: https://www.youtube.com/watch?v=bNb2fEVKeEo

    Slides:http://cs231n.stanford.edu/slides/2017/cs231n_2017_lecture5.pdf

Course Notes : http://cs231n.github.io/
3)cs224d: http://cs224d.stanford.edu/syllabus.html

Lesson 4 :

    Video: https://www.youtube.com/watch?v=uc2_iwVqrRI

    Slides: http://web.stanford.edu/class/cs224n/lectures/lecture4.pdf

Lesson 5 :

    Video: https://www.youtube.com/watch?v=isPiE-DBagM

    Slides: http://cs224d.stanford.edu/lectures/CS224d-Lecture5.pdf

Course Notes : http://cs224d.stanford.edu/lecture_notes/
Keras : Build Different Neural Network Architectures and Experiment on the given fashion mnist training data and try hyper-parameter tuning to improve logloss.

Note :

The Wiki page will contain solution to most of the commonly faced problems. Kindly go through them before you ask any questions.

Please watch the videos well in advance and if possible one of the participants can summarize their understandings and findings during the Meetup (Contact me if Interested)

Do Sign up in Fast.ai forums (http://forums.fast.ai/) and AI Saturdays Forum (https://ai6forums.nurture.ai/)

Please post your questions on AI Saturdays Forum as discussed in General Channel to get faster response.

Try to get some ideas/problems that you are interested to work on. Preferably with corresponding dataset.

6)For people who feel there are too many videos. Please watch as many Videos possible. You need not have 100% Understanding of the videos. Please note down the points that you are not clear.

7)Gist of the Videos will be presented followed by a discussion. Administrative Stuff and other Generic Stuff (Introductions) can be fast forwarded at your ease. Do start with Fast.ai Video and try replicating the notebook without copying the code.

Summary-----

**** Minutes of the Meetup : #5: ****

**** Fast.ai Lesson 4: ****

Linear Layer: Same as Matrix Multiplication When we do Inference we don't perform dropout( It is Done only in Training : Val accuracy will be better as some neurons are off) : Ps- Dropout Parameter (Default Value : Initial layers 0.25 and later layers 0.5. Over fitting increase value and under fitting lower the value) (Recommendation : Same dropout or dropout only at the end)

xtra_fc: {} take list of Fully Connected Layers and appends after CNN

Structured Data - Deep Learning : Rossman Competition: Categorical(a,b,c) and Continuous (1,1.4,2,2.4,3)

Separate Categorical (astype('category'))and Continuous values into different variables.(Type cast accordingly)

proc_df : Pulls the predict variable and puts into separate frame do_scale : Scale data missing value : categorical : 0 continuous: median value new bool column appended to show whether the value was missing.

ColumnalModelData.

from_data_frame : PATH, val_idx,df,yl,cat_flds ,bs

get_learner: Creation of model NOTE : Data Object is used to create learner object Embedding Matrix or Distributed Representation: Use random weights initially and tune them to optimal value used for encoding categorical value . Min of (50, cardinality+1/2) Cardinality ? No of unique Values in a Categorical Variable

Effect of vanishing gradient in structured data.
add_datepart() - custom metrics : define as function and pass it as parameter in fit.

Data Augmentation on Columnar Dataset ?

Language Modeling : Predict Next word : Swift key
Token : Symbol/ word : Use Spacy to tokenize Torchtext library used to preprocess

LanguageModelData backpropthroughtime : bptt Vocab : List of Unique words

Adam : Beta Value : (0.7 to 0.99) AWD LSTM : Dropout distributed across the layers Gradient Clipping : 0.3 (Max)

Torch Text Splits : Split the data into bits : Built in in Torchtext

**** CS-224d : NLP: Fundamentals Of NLP : Representing a Words as Vector ****

Lecture 2 and 3 : Revisited :

Need for Word2Vec. Disadvantages : Computational Expensive and Doesn't not exploit Statistics problem.

Co-Occurrence Matrix : Co-Occurrence matrix is used to get word embeddings (by Exploiting Statistics), A Dense vector is obtained using SVD and other matrix decomposition techniques. Co-Occurrence can be formed by considering a neighboring window or by considering the entire corpus. Disadvantages: Common tokens like "the","a","he","she" etc.. become dominant(More no of count will be observed) and affect the embeddings derived. It is not feasible as the vocabulary size becomes large.

Glove : Exploits both Word2Vec and Co-Occurrence approach.

The Embeddings obtained are highly dependent on the data from which it was obtained.

Dropout can used to test the stability of the model and get a feedback on generalizing capacity of the model.

Gradient clipping in commonly used in RNN/LSTM since the gradient tends to explode as it flows through the network.

Lecture 4 and 5 : Will be Discussed in Next Meetup

**** CS-231N : Will be Discussed in Next Meetup; ****
