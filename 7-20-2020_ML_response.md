A.
Due to COVID 19 and the implemintation of safety guidlines, the informing and enforcement of these guidelines are needed to
protect the health of others. The problem is that some people will not follow these guidelines. To aid in enforcement and targeted
informing of certain groups, can a machine learning model be made that predicts the probability that a person will wear a mask
based upon their personal characteristics? The personal characteristics would include age, race, politicla party, gender, etc. and
whether or not a person would wear a mask would be determined by a connotative analysis from that person's social media post. 

Problems with the study would be first obtaining data that includes personal characteristics and posts of a large number of individuals.
This dataset may also oversample certain groups of people such as a younger age group. That is even if this identifying information
is available from social media outlets to be downloaded as a dataset. Another obstacle of the study is using a conotation of 
a tweet as explicet denial to wear a mask. A person may complain about wearing a mask and therefore have a negative conotation, but
will still wear a mask. A possible avenue around a lack of data is using data from numerous social media sites; however, I could
then be sampling the same person twice if they are on both platforms. 

Other important variables that I would like to include in the model is whether or not the person is a parent that is caring for children,
caring for their own parents, or have health problems. 

C.
[Poster to use](http://cs229.stanford.edu/proj2017/final-posters/5143874.pdf)

D.
1) We used the optimizer RMSprop which is the root mean square prop. This keeps the moving average of the 
sqaured gradients for every weight and then divde by the sqaure root of the mean square. This accomadates
for large datasets better than rprop alone and it also accounts for different gradients with each batch of data which is what we are doing here when we have data in steps.

2) Our loss function is binary crossentropy. This function is used because we are deciding between one of 
two classification, so a binary model. The crossentropy part is from statistics meaning the uncertainty
of a distribution. This relates to the probability of picking one of two classifications, which the model is doing. The estimated entropy and the cross entropy are calculated and then compared in what is known as the Kullback-Leibler Divergence. The loss function minimizes this comparison by finding the best probability of the classifications.

3)
The accuracy metric calculates how often the predicted answer or label is the same as the true answer or label. This is simply a percent correct metric that the model calculates. 

4)
(Model Accuracy)[https://user-images.githubusercontent.com/67921793/88000931-d8f07d80-cacc-11ea-9406-122ca1519d0b.png]

This graph depicts the training and validation accuracy. The model appears to start to overfit around 6 epochs and training the model longer than that is not advisable. This is apparent by the plateau of the blue line (validation), but the continuation of the red line (training).

(Model Loss)[https://user-images.githubusercontent.com/67921793/88001122-6207b480-cacd-11ea-902f-9fb9eb86076d.png]

This graph depicts the training and validation loss. As it is clearly seen, the loss no longer continues a downward trajectory starting at epoch 6 and starts to increase again. This is also the point that it strays from the training loss. This coincides with the model accuracy when determining that training after epoch 6 leads to an overfit model and is not advised.

5)
(dog1)[https://user-images.githubusercontent.com/67921793/88004387-ee69a580-cad4-11ea-9a60-83ddbd16641a.jpg]

(dog2)[https://user-images.githubusercontent.com/67921793/88004407-f75a7700-cad4-11ea-96e9-4f74ac2c925a.jpg]

(dog3)[https://user-images.githubusercontent.com/67921793/88004551-3dafd600-cad5-11ea-9a8b-416debbe05e7.jpg]

(cat1)[https://user-images.githubusercontent.com/67921793/88004541-35f03180-cad5-11ea-9e92-be6c793a4da8.jpg]

(cat2)[https://user-images.githubusercontent.com/67921793/88004347-d5f98b00-cad4-11ea-9099-dd93a733768f.jpg]

(cat3)[https://user-images.githubusercontent.com/67921793/88004370-e4e03d80-cad4-11ea-857c-371cc046eb5e.jpg]

As you can see from the images, these pictures feature dogs and cats with features that are not as defining as other dogs and cats. I wanted to put the model through its paces and these are the results that I got.The model identified all the dogs correctly; however, it also identified cat 1 and 3 as a dog.
Cat 1 was a hairless cat, so the model certainly would have a harder time identifying it if there were no hairless cats in the dataset. Cat 3 may have been misidentified because of its longer face. To improve the accuracy of the model I would have been sure to include all breeds of cats and dogs when training the model to ensure that the model has seen all variations of cats and dogs, since they can vary widely in appearance. 

