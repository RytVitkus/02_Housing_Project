# Ames, Iowa Housing Modeling - Project 2


## Overview
   - In this project, I was given a set of data for houses in Ames, Iowa and a whole bunch of features (79 to be exact). My goal with this data was to clean it, and then create model that could be used to determine, or at least estimate house prices in Ames from these features.
   - Following the creation of my model, I was then to apply it to a `testing.csv` data set where the SalePrice was unknown and submit it to Kaggle
   - My best model had a RSME of 25,000

## Data
- train.csv (Data that was cleaned, split, and used in regressions)
- test.csv (Testing data, SalePrice was unknown and predicted using the model built on train.csv data)


## Data Dictionary

http://jse.amstat.org/v19n3/decock/DataDocumentation.txt


## Methodology

   1) Data from train.csv had to be loaded and cleaned
   2) This involved removing some extra characters, cross checking against the source data (some values were incorrect), and creating dummy variables for some qualitative values, and assigning rankings to others. (Poor to Excellent turned into 1-5 for regression purposes)
   3) Following cleaning, multiple models were created and tested to try to better predict house prices.
   4) This began a cycle of tinkering, including returning to EDA if I wanted to add another feature and clean the column, just so I could add it to my model to try to better predict housing price.
   5) Finally, once I was satisfied with the model, I loaded and used test.csv to predict housing prices and submitted to Kaggle.


## Insights

Summarily:

   1) The 'Qual' variables had a strong correlation with SalePrice, and positively impacted
   2) The SF measurements positively impacted SalePrice. Whether it was Garage Area, 1st Flr Area, or Lot Area, each sq ft of 1 was associated with an increase in SalePrice amount.
   3) It was quite useful to turn several columns that were qualitative and object values into numericals values that could be used to help determine SalePrice



## Conclusion/Recommendations

   1) Creating quantitative columns out of `Kitchen Qual`, `Exter Qual`, `Exter Cond`, `Bsmt Qual`, `Bsmt Cond`, and `Heating QC` were definitely helpful in determining the house price.
   2) The Various SF measurements were some of the strongest indicators of the housing price. That is to say, `1st Flr SF`, `Garage Area`, `Bsmt Area`, and `Lot Area` were very important in tightening up the predicted house values
   3)My later model that runs a RidgeRegression does a better job predicting houses in the price range of 50,000 to 300,000 but both my models (LinearRegression & Ridge) tend to undervalue very expensive homes, and in general struggles to predict the home prices of the very high end houses.
   4) `Overall Qual` was the strongest standalone value in terms of correlation with a home. Intuitively it makes sense; the better quality the home, the more expensive it will be.

 Additional items of note:

   1) I would want to look more into some additional values like `Porch` and `Pool QC`, as well as all the `Misc Features` since those items may aid in predicting very expensive homes
   2) I'd definitely want to look more into what effect dummy-ifying the `Neighborhood` value did to my model, and create/test some models that don't incorporate it at all. (With more time that is)
   3) There were other `Area` style measurements I would want to investigate
   4) `Beds` and `Baths` were omitted in my model, and I find that egregious and worthy of adding in and using to look into creating a better model potentially. 
   5) `Lot Shape`, `Housing Style`, `Roof Material`, `Year Built` are additional columns of data I think could impact that value of a home, and would test those on future models

## Presentation Slides:

https://docs.google.com/presentation/d/1gyhZTeg0ZLme3gP6AnxY4zhEhVtjtDDSYQKc4gYhrBc/edit?usp=sharing


```python

```