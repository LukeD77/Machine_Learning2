A)
Response 1: The image data generator takes the images in the directory and transforms them into tensors 
float 32 along with certain pixel dimensions. It also sends the images in batches along with the corrosponding
labels to the model.The target size is important as the sizes all need to be the same when being input into the 
model or else it will not function correctly or may be biased as it gleans more informtion from more pixels in one image.
When determineing the class mode you want to know what your model is doing and what the potential outputs are.
Because this model is a binary classifier and is classifying as one of two outputs we can use the mode binary.
The test set had a smaller batch size than the training set and that is because it has a smaller dataset due to
how the data were split.

Response 2: The overall structure of the CNN is 3 convolution layers each with a maxpool layer and the 
number of neurons in each convolution increases after the next layer. Then there is a flatten command and two dense layers. 
The image size decreases as it continues through the model by a half after each convolution and pool pair layer.
The sigmoid function was chosen because of the binary classification, so we can have one neuron and an output of 0 for 
a class and an output of 1 for the other class, In the compiler we used the loss function binary crossentropy because of the 
binary classification. The optimizer is RMSprop which is used when training on batch sets to regularize the amount of learning
the model achieves through each new batch of images.

B.
Regression
1.
Using the auto-mpg dataset (auto-mpg.data), upload the image where you used the 
seaborn library to pairwise plot the four variables specified in your model.  Describe 
how you could use this plot to investigate the co-relationship amongst each of your 
variables.  Are you able to identify interactions amongst variables with this plot?  
What does the diagonal access represent?  Explain what this function is describing 
with regarding to each of the variables.
2.
After running 
model.fit()
 on the auto-mpg.data data object, you returned the 
hist.tail()
 from the dataset where the training loss, MAE & MSE were recorded as 
well as those same variables for the validating dataset.  What interpretation can you 
o
ff
er when considering these last 5 observations from the model output?  Does the 
model continue to improve even during each of these last 5 steps?  Can you include 
a plot to illustrate your answer?  Stretch goal: include and describe the final plot that 
illustrates the trend of true values to predicted values as overlayed upon the 
histogram of prediction error.  
C.
Overfit and underfit
1.
What was the significance of comparing the 4 di
ff
erent sized models (tiny, small, 
medium, large)?  Can you include a plot to illustrate your answer?
