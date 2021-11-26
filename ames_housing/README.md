# Project 2: Ames Housing Predictor Model
---

### Executive Summary


Predictors of housing prices can vary from many factors. There are many homeowners who assumes that the older the property, the higher it sells. But to their dismay, they don't get the return on investment especially when selling the older property at it's original state.

A new property agent company is interested to have a model to predict houseprices in Ames and know how they could help homeowners and buyers for better returns with identified features that greatly influence the price. To answer these questions, I fitted different linear regression models to the housing data to determine the features that are most influential on house price.

The goal of this project is to address some of these concerns to, specifically:

1. What are the top 5 features add the most value to a home?
2. Which feature hurt home values most?

### Data Dictionary


I examined a comprehensive housing dataset from the city of Ames in Iowa, USA .Source: [link](https://www.kaggle.com/c/dsi-us-11-project-2-regression-challenge/data)

Below are my added columns to make data more interpretable

|Column Name| Type| Description|
|---: |---:|---:|
remodel_age| int64| the remodel age of property|
property_age| int64| the age of property|
porch_sf|int64| Where porch exist in the property|
garage_cond_area| float64| The overall garage area and condition|

### Conclusions and Recommendation

Lasso regression model had the best predictive performance on housing sale price in Ames USA, and outperformed the other linear models tested. As a regularised regression method, it was able to reveal which features affect sale price the most.

To have a better selling price, homeowners should look at the following based on the results above:
1. Improve overall material and finish quality by repainting and renovating parts of the house to have a new updated look
2. Increase their ground living area as a consideration for renovation works
3. Adding or expanding basement size while improving their quality as well

However, the model was developed using data on houses sold between 2006 - 2010 in Ames, USA. To improve the applicability of the model, one can consider adding in more data from a wider time frame and also other locations to also predict house prices in other states as well
