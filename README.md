# Real Estate Price Predictor

Will Toranto, Kamryn Bendolph, Wil Dotson

## Overview
This project challenged us to create a linear regression model using data from a King County House Sales dataset to predict the price of a home using a combination of different features. Our client, a real estate firm in King County, wants to have a tool that allows their clients to enter information about their home and in return, get a prediction for the sale price of their home. Our job as data scientists, is to create a model that can give an accurate prediction of a home sale price given specific characteristics that we deem important. While cleaning and looking through the data, it became important for us to come up with the most important features that have the biggest impact on a home's value. In addition to realtors, this type of model can be used by any homeowner or potential homeowner who wants to see how much they would have to pay for a home with specific features. This model can take the guesswork out of the homebuying and selling process, making it easier for both parties to come to a deal.

## Data Understanding
To compile our analysis, we used data from a dataframe that includes data from homes that were for sale in King County from 2018-2019. In the dataset, the different characteristics or 'features' are represented in the columns and each row represents the sale of a home. This dataset is perfect for the model that we are creating because it has an abundance of data concerning house sales which is just what we need to make a good predictive model. The dataframe has information for 21,597 home sales in King County with 91 features to describe each one. Needless to say, it is a very thorough dataframe. **insert descriptive statistics**. In our model, we used price as our target variable which means that it was the variable that we were trying to predict. The dataset had a lot of useful features for our model and we used all of them excdept for date and id. Although the datasets included a lot of information on a ton of sales, it was a little limited in that there were null values and/or placeholders in place for characteristics that were not recorded for some features. 

## Data Preperation
As we started to compile of our data and examine it, we realized that the dataset needed to be tweaked in a few places. We decided to clean our data and fill null values and placeholders with values so that we could run our analyses. We dropped columns that did not make sense to have in our model like ID and date. We also created columns that compared data from different columns to get a better sense of the data we were working with. For example, we created a column that returned a boolean (True or False) for whether or not a house had a basement. We also created a column that took the different zipcodes for each house sale, and grouped them by city which gave us a new feature to add to our model. 

## Data Modeling
To model our data, we used linear regressions to display model our baseline and extra models. We made a lot of model iterations to try and get our model at an optimal state. The first iteration we did was getting rid of the outliers in our data that were not within 2 standard deviations away from the mean. Another iteration included the city and basement columns that we made in our data preparation step to see their impact on our prediction score. Our final linear regression model is a log-level linear regression model in which our target variable 'price' was logged. Doing the log transformation reduced the amount of skew in our data which increased our predictive score and decreased our error exponentially. 


## Results
Our final model takes into consideration the most important features in a home that have direct impact on the sale price of that home. Based on trial and error we came up with an optimal model that had an average error of $169,833 and an r-squared value of 0.8391. This means that 83.91% of the data fit our baseline regression model for the testing dataset.



## Conclusions





## For More Information
Please review our full analysis in [our jupyter notebook](./finalnotebook.ipynb) or [our presentation](./Phase_2_Presentation.pptx).

For any additional questions, please contact **Kamryn Bendolph at krbendol@bsc.edu, Wil Dotson at jwdotson@bsc.edu, & Will Toranto at williamtoranto@gmail.com**


## Repository Structure
```
project-folder
    |
    README.md
    data-folder
    images-folder
    notebooks-folder
          |
          report.ipynb
          exploratory-folder
                  |
                  member-1-notebooks-folder
                  member-2-notebooks-folder 
                  member-3-notebooks-folder  
 ```
 