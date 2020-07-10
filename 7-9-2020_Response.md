1) TF Hub is a library that hosts reusable machine learning models. These models can be applied to other datasets, speeding up trainin and improving generalizaiton.
We used it by creating the first layer as a hub layer.

2) the optimizer is adam which uses a stochastic gradient descent method of calculation making it suitable for large datasets. The loss function is BinaryCrossentropy. This calculates the cross entropy 
between labels that can be categorized into two categories. The model had an accuracy of 0.856, or 85.6 %. 

3) ![Training and validation loss](https://user-images.githubusercontent.com/67921793/87189861-6d820100-c2bf-11ea-87cf-50b85402aed7.png)

This graph displays the loss function output compared to the number of epochs the model cycled through. The validation loss is the loss function output when training the data, and the prediction on the test data.
The negative slope is typical of a stochastic descent model and displays a reduction in the loss function over each epoch.

4) ![Training and validation accuracy](https://user-images.githubusercontent.com/67921793/87190333-4841c280-c2c0-11ea-9ee1-c68437eeb094.png)

This graph displays the accuracy of the model in predicting the connotation of a movie review compared to the number of epochs the model cycled through. The positive trend is typical as the optimizer is 
adjusting the cost function with the returns from the loss function. There seems to be a platue at 4 epochs, meaning after 4 epochs we are gaining less returns in run time versus accruacy and may be 
overfitting the model.
