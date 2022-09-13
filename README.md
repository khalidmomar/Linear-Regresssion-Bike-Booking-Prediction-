# Predicting-Bike-Booking-Count-for-BoomBikes-US-Using-Multiple-Linear-Regression
Building a Linear Regression Model which is built to predict the bike booking counts based on different features.

## Introduction:


## Describing Bike Sharing Systems 
Bike-sharing system is a service in which bikes are made available for shared use to individuals on a short term basis for a price or free. Many bike share systems allow people to borrow a bike from a "dock" which is usually computer-controlled wherein the user enters the payment information, and the system unlocks it. This bike can then be returned to another dock belonging to the same system.

## Problem Statement

A US bike-sharing provider BoomBikes has recently suffered considerable dips in their revenues due to the ongoing Corona pandemic. The company is finding it very difficult to sustain in the current market scenario. So, it has decided to come up with a mindful business plan to be able to accelerate its revenue as soon as the ongoing lockdown comes to an end, and the economy restores to a healthy state. BoomBikes aspires to understand the demand for shared bikes among the people after this ongoing quarantine situation ends across the nation due to Covid-19. BookBikes wants to understand the factors affecting the demand for these shared bikes in the American market. 
-Which variables are significant in predicting the demand for shared bikes.
-How well those variables describe the bike demands

## Business Objective
Build a model to identify the features thad would affect the demand based on the new market after COVID.The managment needs to understand the demand dynamics of a new market. How exactly the demands vary with different features?

## Variables:

Data provided: day.csv have the following fields:
-instant: record index
- dteday : date
- season : season (1:spring, 2:summer, 3:fall, 4:winter)
- yr : year (0: 2018, 1:2019)
- mnth : month ( 1 to 12)
- holiday : weather day is a holiday or not (extracted from http://dchr.dc.gov/page/holiday-schedule)
- weekday : day of the week
- workingday : if day is neither weekend nor holiday is 1, otherwise is 0.
- weathersit : 
-- 1: Clear, Few clouds, Partly cloudy, Partly cloudy
-- 2: Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
-- 3: Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
-- 4: Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog
- temp : temperature in Celsius
- atemp: feeling temperature in Celsius
- hum: humidity
- windspeed: wind speed
- casual: count of casual users
- registered: count of registered users
- cnt: count of total rental bikes including both casual and registered

## Prediction of count based on other variables: 
We are trying to predict count variable i.e. number of total bookings which will be behaving as a dependent variable (Y)-axis for our analysis.

## Steps Followed
- 1. Read and Understand the Data
- 2. Visualising the Data
- 3. Data Prepration
- 4. Splitting the Data into Training and Testing Sets
- 5. Building a linear model
- 6. Model Selection
- 7. Residual Analysis of the train data
- 8. Making Predictions Using the Final Model
- 9. Model Evaluation

## Findings:
Equation representing best fit line is:
We can see that the equation of our best fitted line is:
$ cnt = 0.55  \times  temp + 0.23  \times  yr + 0.13 \times winter + 0.1 \times Sept + 0.09 \times summer + 0.07 \times Sat+ 0.06 \times workingday - 0.29 \times Light_Snow_Rain - 0.16 \times windspeed - 0.08 \times Mist_Clouds $
- Demand depends on the following variables:
-- temp , yr ,winter, sept, summer, Sat ,Workingday ,Light_snow_Rain weather,windspeed , Mist_Clouds
- Temp is the most significant with the largest coefficient.
- Followed by weathersit_Light Snow & Rain.
- Bike rentals is more for the month of september

## License:
Use of this dataset in publications must be cited to the following publication:

[1] Fanaee-T, Hadi, and Gama, Joao, "Event labeling combining ensemble detectors and background knowledge", Progress in Artificial Intelligence (2013): pp. 1-15, Springer Berlin Heidelberg, doi:10.1007/s13748-013-0040-3.

@article{
	year={2013},
	issn={2192-6352},
	journal={Progress in Artificial Intelligence},
	doi={10.1007/s13748-013-0040-3},
	title={Event labeling combining ensemble detectors and background knowledge},
	url={http://dx.doi.org/10.1007/s13748-013-0040-3},
	publisher={Springer Berlin Heidelberg},
	keywords={Event labeling; Event detection; Ensemble learning; Background knowledge},
	author={Fanaee-T, Hadi and Gama, Joao},
	pages={1-15}
