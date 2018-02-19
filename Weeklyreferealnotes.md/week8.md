http://forums.fast.ai/t/deeplearning-lecnotes3/7866
https://medium.com/@gokkulnathts/ai-saturday-bangalore-chapter-trash-classifier-tutorial-8e6b3c6860c5
http://forums.fast.ai/t/deeplearning-lec4notes/8146
**** Fast.ai : Lesson 3 and 4 Revisited : ****

Relationship between of Batch Size and Learning rate : https://miguel-data-sc.github.io/2017-11-05-first/

Download Data From Kaggle : Kaggle-cli or CurlWget Extension Method

Minimum Steps to Build a model: Refer Lesson1-Resnext.ipynb

Batch Norm : Make All intermediate Activation Zero Mean and unit variance. Converges Faster.
Tip :  Bigger Large Models on Similar Dataset and Freeze layers all Batch Norm layers.

Dog- Breeds Challenge Very Similar to Trash Classifier

learn.TTA(is_test=True) - To do Prediction on Test Set

df.to_csv() use Compression to make size smaller

Image Kernels : http://setosa.io/ev/image-kernels/

Activation Function : http://neuralnetworksanddeeplearning.com/chap4.html

Multiple Labels Problem: 
-Dont use Softmax  - picks only single thing
-Use Sigmoid -Gives Confidence Score of each label
-Use from_csv approach coz same file cannot exist in multiple folders

top_down: All possible transformation 8 symmetric rotation 
Structured Data - Deep Learning : Rossman Competition:
Categorical(a,b,c) and Continuous (1,1.4,2,2.4,3)

Separate Categorical (astype('category'))and Continuous values into different variables.(Type cast accordingly)

Use of Embeddings instead of One Hot Encoding

Data Imputation : Handling Missing Values : -99999, -1 ,Mean,Median

Fast.ai Library Specific : 
proc_df : Pulls the predict variable and puts into separate frame
do_scale : Scale data
missing value : categorical : 0 continuous: median value new bool column appended to show whether the value was missing.

ColumnalModelData.
1) from_data_frame : PATH, val_idx,df,yl,cat_flds ,bs

2) get_learner: Creation of model
NOTE : Data Object is used to create learner object
Embedding Matrix or Distributed Representation: Use random weights initially and tune them to optimal value used for encoding categorical value . Min of (50, cardinatlity+1/2)
Cardinality ? No of unique Values in a Categorical Variable


add_datepart() - 
custom metrics : define as function and pass it as parameter in fit.

When we do Inference we don't perform dropout( It is Done only in Training : Val accuracy  will be better as some neurons are off) : Ps- Dropout Parameter (Default Value : Initial layers 0.25 and  later layers 0.5. Over fitting increase value and under fitting lower the value) (Recommendation : Same dropout or dropout only at the end)
Jupyter Notebook Tip : shift +tab ; Gives you function details

**** Assignments:  ****
DogBreeds Challenge On Kaggle : Atleast try to make One Submission 
Analytics Vidhya : Try Loan Prediction III Challenge (edited)
