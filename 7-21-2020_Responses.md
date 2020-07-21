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


B.
1.


2.



3.
