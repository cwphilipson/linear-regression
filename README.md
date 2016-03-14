# linear-regression
Linear regression is used as a supervised learning algorithm to predict outcomes in baseball, basketball and wine prices

# Summary
Three separate analyses are performed herein: __Moneyball__, __NBA Playoff Predictions__, and __Wine Price Prediction__. Each analysis uses data to train a linear regression model and identify key features for building a predictive model. Data and scripts are described below. These projects were created as a part of the EdX MIT 15071x "The Analytics Edge" course.  

## Moneyball
In the Moneyball year (2002), the distribution of Major League Baseball team salaries was directly correlated to winnings. Paul DePodesta devised a sabermetric-based evaluation to assemble a competitive team for The Oakland Athletics' (the A's), and predict how to get to _and_ win the world series. This project uses linear regression models to recreate Moneyball predictions.  
### Data
baseball.csv (1233 rows,  15 columns)  
Features: Team, League, Year, RS (runs scored), RA (runs allowed), W (wins), OBP (on base percentage), SLG (slugging percentage), BA (batting average), Playoffs, RankSeason, RankPlayoffs, G, OOBP (opponent on base percentage), OSLG (opponent slugging percentage)  
### Scripts
Linear_Regression_Moneyball.Rmd  
The code performs the following steps:  
1.  Read in baseball dataset and subset only Moneyball years (<2002)  
2.  Compute run differene and verify linear relationship between winning and nun difference  
3.  Build regression model to predict wins based on run difference for past and future seasons  
4.  Build regression model to predict runs scored for past and future seasons  
5.  Compare predictions with actual turnout for 2002  
One html output file is generated from the R markdown script that includes all linear regression models and data plots.  
  
  
## NBA PLayoff Predictions
This analysis investigates archived NBA data in order to make the following predictions about a team making it to the playoffs.  
### Data
NBA_train.csv  
NBA_test.csv  
Features used: PTS (points scored), oppPTS (opponent scoring), FG (successful field goals), X2P (two pointers), X3P (three pointers), and A at the end of any feature name indicates means attempted 
### Scripts
LinearRegression_NBA.Rmd  
The code performs the following steps:  
1.  Import training dataset  
2.  Compute point difference and check for linear relationship between points and wins  
3.  Build linear regression model to predict wins  
4.  Build linear regression model to predict points scored  
5.  Optimize models based on significant variables  
6.  Import testing dataset  
7.  Make predictions on test data set  
8.  Summarize model's predictive power using out-of-sample R^2  
  
  
## Wine Price Prediction
Future wine prices are predicted based on data rather than expert tasting.  
### Data
wine.csv  
wine_test.csv  
Features: AGST(average growing season temperature), HarvestRain, Year (age of wine), WinterRain, Age, FrancePop (population of France) 
### Scripts
LinearRegression_Wine.Rmd  
The script performs the following steps:  
1.  Import all data  
2.  Construct one-variable, two-variable, and multiple-variable linear regression models  
3.  Calculate the sum of squared errors from each model ("SSE") 
4.  Optimize the multiple-variable model based on coefficients  
5.  Assess how well the model performs on new data (wine_test.csv)  
