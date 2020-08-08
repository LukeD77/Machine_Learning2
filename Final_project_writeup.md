[Poster.pdf](https://github.com/LukeD77/Machine_Learning2/files/5044608/Poster.pdf)


A.	Problem statement
In the midst of a pandemic, many people are wearing a mask for the first time. They may be doing so incorrectly or, most importantly, not wearing 
one at all. Research has shown that wearing masks reduces the spread of COVID and saves lives. This is why it is important to educate the public about the benefits of 
wearing a mask. Just as the Truth campaign to end smoking tailors their argument towards teenagers, these education campaigns are most effective when targeting people 
who are less likely to wear a mask. My question is: can I sentiment towards wearing masks by group of people such as age and gender contribute?
The goal of this project is to compare the age and gender of people and to their sentiment towards wearing masks to determine if there is any connection. There is an 
emphasis on implementation of the methods to show that structured data can be extrapolated from unstructured data and analyzed in order to inform real world decisions.

B.	Data
The preliminary data was collected from Twitter and was composed of tweets containing the phrase “wear a mask” and the profile pictures corresponding to the accounts 
that posted the tweet. I received 2693 tweets and profile pictures using a Twitter API. From these data I extracted my feature data and target data. My feature data 
consists of the age and gender of the person posting the tweet and these attributes were determined from the profile picture. The gender is either male or female and 
the age is split into 8 groups that contain a range of ages. The 8 groups together consist of ages from 0 to 100 and the groups were (0-2), (4-6), (8-12), (15-20), 
(25-32), (38-43), (48-53), (60-100). Therefore, the age and gender are both discrete variables. The model used to determine age and gender did always find a face to 
run an analysis on, due to either a default profile picture or some picture that was not of a person, therefore giving no age or gender value. These data, along with 
the corresponding tweet, were removed from the final dataset used in analysis. My target data is the sentiment towards masks which was extracted from the tweets collected. 
These data were either kept in a continuous form ranging from -4 to 4 or converted into discrete data where values above zero were labeled as ‘positive’ and labels below 
zero labeled as ‘negative’. 

C.	Methods
The first model used was a sentiment analysis model. This model is a tensorflow RNN model that was used in a lesson to predict the sentiment of movie reviews. I trained the 
model using the structure used in the text analysis tutorial on tensorflow with an embedding layer, two bidirectional layers, a dense layer with 64 neurons and an aggressive 
dropout layer of 0.5. The model was trained on the IMB move review dataset for 10 epochs. After testing the model on a few sample tweets that wrote with very explicit connotations 
towards masks, I realized the model was highly inaccurate, so I retrained the model using a Yelp review dataset, which yielded better results. The image analysis model that 
determined gender and age was a model produced as part of the OpenCV2 project.  The model contained three convolutional layers with 96, 256 and 385 nodes respectively and a 
decreasing kernel size from 7 to 5 to 3. It then had two inner product layers with 512 neurons each and both were follower by a dropout layer that removed half the neurons to 
prevent overfitting. The final layer was either a 2 neuron output for the gender model, which corresponded to either male or female or it was an 8 neuron layer for the age model 
that corresponded to the 8 different age ranges mentioned earlier.
After this the feature data and target data, one set in continuous form and another set using the discrete form, were analyzed using a bar plot and decision tree classifier. 

D.	Model Performance
The  accuracy of the final output depends on the accuracy of the feature data and target data extracted from the profile pictures and tweets respectively. The first model, the 
sentiment analysis model, was at first inaccurate when attributing sample tweets a sentiment value, but increased in accuracy when trained on the Yelp review dataset instead of 
the IMB movie review dataset. The age and gender classifier was rather accurate when they pictures were very clear; however, the picture size and quality when pulled from Twitter 
were very low, so the model was less accurate. There were also many pictures where no face was detected. This may be due to a default profile picture on Twitter or no face was 
actually in the image. 

E.	Analysis
I first made a barplot illustrating the different age groups and genders’ sentiment towards wearing a mask using example data generated through a random number generator because I 
was unable to produce a large amount of age and gender data. I then used another randomly generated dataset for the decision tree classifier with showed equal partitioning of 
positive and negative reviews in the second and fourth leaf, but showed more negative sentiments in the 1st and 3rd leaf.

F.	Compare to other studies
A study conducted by Zubair, et al. using an online survey of Pakistani people found a significant correlation between gender and the frequency of wearing a mask with 78% of 
females wearing them and 59% of males wearing them (Zubair, et al., 2020). I would compare my results to the results of this study to determine if my correlation in gender and 
mask sentiment coincide with the percent mask usage by men and women.

G.	What to do next
To take my model one step further, I would finish setting up an automated workflow for cleaning up the image data. This would allow me to run the images through the age and gender 
classifier in large batches to increase the amount of data to conduct my analysis on. I could also include more features in the data such as what state the users live in or what 
political party the governor of their state belongs to. I could also modify that data I pull from twitter to either include different search phrases to increase my dataset, I could
create a live stream of data that would update the model over time, or I could conduct my analysis on tweets before and after a mask mandate is implimented within a specific state.

References
Zubair, K. ., Luqman, M. ., Ijaz, F. ., Hafeez, F. ., & Aftab, R. K. . (2020). Practices of General Public Towards Personal Protective Measures During the Coronavirus Pandemic. 
Annals of King Edward Medical University, 26(Special Issue), 151-156. Retrieved from http://annalskemu.org/journal/index.php/annals/article/view/3629
