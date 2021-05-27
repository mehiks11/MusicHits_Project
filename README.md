# Predicting the Peak Rank of Songs on Billboard Hot 100

## Abstract
The goal of this project was to use billboard data combined with data from the most popular subscription music streaming service to predict the peak ranking a song would reach on billboard given a select number of features. After building and comparing multiple models, there are a select few features from the original datasets that provide a decent prediction about the peak a song may reach in a given week. 

## Design
This project pulls its data via webscraping from [Billboard's Top 100 Charts](https://www.billboard.com/charts/hot-100) and using spotify's web API tool. Using correlative features from these two data sets, the linear model can help better predict the ability of a song to reach higher peaks and provide some guidance to record labels, investors, and musicians seeking to have a top hit. 

## Data
The dataset contains 2761 data points with 16 features for each, 5 of which were selected, and 3 of which were engineered for final model building purposes. Some of the most useful features were those that had to do with the artist, including artist popularity and followers on spotify. A baseline model was created using just the five selected features: danceability, artist popularity, artist followers, number of weeks on the charts, and song mode.


## Algorithms

*Feature Engineering*
*  The first model modifications made post creating a baseline included ones with engineered features. These are the features originally tested, with those who did not improve model R2 scores being thrown out.
   * polynomial features:
      1. popularity squared *
      2. followers squared *
      3. number of weeks on charts squared *
      4. danceability squared 
   * interaction terms:
      1. popularity and followers multiplied
      3. popularity and followers divided
      4. followers X danceability
      5. danceability X popularity 

*Models*
The target variable was logged from the start because it had a skewed distribution. A feature engineered model was selected including all thee of the starred features above. All three were selected as they provided the highest R2 values on validation data, scores that were higher scores from the training data. 
Further, lasso and ridge models were created for both the baseline model and the engineered model to test for overfitting, with the best alpha found using CV. 

  

*Model Evaluation and Selection*
Ultimately, the 6 chosen models were compared using cross validation and the means were compared, and found the feature engineered model to be the best model. The cross validation occured on validation data + training data, split into 5 folds. 


## Final coefficients:
* Intercept: 4.222894599606599
* Danceability:-9.18010339e-01
* Popularity:2.66326807e-02
* Followers:-4.04140264e-08
* Num_wks:-1.06595401e-01
* Mode:1.71709497e-01
* Popularity Squared:-2.09622088e-04
* Followers Squared:3.23195872e-16
* Num_Wks Squared: 7.87829545e-04

## Tools
- Numpy and Pandas for data manipulation
- Scikit-learn for modeling
- Seaborn for plotting
- Spotify API
- Beautiful Soup/Selenium for Webscraping

## Communication
In addition to the presentation provided on my github, I plan to create a visual for my website when it is posted. 
