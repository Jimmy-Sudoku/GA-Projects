# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Required core features for the next development project.

## Project Description

The project was built as part of General Assembly's requirement to pass the course. The project aims to find out what is required core features for the next development project to increase the sales price. To do that, my team has cleaned the data, analyze the features, trained the model till a scoreof 84%. 

---

## Table Content

- [Background](#Background)
- [Problem Statement](#Problem-Statement)
- [Assumptions](#Assumptions)
- [Data Import,Cleaning and EDA](#Data-Import,-Cleaning-and-EDA)
- [Preprocessing & Modeling](#Preprocessing-&-Modeling)
- [Conclusions & Recommendations](#Conclusions-&-Recommendations)

---

## Background

Real Sky Estate Development has been developing residential areas around Ames and is looking to procure and develop new housing in the area. 

Previous housing developments were not returning favorable profits due to the recent pandemic and political tensions. It also caused a rise in the costs of living and building materials over the years.

Facing a forecasted recession in the upcoming year, Real Sky senior management team has reached out to our data science team to pinpoint factors that will direct towards revamping the company’s focus structure to improve the attractiveness and sales price of new housing developments.  

---

## Problem Statement

To find out which core features to focus on to increase a house’s sale price for our next development project using Linear, Ridge and Lasso model. 

---

## Assumptions

The following are the assumptions made:
- Only features with metrics correlation >0.3 with reference to sale price are considered for the analysis
- Time constraint for the project
- Only select features with less than 5% missing data
- Missing data are replaced with median values of the features ([*source*](https://www.mastersindatascience.org/learning/how-to-deal-with-missing-data/)) 

---

## Data Import & Cleaning

#### Datasets

There are 2 datasets are used. The below are the 2 datasets :

* [`Train.csv`](./data/Train.csv): Train score for model
* [`Test.csv`](./data/Test.csv): Test score for model

The below are the steps that was done for data import and cleaning:
- create functions for cleaning;
- import libraries such as pandas, numpy, matplotlib.pyplot, shapy, sklearn , Image, warnings, scipy and seaborn;
- cleaning the data such as converting dictionary to dataframe, remove duplicates, check and remove missing values, convert values format into suitable format, convert ordinal to values, replace missing values with median,rename headings and remove data not used for analysis;

#### Data dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**saleprice**|int64|Train|The sale price of the house.| 
|**garage area**|int64|Train & Test|The size of garage in square feet.| 
|**gr liv area**|int64|Train & Test|Above grade (ground) living area square feet.| 
|**total bsmt sf**|int64|Train & Test|Total square feet of basement area.| 
|**bsmt qual**|int64|Train & Test|Evaluates the height of the basement.| 
|**exter qual**|int64|Train & Test|Evaluates the quality of the material on the exterior.| 
|**overall qual**|int64|Train & Test|Rates the overall material and finish of the house.| 
|**year built**|int64|Train & Test|Construction date.| 
|**year remod/add**|int64|Train & Test|Remodel date.| 
|**mas vnr area**|int64|Train & Test|Masonry veneer area in square feet.| 
|**bsmt exposure**|int64|Train & Test|The walkout or garden level walls.| 
|**full bath**|int64|Train & Test|Full bathrooms above grade.| 
|**totrms abvgrd**|int64|Train & Test|Total rooms above grade.| 
|**fireplaces**|int64|Train & Test|The number of fireplaces.| 
|**wood deck sf**|int64|Train & Test|Wood deck area in square feet.| 
|**open porch sf**|int64|Train & Test|Open porch area in square feet.| 

---

## Exploratory Data Analysis

From the Data Analysis, I have found out the top 3 core features that contributed to the sales prices are :
- overall qual 
- exter qual                    
- gr liv area

---

## Data Visualization

The following are the visualization done:
- Triangle Heatmap
- Triangle Pair Gird
- Histogram
- Boxplot
- Bar plot
- Variable Importance Plot
- Shapley value plot

---

## Conclusions & Recommendations

The key takeaway :
1. Ridge model has a 84% Score;
2. Identified 3 top core features which are ground living area, overall quality and external quality

Therefore, I recommend that we can have a greater budget allocations and maketing on the 3 core features improve the sales price of the new housing development.

In the future, I hope that I can implement features such as forcasting sales price using of machine learning.

---