# Churn-Modeling
We will understand what is mean by  customer churn and different approach we can use for churn modeling. 

## Lets understand the conepts for churn modeling and analysis
Customer churn is a serious problem in the competitive world. Almost very organization face this issue of customer churn. Best way to reduce the churn is by identifying the customers who may churn and then take some action to retain the customer and keep them loyal and happy.  Customer churn analysis is important part of customer analysis and we have various frame work available for the same. One of the most popular frame-work for customer analysis is given by Forrester.

## What is Forrester customer analytics framework?
The scale and diversity of customer data provide rich new sources of insight, letting firms engage with customers in new ways and enable the digital disruption of entire industries. This will help us to understand customer and provide better understanding and insights. Forrester Research Inc. has provided with reference model called Forrester customer analytics model and Framework, which can be used as a reference for developing any solutions for customer analytics.

## 1) Contextual Marketing: 
Customers are everything to any organization but there is very rare chance that customer will approach you first. In the completive world the most important part is to target best clients who will get engage with us in near future. 
Contextual marketing refers to online and mobile marketing that provides targeted advertising based upon user information, such as the search terms they’re using or recent web-browsing activity (See also Computational Marketing).The goal is to present ads to customers representing products and services they are already interested in. For example, a customer performs an Internet search for cars and fuel efficiency. Afterwards, they check their daily news website and the ads which show up alongside of news includes for hybrid cars. The customer, already thinking about saving fuel on their commute, clicks on the ad to check out the latest hybrids.
## 2) Acquisition and retention:
Once we get the details of potential customer then the next task is to acquire the customer and get him engage with our products and services. 
Best example will be POC done to our clients. Here we know what they require and now it is our task to acquire those clients by providing them confidence with our product and/or service.
## 3) Retention and loyalty: 
Customer retention refers to the activities and actions companies and organizations take to reduce the number of customer defections. The goal of customer retention programs is to help companies retain as many customers as possible, often through customer loyalty and brand loyalty initiatives.
## 4) Personalization:
This involves generation of recommendation in which customer will be interested in, identifying the best possible action to make business from the customer along with keeping customer happy. 
## 5) Customer Experience:
Customer experience is most important for the business. When customer has good experience they remain loyal and are retained with the business. We can understand customer experience by understanding customer engagement with the organization, satisfaction with the requirement fulfilled also by understanding the journey from the start of service.      

## Current Problem Statement:
There is a US based telecom company who face a problem with customer churn we need to make a predictive model so that company knows about the customers who will churn in near future so that they can take active steps for customer retention. 

Data Set Provided Overview:
Company keeps track of following data and which I reflected in the data set provided.
•	State: They are state code (2 character) representing the state from US.
•	Account length: This represents customer timeline. 
•	Area code: It is to specify the exact location of customer, just like pin-code /postcode. 
•	Phone number: can be used as customer identifier.
•	International plan: It states if the customer as opt for international service plan.
•	Voice mail plan:  It states if the customer as opt for voice mail service plan.
•	Number vmail messages: Total voice-mail send.
•	Total day minutes: Shows total minute spent in call during the day.
•	Total day calls: Total number of calls during the day.
•	Total day charge: Total charge the customer has to pay for all the calls during the day.
•	Total eve minutes: Shows total minute spent in call during the evening.
•	Total eve calls: Total number of calls during the evening.
•	Total eve charge: Total charge the customer has to pay for all the calls during the evening.
•	Total night minutes: Shows total minute spent in call during the night.
•	Total night calls: Total number of calls during the night.
•	Total night charge: Total charge the customer has to pay for all the calls during the night.
•	Total intl minutes: Shows total minute spent in international calls.
•	Total intl calls: Total number of international calls.
•	Total intl charge: Total charge the customer has to pay for all the international calls.
•	Customer service calls:  Calls made to customer service center.
•	Churn: Shows whether the customer has churned or not. 


