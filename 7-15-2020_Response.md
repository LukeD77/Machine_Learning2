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
Response 1: [Figure 1](https://user-images.githubusercontent.com/67921793/87625752-ec7c9c80-c6f8-11ea-817a-ba6d4c5b29ec.png)

This plot can be used to investigate the relationships  between variables because it displays they plots
of numerous variables against each other. We then want to look for general trends in the data and obvious patters. For example, as the number of cylindars increases so does the displacement of the car.
The diagonals is a frequency distribution of the number of cars in the dataset that fall into that category of data.


Response 2: The loss in the last 5 observations is speradic as it falls then rises and falls again. This demonstrates that the model is no longer improving over these 5 epochs and increasing the number of epochs even more will not yield benefits to model accuracy. 

[Figure 2](https://user-images.githubusercontent.com/67921793/87626429-45990000-c6fa-11ea-875b-002262f9b9ae.png)


C.
Response 1: As the models got larger they took longer to process and the large and medium model became highly overfit.

[figure 1](https://user-images.githubusercontent.com/67921793/87629203-90b61180-c700-11ea-9d63-701250ba141c.png)
