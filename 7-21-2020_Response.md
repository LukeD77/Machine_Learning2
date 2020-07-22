A.
1)
We split the labels by using pop to remove the labels from the original dataset and make it into its own.
The labels were: Setosa, Versicolor, and Virginica and they were kept in the variables train_y and test_y.

2)
5 examples of estimators are: DNNClassifier, DNNEstimator, DNNLinearCombinedClassifier, DNNRegressor, and 
DNNLinearCombinedRegressor.

DNNClassifier = tf.estimator.DNNClassifier()
DNNEstimator = tf.estimator.DNNEstimator()
DNNLinearCombinedClassifier = tf.estimator.DNNLinearCombinedClassifier()
DNNRegressor = tf.estimator.DNNRegressor()
DNNLinearCombinedRegressor = tf.estimator.DNNLinearCombinedRegressor()

3. 
The input function converts the overall dataset into batches of smaller datasets and can shuffle in repeating
images if training=True.
The feature column tells the model what the nature of our input data is and how to use it. Because the data
we are using to predict the species are numerical measurements, we want to present them to the model as such.

4.
In short, classifier.train actually runs the model on the given data. The classifier is the model which 
is a DNNClassifier that contains two hidden layers, one with 30 neurons and another with 10, and gives an
output of one out of 3 classes. After calling .train, the model is being fed data in batches from the 
input_fn function that was defined earlier.

5.
DNNClassifyer test set accuracy: 0.533 -- rank 3
DNNLinearCombinedClassifier test set accuracy: 0.733 -- rank 2
LinearClassifier test set accuracy: 0.967 -- rank 1

B.
1.
[pairplot](https://user-images.githubusercontent.com/67921793/88133733-c3ed1a80-cbb0-11ea-8578-b439c5fa2ee3.png)

[Barplot of age](https://user-images.githubusercontent.com/67921793/88133747-ce0f1900-cbb0-11ea-9ac6-0019ef59e479.png)

The barplot of age matches the middle probability distribution function in the top left corner where age is compared to age. This displays how many of the data fall within certain categories and if you were to calculate the area under the curve you could find out how much data are in certain excerpts of the dataset.

2.
A categorical feature column defines a feature that will be used by the model. Explained differently, it
tells the model how the data is represented and should be interpreted based upon its class. A dense feature column is a categorical column that is transformed to an indicator column and then a dense column. This is to allow it to be used in the dense features layer which allows you to examine an output.


3.
The feature columns contained numerical values such as age and number of siblings and spouses. It also contained categorical information such as what deck the people were living on, gender, and what port they embarked at. You would asses the results from your intial output with the linear_est.evaluate command that would act on the eval_input_fn that contains the test data. The interatction between age decreased the accuracy of the model.

without cross column test accuracy: 0.76
with cross column test accuracy: 

[ROC curve without cross column](https://user-images.githubusercontent.com/67921793/88132612-02cda100-cbae-11ea-99c9-d22e65528635.png)

[ROC curve with cross column](https://user-images.githubusercontent.com/67921793/88132617-06612800-cbae-11ea-8f7b-ed58453d0e71.png)

If you flip back and forth between the ROC graphs you will notice that the cross column graph exhibits a slightly lower false positive rate than the model without the cross column.