# Approach for getting solution 
1)	Understand the problem.
2)	Understand the data. 
3)	Discover the relations among data.
4)	Featuring engineering.
5)	Modeling.
6)	Predict the result. 
Understand the problem
Understanding the problem is very important as this helps in taking right step in getting accurate and desired result. The present problem is to identify and predict the customer who may churn in near future. We can do this by using Machine Learning (Classifier Problem).
Understand the data
This is one and most important step while working with discovery phase. This involves understanding of meanings and value of data provided. It also includes clarifying the doubts in data if present. 
In our case we have a clear idea of data provided to us which are already described above.
Discover the relations among data
We gather, analyze relationship among the data. We can use different approach for the same.
1)	Using python libraries such as seaborn, matplotlib, etc.
2)	Visualization tools.
The best approach is to use visualization tools as it reduces the coding and also give better picture of data. We can track the changes in data using UI controllers and filters. This helps in understanding the story.
The data which has the highest relationship (dependency) with the problem are used as Features during the modeling phase.
For the given problem let’s use the visualization and reporting tool Tableau to determine the insights form the data.




## Featuring engineering
Once we know the relationship among the data we work for getting the Features for modeling. Feature engineering is the process of using domain knowledge of the data to create features that make machine learning algorithms work. Feature engineering is fundamental to the application of machine learning, and is both difficult and expensive. The need for manual feature engineering can be obviated by automated feature learning.

A feature is an attribute or property shared by all of the independent units on which analysis or prediction is to be done. Any attribute could be a feature, as long as it is useful to the model. The features in your data are important to the predictive models you use and will influence the results you are going to achieve. The quality and quantity of the features will have great influence on whether the model is good or not.

## General approach for Featuring engineering:
1.	Brainstorming or Testing features
2.	Deciding what features to create
3.	Creating features
4.	Checking how the features work with your model
5.	Improving your features if needed
6.	Go back to brainstorming/creating more features until the work is done.

## Features in our problem are:
•	State 
•	International plan
•	Voice mail plan
•	Number vmail messages
•	Total day minutes
•	Total day calls
•	Total day charge
•	Total eve minutes
•	Total eve calls
•	Total eve charge
•	Total night minutes
•	Total night calls
•	Total night charge
•	Total intl minutes
•	Total intl calls
•	Total intl charge
•	Customer service calls

# Modeling

There are many models available for prediction and classification so we don’t need to make all of our own. In python we have sklearn library which provide almost all the models which we require for machine learning.
For churn modeling following models are mostly used:
1)	Random Forest Classifier
2)	Gradient Boosting Classifier
3)	SVC – Linear SVC
4)	Logistic Regression
5)	Naive Bayes Classifier

# Model Evaluation Basics
The formula for accuracy is: 
### A(M) = (TN+TP)/(TN+TP+FP+FN)
TP is the number of true positives : Predicted as churned and they do
TN is the number of true negatives: Predicted as remaining and they do
FP is the number of false positives: Predicted as they will churn, but they don’t
FN is the number of false negatives: Predicted as won’t churner but they churn

When working with unbalanced dataset we can’t completely depend on Accuracy alone, we need to check the result of other matrix along with accuracy and they are:
•	Sensitivity/Recall - How well the model recalls/identifies those that will leave.
### TP / (TP + FN)
•	Specificity - How well the model identifies those that will stay.
### TN / (TN + FP) 
•	Precision- How believable is the model? A low precision model will alarm you to those who are leaving that are actually staying.
### TP / (TP + FP) 
•	F1 score- This is the harmonic mean between precision and recall or the balance.
### 2 * (precision * recall)/(precision + recall)

# When to use which type of models: Tips and Advice.
There is no fixed approach which can be used for churn modeling. As type of model and its parameters all depend on the Features and relationship of the data.
Mostly used models are 
# Random Forest Classifier:
This model is best in most of the cases as it takes care of model overfitting which make the model bias to trained condition. Also it can easily balance the features by assigning weight to the branches.  Random forest runtimes are quite fast, and they are able to deal with unbalanced and missing data.

Generally use when:

1)	Have missing data 
2)	Training data set size is too large.
3)	 Have unbalance data set 
4)	Overfitting is major concerned.

# Logistic Regression
Logistic regression is used to predict the odds of being a case based on the values of the independent variables (predictors). The odds are defined as the probability that a particular outcome is a case divided by the probability that it is a non-case. This model is best when we can see log graph like pattern in relationship among data.
# Gradient Boosting Classifier
This is also quite efficient as random forest  and takes care of Unbalanced data structure. When the complexity of relationship increased Gradient Boosting Classifier works much better than others.  
# Naive Bayes Classifier
This is a simple classifier and works when the complexity is low with simple dataset. This is suitable for small sized dataset. This model do have issue with overfitting so not much used for real time solutions but all depends on type and structure of the data.   


