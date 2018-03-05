* (reading the data)
- import numpy as np
* (building the model)
- from keras.layers import Dense 
from keras.models import Sequential
* (reads the data to find the number of nodes)
- predictors = np.loadtxt(‘predictors_data.csv’,delimiter=‘,’)
* (reads the data to find the number of nodes in the input layer that stored as cols how many cols specifies the nodes)
- n_cols = predictors.shape[1]

* model building
- model = Sequential() (easier ways to build the model)
sequential requires weights or connections one layer after another in network diagram
* start laying the layers using add , standard layer in known as dense layer because all the nodes in previous nodes connect to current layers), u may specify layers which are not dense ) in each dense layer u can specify the number of nodes=100 in first argument and activation  and input_shape=(n_cols,)(specifying , as any number of rows after col or any number of data points)
- model.add(Dense(100,activation=‘relu’,input_shape = (n_cols,)))

model.add(Dense(100,activation =‘relu’))

model.add(Dense(1))


* model building steps 

specify architecture
compile
fit
predict

* compiling and fitting a model
specify the optimiser 
control the learning rate 
many options and mathematically complex
adam is usually a good choice 


* compiling a model 

n-cols = predictors.shape[1]
model = Sequential()

model.add(Dense(100,activation=‘rely’,input_shape=(n_cols,)))
model.add(Dense(100,activation=‘relu’))
model.add(Dense(1))

model.compile(optimizer = ‘adam’,loss=‘mean_squared_error’)


* fitting a model 
model.fit(predictors, target)


* for classification model ( we do a couple of things different)
instead of loss function as mean_squared_error  change to categotical_crossentropy(lowest is better)[hard to interpret]
so we
Add metrics = [‘accuracy’] to compile step for easy to understand diagnostics
(this is not the only loss function but far common)
modify the last layer(output layer has a separate node for each possible outcome and uses softmax activation ensures prediction sums as 1 interpreted as probability

data binary 
basketball shot  01
table stats
transform to categorial
shot results 1,0 outcome 0 outcome1(this corresponds to one hot encoding)


* classification code 

* (converts one column to multiple columns)
from keras.utils import to_categorical
* upload data
data = pd.read_csv(‘basketball_shot_log.csv’)
* use drop command to get the version of data without target column and store as numpy matrix(as_matrix())
predictors = data.drop([‘shot_result’],axis=1).as_matrix()
* use the dot notation(data.shot_result) to access the column with the prediction target we keep all the data except the column in matrix column called predictors and create target using to_categorical then we build our model looks similar to other model previously built except the line which has 2 nodes and has softmax activation function)
target = to_categorical(data.shot_result)

model= Sequential()
model.add(Dense(100,activation=‘rely’,input_shape=(n_cols,)))
model.add(Dense(100,activation=‘relu’))

model.add(Dense(2),activation = ‘softmax’) (diff from others)

model.compile(optimizer = ‘sgd’,loss=‘categotical_crossentropy’, metrics=[‘accuracy])
(differs from others)

* fitting a model 
model.fit(predictors, target)


results show 
accuracy and lass for three epoch and later improvement slows down 

* using models

save 
reload
make predictions with models

* code for saving reloading and using models
from keras.models import load_model 
* (save function) model are saved in file hdf5 (h5)
model.save(‘model_file.h5’)
* load the model
my_model = load_model(my_model.h5)
* predict the model the model i the classification here prediction come in the same prediction formate as prediction target, one col for shot missed and second col weather shot is made 
in practice want the probability weather the shot is made so extra the second column
predictions = my_model.predict(data_to_predict_with)
* so i extract the the second col with numpy index
probability_true = predictions[:,1]

* verifying model structure 
my_model.summary()


Understanding model optimisation

optimisation is difficult 
*the optimal value for 1 weight depends on the values of other weights we are optimising many weights at once , even our slope tells which was to increase or decrease our updates may not improve models meaningfully small learning rate might cause small update where models does not improve  and too large learning rate may take to direction that seemed to but optimisation problem still exists a smart optimiser like adam help but problem still exist but easiest way to see the effect of different learning rate is to use simplest optimizer SGD this use fixed learning rate 0.01 and specify the argument as SGD(lr=lr)
-simultaneously optimise 1000s of parameters with complex relationships
- update may not improve model meaningfully
- update too small(if learning rate is low) or too large(if learning rate is high)

