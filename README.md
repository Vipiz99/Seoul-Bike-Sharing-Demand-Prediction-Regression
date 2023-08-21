# Seoul-Bike-Sharing-Demand-Prediction-Regression

# OBJECTIVE

Developed a regression model using algorithms such as Random Forest and XGBoost to predict the hourly demand of bikes.Performed hyperparameter tuning techniques and achieved R2 score of 92% using XGBoost model and reduced the public waiting time significantly.

# DATASET
**Date** - shows the date in 'year-month-day' format

**Rented Bike count** - Count of bikes rented at each hour

**Hour** - Hour of he day

**Temperature** - Temperature in Celsius

**Humidity** - humidity in %

**Windspeed** - windspeed in m/s

**Visibility** - level of visibility 10m

**Dew point temperature** - dew point temp. in Celsius

**Solar radiation** - solar radiation in MJ/m2

**Rainfall** - measurement of rainfall mm

**Snowfall** - measurement of cm

**Seasons** - Winter, Spring, Summer, Autumn

**Holiday** - Holiday/No holiday

**Functional Day** - NoFunc(Non Functional Hours), Fun(Functional hours)


# Feature Manipulation & Selection
I convert the "date" column into 3 different column i.e "year","month","day". The "year" column in our data set is basically contain the 2 unique number contains the details of from 2017 december to 2018 november so if i consider this is a one year then we don't need the "year" column so we drop it. The other column "day", it contains the details about the each day of the month, for our relevence we don't need each day of each month data but we need the data about, if a day is a weekday or a weekend so we convert it into this format and drop the "day" column.

# Random Forest Regression
Regression is the other task performed by a random forest algorithm. A random forest regression follows the concept of simple regression. Values of dependent (features) and independent variables are passed in the random forest model.

In a random forest regression, each tree produces a specific prediction. The mean prediction of the individual trees is the output of the regression. This is contrary to random forest classification, whose output is determined by the mode of the decision trees’ class.

Although random forest regression and linear regression follow the same concept, they differ in terms of functions. The function of linear regression is y=bx + c, where y is the dependent variable, x is the independent variable, b is the estimation parameter, and c is a constant. The function of a complex random forest regression is like a blackbox.

Screenshot (30)



# CONCLUSION
1. Hour of the day holds most importance among all the features for prediction of dataset

2. It is observed that highest number bike rentals counts in Autumn/fall Summer Seasons and the lowest in Spring season.

3. We observed that the highest number of bike rentals on a clear day and the lowest on a snowy or rainy day

4. As we can see the top 5 important features of our dataset are: Season_winter, Temperature, Hour, Season_autumn, Humidity

5. Peoples dont use rented bikes in no functioning day

6. People tend to rent bikes when the temperature is between -5 to 25 degrees
7. People tend to rent bikes when the visibility is between 300 to 1700
8. For all the above experiments we can conclude that gradient boosting and random forest regressor with using hyperparameters we got the best results
