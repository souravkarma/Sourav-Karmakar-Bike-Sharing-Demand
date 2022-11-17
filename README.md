# Sourav-Karmakar-Bike-Sharing-Demand
Here I am trying to predict bike sharing demand across various seasons,months and in different times of a day.
# Bike Sharing Demand Prediction

## <b> Abstract: </b>

Bike sharing is a transport service which mainly focuses to lend conventional or electrical bikes to an individual or a group of individuals for an hour, a day or for a month depending on the needs.Using these systems, people are able rent a bike from a one location and return it to a different place on an as-needed basis

In market share we can see that Bike Sharing system has a global market share which was valued around 3.39 billion Dollars in 2019 and is projected to grow to 6.98 Billion Dollars by 2027 with a compound annual growth rate of around 14% indicatively from 2020 to 2027.

Several factors such as low bike rent, increase in capital investments,introduction of e-bikes in the market, technological advancement and government schemes for development of several bike-sharing infrastructure has increased the overall market share and led to the introduction of several opportunities during the forecasted year. However, rise in bike theft and huge initial investment are some of the key factors in order to hinder expected market growth.

Keywords: Bike-Sharing, Data Mining, Predictive Analysis, Linear Regression, Machine Learning.

## **Introduction:**

Bike sharing system demand nowadays is increasing in proportional manners globally. This system has gained a lot of  attention with its cost effective system and easy to use nature. This system has already attracted a huge customer base globally like in South Korea, São Paulo ,China and Australia.
Bike sharing system generally rents bikes on an hour, day and month basis and is generally based on static pricing inclusive of hour,days or month. Because of its affordability and easy renting system anyone can commute on arrival. 
According to our problem our main aim is to build a predictive model so as to find the number of bikes rented based on the given dataset.


## <b> Problem Description: </b>

Currently Rental bikes are introduced in many urban cities for the enhancement of mobility comfort. It is important to make the rental bike available and accessible to the public at the right time as it lessens the waiting time. Eventually, providing the city with a stable supply of rental bikes becomes a major concern. The crucial part is the prediction of bike count required at each hour for the stable supply of rental bikes.

### <b> Data Description: </b>

The dataset contains weather information (Temperature, Humidity, Windspeed, Visibility, Dewpoint, Solar radiation, Snowfall, Rainfall), the number of bikes rented per hour and date information.


#### <b>Attribute Information: </b>

* Date : year-month-day
* Rented Bike count - Count of bikes rented at each hour
* Hour - Hour of he day
* Temperature-Temperature in Celsius
* Humidity - %
* Windspeed - m/s
* Visibility - 10m
* Dew point temperature - Celsius
* Solar radiation - MJ/m2
* Rainfall - mm
* Snowfall - cm
* Seasons - Winter, Spring, Summer, Autumn
* Holiday - Holiday/No holiday
* Functional Day - NoFunc(Non Functional Hours), Fun(Functional hours)

## **Feature Description:**


* Date : Date feature which is str type is needed to convert it into Datetime format DD/MM/YYYY.The new feature extracted from Date are Day, Month and year
* Rented Bike Count : Number of bike rented which is our Dependent variable according to our problem statement which is int type.
* Hour: Hour feature which is in 24 hour format which tells us number bike rented per hour is int type.
* Temperature(°C): Temperature feature which is in celsius scale(°C) is Float type.
* Humidity(%): Feature humidity in air (%) which is int type.
* Wind speed (m/s) : Wind Speed feature which is in (m/s) is float type.
* Visibility (10m): Visibility feature which is in 10m, is int type.
* Dew point temperature(°C): Dew point Temperature in (°C) which tells us temperature at the start of the day is Float type.
* Solar Radiation (MJ/m2): Solar radiation or UV radiation is Float type.
* Rainfall(mm): Rainfall feature in mm which indicates 1 mm of rainfall which is equal to 1 litre of water per metre square is Float type.
* Snowfall (cm): Snowfall in cm is Float type. Seasons: Season, in this feature four seasons are present in data is str type.
* Holiday: whether no holiday or holiday can be retrieved from this feature is str type.
* Functioning Day: Whether the day is Functioning Day or not can be retrieved from this feature is str type.
* Weekend : Weekend extracted from Day 1 when the day is Saturday or Sunday while 0 when weekdays 

## **Conclusion and insights:**

1) In June maximum bike rented near 1000. and january, february enjoys less rented bike demand near 400. March and June enjoys more bike sharing demand in holiday than non-holidays February,December have less bike sharing demand for both in holidays and non-holidays. April,october,december months have nearly zero bike sharing demand in holidays.

2) weekdays have more rented bike demand than weekend

3)In weekdays 6 pm and 8 am but in weekend only 6 pm are peak time of bike sharing demand. 4 and 5 am has lowest bike sharing demand in both weekeend and weekdays

4) Summer season enjoys overall best and least bike sharing demand and winter has overall less demand than any other season. There are very less bike sharing demand in morning 4 and 5 am

5) From the regression plots we can conclude that the columns

'Rainfall', 'Snowfall', 'Humidity' these features are negatively related with the dependent variable 'Rented Bike Count'. This means when Rainfal,snowfal,humidity is higher bike sharing demand is lower.
'Temperature', 'Wind_speed','Visibility', 'Dew_point_temperature', 'Solar_Radiation' are positively correlated with the dependent variable 'Rented Bike Demand'. This means if 'Temperature', 'Wind_speed','Visibility', 'Dew_point_temperature', 'Solar_Radiation' are higher or lower then bike sharing demand maybe higher or lower respectively.
6) After applying linear regression model, we got r2 score of 0.761 for training dataset and 0.76 for test dataset which defines that model is optimally fit for training and test data i.e no overfitting

7) Therefore, for even better fit, we applied polynomial regression model with degree = 2, we got R2 score of 0.91 for training data and 0.89 for test data

8) We also tried Tree based classifiers for our data, we applied Decision Tree Regressor, since decision tree is prone to overfit, we gave certain parameters like maximum depth of the tree, maximum leaf nodes etc, with that we we got R2 score of 0.842 for training data and 0.798 for test data which is less than polynomial regression.

10) To get better accuracy on tree based model, we applied Random forest with n_estimator as 180 and with maximum depth as 12, with that we got R2 score of 0.875 for training data and 0.854 for test data.

11) Finally, we applied Gradient boost with parameters selected after grid search which resulted in highest R2 score of 0.945 for training data and 0.916 for test data with very less mean squared error of 8.6 and 12.4 in training as well as in test data.

Therefore we can say that it gives us optimal result in term of test dataset. It is best for final prediction

12) Lastly, In bar graph we can see Winter has the highest feature value.We can conclude that Hour_8,Visibility and Wind Speed is not contributing in Decision Tree,Random Forest and Gradient Boost in model prediction

## References
1. GeekforGeeks
2. Kaggle
3. Analytics Vidya