def get_new_model(input_shape = input_shape):
	model = Sequential()
	model.add(Dense(100,activation =‘relu’,input_shape = input_shape))

model.add(Dense(100,activation=‘relu’,input_shape=input_shape))

model.add(Dense(100,activation=‘relu’))
model.add(Dense(2,activation=‘softmax’)
return(model)

lr_to_test=[.000001,0.01,1]
for lr in lr_to_test:
(we have a function that creates a new model get_new_model(), creating model in forloop each time we compile the model with SGD(lr=lr) with different learning rate and pass in the optimiser with same argument previously passed as adam in exercise u compare the result with training models trained low medium high learning rates even if ur learning rate is well tuned u can run into the dying neuron  problem this occurs when the neutron takes the value less then 0 for all the row of data recall with relu activation problem any node with neitive value produce output of 0  also has slope of zero as seen in graph because the slope is zero and any weights flowing into that node is also zero so that nodes does not get updated in other words once 
- once nodes starts always getting negative inputs 
- it may continue only getting negative inputs
- contributes nothing to the model 
- dead neuron 
-    earlier vanishing gradient we used the s taped tan function many layers had vey small  slope in deep network updates to backdrop were close to 0)
	model = get_new_model()
	my_optimizer = SGD(lr=lr)
	model.compile(optimizer=my_optimizer,loss=‘categorical_crossentropy’)

model.fit(predictors, target)


* model validation 

is used to test performance 
-commonly use validation split rather than cross-validation
models performances from your training data is not a good indicator of how it performs on new data for this we use validation data to test performance 
-validation data is data that is explicitly held up from training and only used for test performance 
-k fold cross validation takes long time and is expensive 
-single validation score is based on large amount of data and is reliable 

keras makes it easy to make sum of validation data 
code
model.compile(optimizer=‘adam’,loss=‘cat_cross’,metrics=[‘accuracy]
model.fit(predictors, target,validation_split=0.3)
keep trying when validation are improving and stop when validation are not improving we do this by early stopping 
*  Early stopping 
code 
from keras.callbacks import EarlyStopping
*befor fitting the model it takes the argument patience that how many apex the model takes without improving before we stop training  2 or 3 are reasonable values for  some time we get single epoch without improvement but the model starts improving again after that epoch but if u see three epoch with no improvement then its unlikely to turnaround and start improving again
early_stopping_monitor = EarlyStopping(patience=2)
* fit function with callback which takes the list u add other call back as u get advanced early stopping is what u want for now 
model.fit(predictors, target, validation_split = 0.3, epochs=20,
callbacks =[early_stopping_monitor])

for default keras trains for 10 epochs
for higher epoch we can place an arguments with higher epochs 

experiment with more layers , different artitecture, few, layers with more nodes ,few nodes, creating a great model requires experimentation



# Fit model 1
model_1_training = model_1.fit(predictors, target, epochs=20, validation_split=0.4, callbacks=[early_stopping_monitor], verbose=False)

# Fit model 2
model_2_training = model_2.fit(predictors, target, epochs=20, validation_split=0.4, callbacks=[early_stopping_monitor], verbose=False)

# Create the plot
plt.plot(model_1_training.history['val_loss'], 'r', model_2_training.history['val_loss'], 'b')
plt.xlabel('Epochs')
plt.ylabel('Validation score')
plt.show()

* model capacity or network capacity 

Thinking of overfitting and under fitting

overfitting will make  accuracy  prediction on trying data but on validation data it  make  inaccurate predictions

undefitting is opposite it neither makes accurate predictions on training or validation data fails to predict important patterns in model

validation score is the ultimate measure of models predictive  quality 

model capacity = increase the layers increase the model capacity

workflow for optimisation model capacity
start with small network
get validation score
keep increasing capacity until validation score is no longer improving

*Recognizing handwritten digits 
images of handwritten digits 
MNIST dataset
28*28 pixel grid flattened to 784 values for each image
image is shown how dark pixel is by 0 = dark 255=light as possible , and he grid is flattened into one image of 784 each image shows as digit 1,2,3 till  9 model will predict which digit it is written
value in each part of array denotes darkness of that pixel


a deep learning model in those 784 features for each image for input and predicting from ten possible values for output


http://www.datascribble.com/blog/deep-learning/getting-started-keras/
https://hackernoon.com/how-to-do-real-time-trigger-word-detection-with-keras-b8a56ab106b7
