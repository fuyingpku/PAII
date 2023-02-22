# PAII
Practical Application Assignment 11.1: What Drives the Price of a Car?
What drives the price of a car? Github code: https://github.com/fuyingpku/PAII/blob/b05fb42dbe12a30e917589212f450b0b70231aef/prompt_II-checkpoint.ipynb

#OVERVIEW

In this application, you will explore a dataset from kaggle. The original dataset contained information on 3 million used cars. The provided dataset contains information on 426K cars to ensure speed of processing. Your goal is to understand what factors make a car more or less expensive. As a result of your analysis, you should provide clear recommendations to your client -- a used car dealership -- as to what consumers value in a used car.

#CRISP-DM Framework
To frame the task, throughout our practical applications we will refer back to a standard process in industry for data projects called CRISP-DM. This process provides a framework for working through a data problem. Your first step in this application will be to read through a brief overview of CRISP-DM here. After reading the overview, answer the questions below.

#Business Understanding
From a business perspective, we are tasked with identifying key drivers for used car prices. In the CRISP-DM overview, we are asked to convert this business framing to a data problem definition. Using a few sentences, reframe the task as a data task with the appropriate technical vocabulary.

#Determine Business Objectives
(1) Background: The provided dataset contains information on 426K cars including features and price/value.

(2) Business Objectives: The goal is to understand what factors/features make a car more or less expensive.

(3) Business Success Criteria: As a result of this model based analysis, the model should provide clear recommendations to the client what consumers value in a used car and we can provide a clear indication about the estimated price

#Assess Situation
(1) Inventory of Resources: class chat in module 11, python and modeling, and other previous trainings in this course.

(2) Requirements, Assumptions, and Constraints: this is a practice work due Feb 28th, no legal issue with data usage. The assumptions are good data collection in the public database. Due to the limiation of CPU power, a fration of the whole dataset (containing 3 million cars) was used.

(3) Risks and Contingencies terminology: The success may rely on good analysis skillset of the performer in this case.

(4) Costs and Benefits: It is a good business model which could be used for car resale companies across the world.

#Determine Data Mining Goals
（1） Data Mining Goals：Predict the price range that a seller willing to sell and a buyer willing to buy, and calcualte the business model about the gap between the buying price and sale price as revenue for the car.

（2） Data Mining Success Criteria：MSE or error rate when using trained model to predict the price of sale to untrained dataset.

#Produce Project Plan
（1） Project Plan：the CRISP-DM standard protocol will be carried out, in total, 16 hrs for data understanding/preparation/modeling/evaluation/deployment

（2） Initial Assessment of Tools and Techniques：linear regression

# Evaluate results: first of all, the model build in this case is a very universal model, with very limited input of data (year, transmission, odometer), the predicted price can narrow down to 10K USD as error rate
 The challenges is that due to the limit of computation power, the dataset is only a portion of the whole dataset (8-fold more in terms of size)
 Future directions: AI based model will do a much better work than linear regression 

# Access of data mining results with respect to business success creteria:
 In principle, a business is based on the consistency of the model, which is shown not overfitting in this case, the model(s) build here provided the inital analysis of the price which address the business quesiton of predicting price with limited input of data
Business Objectives: The goal is to understand what factors/features make a car more or less expensive, from the model and its coef, we can see the strongest to weakest correlation as predicted in permutaiton analysis: odometer>year>transmission
Business Success Criteria is met: As a result of this model based analysis, the model should provide clear recommendations to the client what consumers value in a used car and we can provide a clear indication about the estimated price. For example: as shown before,let us try some selected conditios like 10000 miles, 2000 yr made, automatic car worth how much (ca. 3k USD), and it is higher than older, more milage car
With this model, it is feasbile to put in any future features and give a predicted value of the car

Review process: in summary, the whole process start with overview of all the features in the dataset, remove outliers and Nan values, using graphic and correlation function to identify what are the factors contribute/correlate the price of the car. During the analysis, it is noticed the although the model and maker also could contribute a lot of the price, it is feasible that these two features could be looked into when building a newer model with larger dataset. We used the correct attributes with correct model, but we admit there is still room to improve with a much larger dataset. 

#Plan deployment: it is a general procedure used to identify and create the model in this case. all the parameters were fixed for any repeat needed. The model itself is ready for deployment and for sure training and interface could be employed for the customers 

#Produce final report: In this project, we screened all the features, based on the avaiablity of the dataset, we narrow down factors: 'region', 'year',  'manufacturer', 'model', 'fuel', 'odometer', 'title_status','transmission', 'state'. Further correlation analysis narrown down the list to three major factors: odometer, year, and transmission. In the regression analysis, it is found that the impact sequence to price from strongest to weakest is odometer>year>transmission. The lasso model is provided to predict the price. 

#Review project: The initial analysis and data prep went well. However, the model (linear regression) gives a large MSE, with 10K difference on avarage between predicted value to test value. That could be improved with better model e.g. AI based model and larger dataset with more features could be selected. A group discussion could be beneficial across the class.



