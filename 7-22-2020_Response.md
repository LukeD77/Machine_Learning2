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


Jump Start Data Science Speaker Session 7/24

Ben Arancibia
•	BA in international relations and environmental policy in 2011 focusing on quantitative economics from WM and master’s in data science for City University of New York
•	Works at GSK – a British multinational pharmaceutical company
•	Got a grad certificate in GIS from VCU 
o	Became a GIS developer to do route optimization for USPS
o	Then did management consulting and got masters 
o	Good at building big data platforms and building ML algorithms
•	Past few months in pharmaceuticals has been busy with covid
o	Ben works in biostats	
	Stat analysis and programming of clinical trial data
	Very controlled scientific experiments and covid is difficult to report soundness of experiments in a way that is explainable
o	Old way of thinking that having 2 entities in groups: hardcore math people to construct experiments and plans and programmers that enact that plan
	Don’t need separation of these individuals
	Speed to market 
•	Some biostat people do covid modeling and showed we have the ability to do quick to market analysis that don’t need statisticians to do the plan and everything
•	Hiring
o	Know type of data science you want to do
o	Need to understand there is academic research orientated data science and business path of data science
o	Know where you are applying
o	Have tech skills like R or python and be able to talk about problems you have solved before
o	Connections
	Civilian data hackers that tackle problems themselves and means you can work on a project in real life and use that experience and connections to help hire
•	Use Linkedin
•	Data science interview
o	Depends on the sector you interview in
o	Management consulting
	Phone screen then team lead that drills you on how to do business problems and ask tech questions
	Third interview where you go to panel discussion and deeper dive into tech skills and business knowledge or problem solving skills
	Some have you solve problems and provide the way you do work
	Some interviews do whiteboard exercises 
•	How well you are able to solve problems involves googling answers and figuring out how to tackle things
•	Gap year to grad
o	Some programs require years of experience before you can apply
o	Went to labor market first because didn’t know if wanted to be ds 
o	Wanted to see what skills wanted and then went to masters to get on paper data science degree
•	GIS analyst and developer
o	Moved away from it being central core because he has it as tool in toolbelt 
•	Have strong domain knowledge of the business and be able to speak well to convey results and importance info about the data
•	Parting words
o	Get first job and it doesn’t even need the title of data science
o	Build network and in smart way and be personal when reaching out


Jasper Liu
•	Head of DS for Tripadvisor
•	Bachelor of Economics and math from WM
•	Master’s in mathematical finance from Boston University Questrom School of Buisness
•	Worked at Wayfair as up to a DS manager for 4 years
•	Class of 2011 from wm
•	Programming
o	Realized didn’t want to work in finance
•	Graduated with masters and went to Liberty mutual for 2 years
o	Insurance is highly regulated and slow moving
•	Wanted to go to face paced company and was picked up by wayfair
o	Pricing work
o	Looking at trends and supply demand
o	Also did product performance side and investing in certain brands
	Predictive analytics
o	Pure data science – product recommendations
o	Product curation – what types of products you want to keep because people like them and why
•	Went to Tripadvisor
o	Head data science function for flights cars and groups so investing their part in analytics
o	Laid off due to COVID
•	Taking offer in shopify which is Canadian company for DS
•	Figure out where business will be affected and how the rebound will start
o	There were an uptick in flights when pandemic hit then steep drop
o	Companies made deep cuts intentionally that were more planned
o	Tripadvisor is trying to get covid information for customers such as different airline rules
•	Businesses are being more picky for hiring
o	However data scientists are applicable everywhere so you can find a job
•	Stuff you could do
o	Kaggle competitions and talk about tackling business problems
o	People who have experience outside of class
o	At larger tech companies – analytical thinking data science and ML
•	Interviews
o	Varies, but challenge you and interview on DS coding and ML techniques
o	Can you code?
o	Critical thinking and tackle business problems
o	Some actually see if you are a good fit and can work with a team
•	Going straight to grad school
o	Helps on paper but does it really make a difference not really unless you go to quantitative PhD which helps. Master’s doesn’t really add much except interview
o	Will take experience over higher degree 
•	Parting words
o	Get experience and first job is very important
o	After this it is a lot easier to get a job
o	The first job doesn’t have to be amazing but as long as you learn a lot from it

