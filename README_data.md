#DATA SUBMISSION

The dataset I am using for my project is the "Credit Card Fraud Detection" dataset from Kaggle.
This dataset contains transactions made with credit cards in September 2013 by European cardholders. 
It presents the transactions made in two days, where there are 492 cases of fraud out of 284,807 total transactions.

There are 31 features.
Time: The number of seconds elapsed between the current transaction and the next transaction in the dataset.
V1-V28: The principal components obtained with PCA (the creators of the dataset can not reveal the original features due to confidentiality)
Amount: The transaction amount
Class: The response variable. Is a 1 in case of fraud and a 0 otherwise.

This dataset can be used to train or improve a model that can detect fraud. This is helpful because when fraud is detected, a bank can temporarily put a hold on the card to prevent further charges, and reach out to contact the cardholder.

One engineering problem I would like to solve with this dataset is the implementation of a cost-sensitive decision threshold. A standard classifier would treat a missed $5 charge the same as a $5,000 charge. Implementing a cost-sensitive decision threshold would cause the model to basically treat higher amounts as a "bigger deal". This is an engineering problem because while a false negative might cost the bank a certain amount, a false positive could lead to consquences like irritated customers and call-center overhead. With a cost-sensitive decision threshold, our goal shifts from purely detecting fraud as accurately as possible to costing the bank less money in the long run. 

Another engineering problem I would like to solve is the issue with the extreme class imbalance in this dataset. The cases of fraud make up only around 0.2% of transactions in this dataset. A classifier that only guesses "no fraud" will have a 99.8% success rate, while catching none of the actual fraud. This means that a standard accuracy metric will be useless for our model. This is an engineering problem because it requires the use of other metrics to determine how good our model truly is. 

In order to obtain this dataset, go to https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud/data
From there, you can download the creditcard.csv file.

The dataset has been collected and analysed during a research collaboration of Worldline and the Machine Learning Group (http://mlg.ulb.ac.be) of ULB (Université Libre de Bruxelles) on big data mining and fraud detection.
