The initial training of the model started out with a CNN with one convolutional layer at 32 neurons and a dense layer with 
500 neurons outputing to 1 neuron. All the neuron activations were relu. I set the batch size in each image generator to 50 
and ran the first model on 1000 training images and 500 testing images once I was reliably able to run the model on much 
smaller datasets. With an adam optimizer, 5 epochs, and 2 steps per epoch and validation, I got an mse of 660 and 
a val_mse of 740. 

I then added more convolution layers, one with 16 neurons and one with 64 neurons. I also increased the amount
of training images to 2500. Running this model with 10 epochs and 5 steps per epoch, the model output an MSE of 221 and 
a val_mse of 269. After increasing the training images to 5000 and setting 10 epochs with 10 steps per epoch, the model 
had an mse of 755 and a val_mse of 303. This model is clearly underfit. 

After this I ran the model using 9000 training images and the MSE and val MSE skyrocketed. I attempted to rectify this by
testing numerous modifications to the number of dense layers and number of neurons in each layer, I settled on adding a 
second dense layer with 250 neurons. This produced an output of and mse of 1642 and vla mse of 2233. Blue is the validation MSE 
and red is the training MSE. I could not figure out how to put a y axis on the image, unfortunately.

[figure 1](https://user-images.githubusercontent.com/67921793/88495306-84934500-cf87-11ea-95d4-9d0fcf90b83a.png)

I noticed when examining the data that the last folder, accra 4, contained many labels that were 0. I found this troubling 
since I used the 1000 images in accra 4 as my testing data. To adjust for any bias the large amount of zeros may add to the model
I repartitioned my training and testing data and reran the model. My MSE then was 1635 and the val MSE was 2399. Below
is a graph illustrating the MSE of this model. Blue is the validation MSE and red is the training MSE. I could not figure out
how to put a y axis on the image, unfortunately. 

[Figure 2](https://user-images.githubusercontent.com/67921793/88494417-071a0580-cf84-11ea-93b5-77d223668241.png)


