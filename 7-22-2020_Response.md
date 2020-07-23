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


2.


3.
