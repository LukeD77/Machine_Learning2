A.
1.
A one-hot-encoded column categorizes categorical data by separating it into n columns pertaining to
n categories with a 1 in the column coinciding with the correct category.
This allows the model to easily identify categories while also preventing them from being ranked or considered
ordinal data.

2.
A dense feature column adds zeros to any blank data entries. This is useful as it indicates absenses in a dataset
and is easier for the model to read. 


3.
[Linear estimator probabilities](https://user-images.githubusercontent.com/67921793/88244759-c27c2a80-cc62-11ea-915e-163bf2948c13.png)

[Boosted trees probabilities](https://user-images.githubusercontent.com/67921793/88244761-c445ee00-cc62-11ea-9941-1b7d3e9a285b.png)

The figures show a clear disparity between the models, where the linear estimator acted almost as a binary
classifier and predicted either survived or didnt vs the boosted trees, which predicted probabilities continuously.
Both models agree that the data are centered at the ends of the probability range.

[ROC](https://user-images.githubusercontent.com/67921793/88244763-c60fb180-cc62-11ea-962d-a0b72e59f3c8.png)

The ROC is generally good as the false positive rate of the model's predictions do not hit 0.2 until at 
0.8 of the true positive rate. Therefore, 4 out of 5 of its predictions are correct. Calculating the area
under the curve allows us to interpret how much data falls within a certain section of the graph.
If we were wanting to set a threshold on the data at a certain point of false positives, we could then 
calculate the amount of data that falls within that threshold.

B.
1.
[Feature values bar plot](https://user-images.githubusercontent.com/67921793/88245545-931aed00-cc65-11ea-8b99-cc7a532f174c.png)

[Violin Plot](https://user-images.githubusercontent.com/67921793/88245560-9c0bbe80-cc65-11ea-8472-9a9fc776d1bc.png)

Gender, age, and class appear to be the top three contributor, in that order.

2.
[Gain feature importance](https://user-images.githubusercontent.com/67921793/88246144-a5962600-cc67-11ea-99d5-0c16998a7e08.png)

This figure displays the feature importance to the probability in both directions, positive and negative.

[Directional feature importance](https://user-images.githubusercontent.com/67921793/88246167-b9418c80-cc67-11ea-9c89-fb403465ac8f.png)

This figure displays the features' importance to the probability as an absolute value, so only in the positive direction.

Clearly, sex is the most important factor when determining the probability of survival; however, the figures are not in congruence about the ranking of values after that. In the Gain feature figure, the second most valued feature is class, whereas age and fare are the second and third highest contributors in the mean directions feature graph.
