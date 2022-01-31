# Summary

* [1. Installation] 
* [2. Project Motivation] 
* [3. File descriptions] 
* [4. How To Interact With The Project]

This is the link to the Medium article:
https://medium.com/p/9d6343ee720d/

# 1. Installation

In order to execute this project, the following libraries were used

* Numpy library
* Pandas library
* Python version 3.8.5
* math
* json
* seaborn
* matplotlib
* sklearn

# 2. Project Motivation

This project presents a Machine Learning (ML) model that predicts whether or not a customer will respond to an offer with more that 92% of accuracy. 

The model was trained with data that simulates how people make purchasing decisions and how those decisions are influenced by promotional offers.

The data register the events produced by customers: receiving offers, viewing offers, completed offers and the transactions they do through the business.

The data have three types of offers: buy-one-get-one (BOGO), discount, and informational:

* BOGO: the user have to spend a certain amount of money to get a reward equal to that amount.
* Discount:  a user gets a reward from a certain fraction of the money she spent. 
* Informational: there is no reward.

The project applies the ML algorithm Random Forest Regressor to perform binary classification: 1- the customer viewed and completed the offer and 0- the customer viewed the offer but she didn't completed it.

# 3. File descriptions

retail_industry/

├── README.md

├── data/
    portfolio.json
    profile.json
    transcript.json

├── ML_model_retail_industry.ipynb

├── Other.ipynb

├── images/

# 4. How to interact with the project

The data is contained in three files:

    portfolio.json - containing offer ids and meta data about each offer (duration, type, etc.)
    profile.json - demographic data for each customer
    transcript.json - records for transactions, offers received, offers viewed, and offers completed

Here is the schema and explanation of each variable in the files:

portfolio.json

    id (string) - offer id
    offer_type (string) - type of offer ie BOGO, discount, informational
    difficulty (int) - minimum required spend to complete an offer
    reward (int) - reward given for completing an offer
    duration (int) - time for offer to be open, in days
    channels (list of strings)

profile.json

    age (int) - age of the customer
    became_member_on (int) - date when customer created an app account
    gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)
    id (str) - customer id
    income (float) - customer's income

transcript.json

    event (str) - record description (ie transaction, offer received, offer viewed, etc.)
    person (str) - customer id
    time (int) - time in hours since start of test. The data begins at time t=0
    value - (dict of strings) - either an offer id or transaction amount depending on the record

This is the link to open the Medium article:
https://medium.com/p/9d6343ee720d/

# References

Udacity: Data Scientist Nanodegree

Random Forest GridSearchCV: https://towardsdatascience.com/hyperparameter-tuning-the-random-forest-in-python-using-scikit-learn-28d2aa77dd74
