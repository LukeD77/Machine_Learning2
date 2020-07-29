C.
1.
One hot encoding would be inefficient for a large corpus of data, such as the one we are using, 
because it would require n number of rows and columns where n is the number of words in the corpus. 
Word embeddings not only allow us to represent words like one hot encoding does, but it also allows us to
display what meaning certain words give to a corpus. These embeddings are learned by the model in an
unsupervised manner. 

2.
[figure 1](https://user-images.githubusercontent.com/67921793/88744464-6d825d80-d115-11ea-875b-88fa3f5d836a.png)

From this graph of the training and validation loss over a number of epochs you can see that the training loss steadily decreased while the validation
loss decreased, but started to increase. This change to increasing loss in the validation means that the model is becomming overfit on the training
data.

[figure 2](https://user-images.githubusercontent.com/67921793/88744552-b2a68f80-d115-11ea-83cc-9ede3aab252d.png)

This second graph depicts the training and validation accuracy over a number of epochs. The accuracy of the training set continues to increase
while the validation accuracy is roughly unchanging over time besides a small fluctuation. This model does not need to be trained very long. 6 epochs apears
to be the optimal number of epochs to train the model at.

D.

[figure 1](https://user-images.githubusercontent.com/67921793/88745295-ad4a4480-d117-11ea-8775-74af70fc66e3.png)

This graph depicts the training and validation accuracy over a number of epochs in the simpler model. The training accuracy increased more than the validation accuracy,
which plateaued earlier on.

[figure2](https://user-images.githubusercontent.com/67921793/88745306-b76c4300-d117-11ea-8325-a194890c606c.png)

This graph depicts the training and validation loss over a number of epochs in the simpler model. The training loss decreased more than the validation accuracy,
which plateaued earlier on. The loss eventually started to increase meaning we were overtraining the model.

[figure3](https://user-images.githubusercontent.com/67921793/88745971-53e31500-d119-11ea-9bb2-7c8cbe2e4fc4.png)

This figure shows the training and validation accuracy over a number of epochs for the complex layered model.
Just like the other model, the training accuracy increased more than the validation; however, both values are
higher than the other model.

[figure 4](https://user-images.githubusercontent.com/67921793/88746334-4ed29580-d11a-11ea-8b18-9758b060a196.png)

This graph depicts the training and validation loss over a number of epochs in the complex model.
The model is extremely overfit with the validation loss steeply rising over the number of epochs.
