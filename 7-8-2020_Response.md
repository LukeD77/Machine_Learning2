1)  A: He splits the data into training and testing because if we only trained the model on one set of data, it will get overfit. It allows for the verification of the model's accuracy in identifyng images it has not seen before in training.

B:  relu turns any neuron output that is less than zero to zero. This alleviates the effect of the negative neuron values on other neurons. Softmax takes the largest value out of all the neurons in the layer and turns it to 1, while setting all other neuron values to zero. There are 10 neurons in the last layer because we are predicting 1 of 10 outcomes, so there is a neuron for each prediction.

C) The loss function gives penalties to the model predictions that are incorrect. These penalities are fed into the optimizer that adjusts the weights for each neuron based upon the size of the penality from the loss function.

D) 
1. 60000, shape = 28,28
2. 60000
3. 10000, shape = 28,28
4. 
