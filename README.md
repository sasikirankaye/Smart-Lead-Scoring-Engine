# Smart-Lead-Scoring-Engine


A D2C startup develops products using cutting edge technologies like Web 3.0. Over the past few months, the company has started multiple marketing campaigns offline and digital both. As a result, the users have started showing interest in the product on the website. These users with intent to buy product(s) are generally known as leads (Potential Customers). 

Leads are captured in 2 ways - Directly and Indirectly. 

Direct leads are captured via forms embedded in the website while indirect leads are captured based on certain activity of a user on the platform such as time spent on the website, number of user sessions, etc.

Now, the marketing & sales team wants to identify the leads who are more likely to buy the product so that the sales team can manage their bandwidth efficiently by targeting these potential leads and increase the sales in a shorter span of time.

Problem Statement

To predict the propensity to buy a product based on the user's past activities and user level information.

## Important insights
### Products_purchased

<img src="https://github.com/sasikirankaye/Smart-Lead-Scoring-Engine/blob/main/Images/Products_purchased.png">
The "0" class category products are considerably high

### Year

<img src="https://github.com/sasikirankaye/Smart-Lead-Scoring-Engine/blob/main/Images/Year.png">
The sales in the year 2020 and 2021 are more than 50% compared to overall sales

### month

<img src="https://github.com/sasikirankaye/Smart-Lead-Scoring-Engine/blob/main/Images/month.png">
The sales are almost equal in all the months

### day

<img src="https://github.com/sasikirankaye/Smart-Lead-Scoring-Engine/blob/main/Images/day.png">
There is no useful insight from the day feature

# Predictive Modelling results
In order to find a decent model to predict sales we performed an extensive search of various machine learning models available in Python. In the end, however, models from the h2o package yielded the best results for this task. In particular, deep learning neural networks h2o.deeplearning and gradient boosting regression trees h2o.gbm performed particularly well. An ensemble of various such models, constructed in h2oEnsemble. Here, we used only the 12 most important predictors to avoid over-fitting. To include some features we may have missed with this rather small subset of predictors we supplemented the ensemble with a deep learning neural net using 12 predictors.

|model_id	|F1_Score  |
| ------------- |
|LogisticRegression|	0.731 |
|Ridge Classifier	|0.70|
|knn|	0.54757|
|Support Vector Machine (SVM)|	0.63|
|Bagged Decision Trees (Bagging)	|0.71|
|Stochastic Gradient Boosting|	0.77|
