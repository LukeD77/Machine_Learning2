A)
[Filter 1](https://user-images.githubusercontent.com/67921793/87493981-f2e91680-c61b-11ea-8db2-3e05b4d0114e.png)
This first filter accentuates vertical lines. This is useful for identifying the rungs in the staircase or
structural support architecture. 


[Filter 2](https://user-images.githubusercontent.com/67921793/87494065-21ff8800-c61c-11ea-80e7-28c926938c81.png)
This filter accentuates horizontal lines. This is useful for identifying handrails.


[Filter 3](https://user-images.githubusercontent.com/67921793/87494179-5e32e880-c61c-11ea-9b0d-6dde23b4f7d9.png)
This third filter does both as well as further emphasizing all lines that it sees. This filter is useful because
it optimizes the amount of code needed to identify structures in an image.

When a filter is applied, the model iterates through each pixel and multiplies them and its neighbors by the values in the filter
and adds them up to get the new pixel value.
This keeps the image the same size as before it was conveluted. Applying the filter to convelute the image aids the computer
in recognizing patterns in the data via their enhancement by the filter. The computer can then learn to recognize these patterns
over time and better identify objects. 

B)
Pooling takes a an area of pixels in preset dimensions and selects the pixel with the highest value to be made into a new photo.
This process is iterated over the entire convoluted image, eventually making a new image with the selected pixels. This decreases the size of the image, therefore reducing the amount of computation needed to analyze them. We are using max pooling
as we keep the highest pixel value.

[Pooled image](https://user-images.githubusercontent.com/67921793/87494991-55431680-c61e-11ea-876f-df34bb1e8c4a.png)

C)
The accuracy of the neural network was improved as it reached 99.8% accuracy after only 9 epochs of training.
The test accuracy was 0.9847999811172485, so slightly overfit but not by much.
[Convolutions](https://user-images.githubusercontent.com/67921793/87500089-ae647780-c629-11ea-808e-2a2d6bca203d.png)

The filters identified three patterns within the data. A top bar, which is indicative of a 7 or 5, a vertical line which
could be a 7, 9, 1, or 4, and a loop pattern which could mean a 5,6,8,9, or 0. The identification of these patterns in a test
image allows the computer to see and put a pattern to the image and determine its value. 
When reducing the convolutions to 16, the test accuracy increased from 0.9847999811172485 to 0.9858999848365784. The runtime
for each epoch also decreased from 16 to 11 seconds. The model took the same 9 epochs to reach 99.8% training accuracy.
If you add more convolution layers, the time for each epoch increases to on average 18 seconds and it took 12 epochs to fit the training
data with 99.8 percent accuracy. However, the testing accuracy also increased to 0.9926999 while the training score was 0.9927. This model
is not overfit at all. 


