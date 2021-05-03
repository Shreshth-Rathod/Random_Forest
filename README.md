# Restaurant Revenue prediction in R using Random Forest - TidyModels 

# Introduction & Goals
- The goal is to predict the restaurant revenue and submit it on the kaggle leaderboard to get ranked amongst other kagglers.

# Contents

- [The Data Set](#the-data-set)
- [Used Tools](#used-tools)
- [Conclusion](#conclusion)
- [Follow Me On](#follow-me-on)


# The Data Set
- Data Description
  - The data set contains train and test set. 
  - The train set consists of information of 137 restaurants.
  - The test set consists of information of 100000 restaurants of which the revenue has to be predicted.
    - Id : Restaurant id. 
    - Open Date : opening date for a restaurant
    - City : City that the restaurant is in. Note that there are unicode in the names. 
    - City Group: Type of the city. Big cities, or Other. 
    - Type: Type of the restaurant. FC: Food Court, IL: Inline, DT: Drive Thru, MB: Mobile
    - P1, P2 ... P37: There are three categories of these obfuscated data. Demographic data are gathered from third party providers with GIS systems. These include population in any given area, age and gender distribution, development scales. Real estate data mainly relate to the m2 of the location, front facade of the location, car park availability. Commercial data mainly include the existence of points of interest including schools, banks, other QSR operators.
    - Revenue: The revenue column indicates a (transformed) revenue of the restaurant in a given year and is the target of predictive analysis. Please note that the values are transformed so they don't mean real dollar values. 


- The challenges faced were:

  - Train set was much smaller than test set.
  - Overfitting on training set and not getting promising results on validation set.
  - Multiple columns with no names (P - variables), unable to extract exact purpose of these columns.
  
- Approach to overcome the problem:

  - Ran Linear Regression, SVM, Neural Networks but overfitting was still the problem.
  - Parameter tuning the Random Forest made it's way to getting better RMSE values in the prediction.
  - Tried using PCA in order to reduce the dimension of the dataset but were unable to get good results, ended up using all the columns and the model performed well


# Used Tools
- Rstudio was used in model building.
  - Tidymodels and Tidyverse were the main packages used for building and tuning the model.
  
# Conclusion
- Project turned out really well with tuned Random Forest.
- Major things learnt in the project are:
  - Parameter Tuning.
  - How to deal with unknown columns and how to apply & interpret Principal Component Analysis.
  - How to visualise data and wrangle it according the requirements.

- Secured 461 Rank out of ~2260 teams in the private leaderboard.

# Follow Me On
http://linkedin.com/in/shreshthrathod
