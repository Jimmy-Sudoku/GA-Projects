# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) GA Capstone Project: CryptoCurrency(Ethereum) Fraud Detection

## Summary

The project was built as part of General Assembly's requirement to pass the course. The project aims to detect fraud in Ethereum cryptocurrency. 
Cryptocurrency is digital coins and tokens that has real-world value. One of the difference between cryptocurrency and physical currency is that cryptocurrency does not rely on a central issuer, such as government or bank, where as physcial currency requires a issuer.

There has been an increase in fraud cases and are on the rise. In 2021 alone, there has been over 10 billion USD lost due to fraud cases. This amount is equavilent to 15  Air Force One, the world's most expensive private jet ([source](https://luxe.digital/lifestyle/travel/most-expensive-private-jets/#Air-Force-One)) or 2 Buckingham Palaces , the world's most expensive and biggest house ([source](https://luxe.digital/lifestyle/home/most-expensive-houses/#:~:text=The%20most%20expensive%20house%20in%20the%20world%20and%20the%20world's,fancy%20houses%20and%20luxury%20mansions.)).

Therefore, it is vital to detect fraud transaction in cryptocurrency, which is the focus for this project.

Based on the analysis done, the following are the findings:
1. 19 features/factors to determine fraud transactions, which is a reduction of features/factors by 62%
2. Model can detect fraud with around 97% recall score
3. Most of the fraud cases occurs uses famous crypto names to mislead people
4. 22% of the transactions are fraud.

With these findings, it is recommended to blacklist token names that uses famous crypto names and use the model to detect fraud transactions.

---

## Acknowledgment

First, I would like to express my deepest graditiude to Singapore DSI (Data Science Immersive) 33 Teaching Instructor, Kishan, and Teaching Assistants, Ryan Chang and Fung Xue Feng for their guidance, enthusiastic encouragement and useful critiques of this project. Special mention to Ryan Chang who has provided speedy response despite having a small amount of free time and has never failed to patiently assist me whenever I needs help throughout the DSI course and projects. I am immensely appreciative for that.

Secondly, I would like to exend my gradtitude to the internet community for their help in providing me free solutions, guidances and knowledge whenever I facing code difficulties due to my limited skills and the ways to go about certain bugs and gitches for the software. I am very appreciative to these internet communities: google, youtube, stack overflow, github, towards data science, kaggle, codewars, leetcode, and open-source softwares such as python, python libraries and jupyter notebook.

Lastly, I would like to thank my family, friends and coursemates for their encouragement and support throughout this course and capstone project at General Assembly.

The project will not have been completed without their unwavering support.

---

## Table Content
- [Summary](#Summary)
- [Acknowledgment](#Acknowledgment)
- [Introduction](#Introduction)
- [Problem Statement](#Problem-Statement)
- [Literature Review](#Literature-Review)
- [Assumptions](#Assumptions)
- [Import Libraries](#Import-Libraries)
- [Data Import, Cleaning & Exploratory Data Analysis](#Data-Import,-Cleaning-&-Exploratory-Data-Analysis)
- [Preprocessing, Modeling & Postprocessing](#Preprocessing,-Modeling-&-Postprocessing)
- [Conclusions & Recommendations](#Conclusions-&-Recommendations)

---

## Introduction

Cryptocurrency is digital coins and tokens that has real-world value. One of the difference between cryptocurrency and physical currency is that cryptocurrency does not rely on a central issuer, such as government or bank, where as physcial currency requires a issuer.([source](https://worldcoin.org/articles/why-is-cryptocurrency-important#:~:text=Cryptocurrencies%20are%20digital%20coins%20and,blockchain%20technology%20to%20verify%20ownership.))<br><br>
Other difference include how the ownership is verified. For cryptocurrency, it uses cryptography, public ledgers and blockchain technology for verification. Whereas for physical currency, it uses government or bank. 
<br><br>
One of the main advantages of using cryptocurrency is that some cryptocurrency cannot tampered, where as all physical currency can be tamplered, causing the the physical currency to lose it power.([source](https://worldcoin.org/articles/why-is-cryptocurrency-important#:~:text=Cryptocurrencies%20are%20digital%20coins%20and,blockchain%20technology%20to%20verify%20ownership.)) An example will be in 2020, the fed reserve increase the money supply too rapidly and this result in the rapid rise of inflation ([source](https://news.stanford.edu/2022/09/06/what-causes-inflation/)), causing the price of food and services to increase rapidly ([source](https://www.imf.org/external/pubs/ft/fandd/basics/inflat.htm)).


Another main advantages of using cryptocurrency is that it is scalable and convient as anyone can exchange cryptocurrency without leaving home. This can be very useful and convient, espiecially in places or situations where people do not have access to banks. 
<br>
Because of this advantage, cryptocurrency is on a rise and the total marketcap on its peak is around 3 trillion USD in 2021 ([source](https://coinmarketcap.com/charts/)). 
That is more than 3 times of meta(facebook) marketcap, at 921.93 billion USD ([source](https://companiesmarketcap.com/meta-platforms/marketcap/)),
3 times of tesla marketcap, at 1 trillion USD ([source](https://companiesmarketcap.com/tesla/marketcap/)) 
and more than 7 times the GDP of Singapore.
<br><br>
With such a high marketcap for cryptocurrency, there has been an increase in fraud cases and are on the rise. In 2021 alone, there has been over 10 billion USD lost due to fraud cases. This amount is equavilent to 15  Air Force One, the world's most expensive private jet ([source](https://luxe.digital/lifestyle/travel/most-expensive-private-jets/#Air-Force-One)) or 2 Buckingham Palaces , the world's most expensive and biggest house ([source](https://luxe.digital/lifestyle/home/most-expensive-houses/#:~:text=The%20most%20expensive%20house%20in%20the%20world%20and%20the%20world's,fancy%20houses%20and%20luxury%20mansions.)).

A number of the fraud cases came from one of the second the biggest cryptocurrency marketcap in the market, eth (Ethereum). The reason for that is that eth is used by many defi applications.([source](https://www.cnbc.com/2021/11/19/over-10-billion-lost-to-defi-scams-and-thefts-in-2021.html)).
 Therefore, it is vital to detect fraud transaction in the eth, which is the focus for this project. 
 
The dataset is taken from ([kaggle](https://www.kaggle.com/datasets/vagifa/ethereum-frauddetection-dataset?resource=download)) from a user named, Vagif Aliev, and it will used for this project.
 
---

## Problem Statement

With the increase lost of money due to fraud in eth, as a data scientist working for Ethereum, my team has been tasked by the higher managment to :

- deliver insights on fraud and 
- what are the factors to focus on to detect fraud

This is done so that the implement team can decide on what measures to take to reduce fraud cases. With the reduce in fraud cases, my company hope to reduce the billions of lost money due to fraud.

---

## Literature Review

This is done to find out why certain methods were choosen in this project. 

---

## Assumptions

The following are the assumptions made:
- the price of eth is assumed to be constant
- time constraint in doing this project
- any other factors that are outside the dataset are constant throughout
- this project is a supervised anomaly detection problem
- data has the same distribution ([source](https://towardsdatascience.com/how-to-select-a-data-splitting-method-4cf6bc6991da))
- data collected in the dataset is enough to be a representive ([source](https://towardsdatascience.com/how-to-select-a-data-splitting-method-4cf6bc6991da))
- the labels given in the data are all labelled correct which is why it is a supervised anomaly detection problem.
- when there are enough data, the distribution of the data is standard normal distributed.

---

## Import Libraries

pandas ,seaborn , plt , shap , train_test_split , GridSearchCV , StratifiedKFold , plot_confusion_matrix , classification_report , plot_precision_recall_curve , average_precision_score , recall_score , imbpipeline , SimpleImputer , SMOTE , StandardScaler , LogisticRegression , KNeighborsClassifier , AdaBoostClassifier , XGBClassifier , joblib , Image

---

## Data Import, Cleaning & Exploratory Data Analysis

#### Datasets

There are 1 datasets are used which is ['transaction_dataset.csv'](./00-Dataset/transaction_dataset.csv) : Train, Validation and Test score for model

The below are the steps that was done for data cleaning:
- cleaning the data such as converting dictionary to dataframe, remove duplicates, check and remove missing values, convert values format into suitable format, replace missing values with most frequent ,rename headings and remove data not used for analysis;

#### Data dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**time diff between first and last (mins)**|float64|Train & Validation & Test|The time difference between the first and last transaction.| 
|**avg min between received tnx**|float64|Train & Validation & Test|Average time between received transactions for account in minutes.| 
|**received tnx**|int64|Train & Validation & Test|Total number of received normal transactions.| 
|**sent tnx**|int64|Train & Validation & Test|Total number of sent normal transactions.| 
|**unique sent to addresses**|int64|Train & Validation & Test|Total Unique addresses from which account sent transactions.| 
|**unique received from addresses**|int64|Train & Validation & Test|Total Unique addresses from which account received transactions.| 
|**avg min between sent tnx**|float64|Train & Validation & Test|Average time between sent transactions for account in minutes.| 
|**total erc20 tnxs**|float64|Train & Validation & Test|Total number of ERC20 token transfer transactions.| 
|**min value received**|float64|Train & Validation & Test|Minimum value in Ether ever received.| 
|**erc20 uniq sent addr**|float64|Train & Validation & Test|Number of ERC20 token transactions sent to Unique account addresses.| 
|**erc20 uniq rec contract addr**|float64|Train & Validation & Test|Number of ERC20token transactions received from Unique contract addresses.| 
|**erc20 uniq rec addr**|float64|Train & Validation & Test|Number of ERC20 token transactions received from Unique addresses.| 
|**avg val received**|float64|Train & Validation & Test|Average value in Ether ever received.| 
|**erc20 total ether received**|float64|Train & Validation & Test|Total ERC20 token received transactions in Ether.| 
|**total ether balance**|float64|Train & Validation & Test|Total Ether Balance following enacted transactions.| 
|**min val sent**|float64|Train & Validation & Test|Minimum value of Ether ever sent.| 
|**erc20 uniq sent token name**|float64|Train & Validation & Test|Number of Unique ERC20 tokens transferred.| 
|**erc20 min val rec**|float64|Train & Validation & Test|Minimum value in Ether received from ERC20 token transactions for account.| 
|**erc20 total ether sent**|float64|Train & Validation & Test|Total ERC20token sent transactions in Ether.| 
|**flag**|int64|Train & Validation & Test|Evaluate whether the transaction is fraud or not.| 

#### Exploratory Data Analysis

From the Data Analysis, the following has been found : 

-  22% of the transactions are fraud
-  Most of the fraud cases occurs uses famous crypto names to mislead people

---

## Preprocessing, Modeling & Postprocessing

From preprocessing the following is used :
- Simple Imputer
- Smote
- Standard Scalar

For modeling, the following is used :
- Logistic Regression
- kNN
- Ada
- Xgboost

For postprocessing, the following is used :
- Recall Score
- PR curve
- Classification report
- Confusion matrix

---

## Conclusions & Recommendations

To conclude, the below are the following summary:

1. The best model recall score was around 97%, it is able to detect 196 fraud transactions out of 218 transactions, with a type II error of 22 cases.

2. Fraud transactions consist of 22% of the total transactions ,

3. From the most recorded tokens feature, most of the fraud cases occurs uses famous crypto names to mislead  people who are not familar within the crpyo industry or people who did not do their research well. 

4. Based on machine learning model, there is a total of 19 factors/features that determines fraud transactions.

5. Successfully reducted the importance features/factors by 62% ,which is, from 50 factors/features to 19 factors/features. The purpose is to reduce computational cost and improve efficiency of the model.

With that,the recommendations to reduce eth fraud detection are the following:

1. Blacklist token names that uses famous crypto names

2. Use model to detect fraud

---
