# StarbucksCapstoneChallenge


## Project Overview

The dataset provided by Starbucks for Udacity Data Scientist Nanodegree Capstone challenge data set is a simulation of how people make purchasing decisions and how those decisions are influenced by promotional offers on a mobile application.

With the data provided and the skills aquired during the course this project aims to use Data Science to give Insights about user behavior.

I choose to follow 3 classic simple steps on project workbook, first step is to clean the data we use, next step is the Visual Data Exploration and finally data modeling/machine learning.

In the end we sucessfully trained a RandomForestClassifier model with optimized hyperparameters with RandomSearch and also got a 71.52% accuracy metric which will certainly give the analysts some insight about the sucess of an offer before it is sent.

link to medium post: https://gletsongirao.medium.com/starbucks-capstone-challenge-bb715ca03e40


## Datasets

The data is contained in three files:

* portfolio.json - containing offer ids and meta data about each offer (duration, type, etc.)
* profile.json - demographic data for each customer
* transcript.json - records for transactions, offers received, offers viewed, and offers completed

Here is the schema and explanation of each variable in the files:

**portfolio.json**
* id (string) - offer id
* offer_type (string) - type of offer ie BOGO, discount, informational
* difficulty (int) - minimum required spend to complete an offer
* reward (int) - reward given for completing an offer
* duration (int) - time for offer to be open, in days
* channels (list of strings)

**profile.json**
* age (int) - age of the customer 
* became_member_on (int) - date when customer created an app account
* gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)
* id (str) - customer id
* income (float) - customer's income

**transcript.json**
* event (str) - record description (ie transaction, offer received, offer viewed, etc.)
* person (str) - customer id
* time (int) - time in hours since start of test. The data begins at time t=0
* value - (dict of strings) - either an offer id or transaction amount depending on the record

  
## Problem Statement 

We want to use the data to identify which groups of people are most responsive to each type of offer, and how best to present each type of offer.

For this we set a classification problem where we want to identify if a uffer will be sucessfull based on user characteristics

Classification problem where we out goal is to predict if a offer will be completed by a user based on user characteristics.


## Metrics 

As it is a classification problem we will use a Accuracy to measure how well a model correctly predicts whether an offer is successful.
	
## Python Libraries Used
-[Python Data Analysis Library](https://pandas.pydata.org/)  
-[Numpy](http://www.numpy.org/)  
-[Matplotlib](https://matplotlib.org/)  
-[seaborn: Statistical Data Visualization](https://seaborn.pydata.org/)  
-[scikit-learn: Machine Learning in Python](https://scikit-learn.org/stable/)  

## Acknowledgements

Udacity mentors for the always helpful insights in the reviews, Starbucks for providing this dataset.


### File structure of project:

1.  ../data - folder for 3 json archives with the data

    ../data/portfolio.json - data containing offer ids and meta data about each offer (duration, type, etc.)
    
    ../data/profile.json - demographic data for each customer

    ../data/transcript.json - records for transactions, offers received, offers viewed, and offers completed

    

2.  ../Starbucks_Capstone_notebook.ipynb - jupyter notebook containing all our project coding.

    

3.  README.md

    ../models/train_classifier.py - model training script
    
    ../models/classifier.pkl - saved model when running `python train_classifier.py`




  
