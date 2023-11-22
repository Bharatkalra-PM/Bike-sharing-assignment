#Bike SHaring assignment

#Problem Statement
A bike-sharing system is a service in which bikes are made available for shared use to individuals on a short term basis for a price or free. Many bike share systems allow people to borrow a bike from a "dock" which is usually computer-controlled wherein the user enters the payment information, and the system unlocks it. This bike can then be returned to another dock belonging to the same system.


A US bike-sharing provider BoomBikes has recently suffered considerable dips in their revenues due to the ongoing Corona pandemic. The company is finding it very difficult to sustain in the current market scenario. So, it has decided to come up with a mindful business plan to be able to accelerate its revenue as soon as the ongoing lockdown comes to an end, and the economy restores to a healthy state. 



#Business Goal:
You are required to model the demand for shared bikes with the available independent variables. It will be used by the management to understand how exactly the demands vary with different features. They can accordingly manipulate the business strategy to meet the demand levels and meet the customer's expectations. Further, the model will be a good way for management to understand the demand dynamics of a new market. 
This is a Group project assigned as a module in Exploratory Data Analysis

#Data Set
Dataset characteristics
=========================================	
day.csv have the following fields:
	
	- instant: record index
	- dteday : date
	- season : season (1:spring, 2:summer, 3:fall, 4:winter)
	- yr : year (0: 2018, 1:2019)
	- mnth : month ( 1 to 12)
	- holiday : weather day is a holiday or not (extracted from http://dchr.dc.gov/page/holiday-schedule)
	- weekday : day of the week
	- workingday : if day is neither weekend nor holiday is 1, otherwise is 0.
	+ weathersit : 
		- 1: Clear, Few clouds, Partly cloudy, Partly cloudy
		- 2: Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
		- 3: Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
		- 4: Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog
	- temp : temperature in Celsius
	- atemp: feeling temperature in Celsius
	- hum: humidity
	- windspeed: wind speed
	- casual: count of casual users
	- registered: count of registered users
	- cnt: count of total rental bikes including both casual and registered



#Steps to perform Mul􀆟ple Linear Regression:
1) Reading and understanding the data
2) Cleaning the data
3) Visualizing the data using EDA
4) Preparing the data for modelling(train-test split, rescaling)
5) Training the model
6) Residual Analysis
7) Predic􀆟ons and Evalua􀆟ons on test set



#Insight Summary:

From the boxplots, we can see that count of total rental bikes(dependent variable) is :
• higher during the fall season and rela􀆟vely low in spring season
• increases significantly in the year 2019 from 2018
• increases somewhat linearly in first half of the year and then it starts decreasing. During September, bike sharing is more.
• higher on days (other than holidays), probably because people commute to office
• count of total rental bikes is higher during clear weather and dips during rainy days
• Addi􀆟onally, correla􀆟on between temp and atemp is quite high
• Weekday is not giving clear picture about demand.


Top 3 variables contribu􀆟ng significantly towards the demand of shared bikes:
a) Temp
b) yr
c) winter season

R^2 value for test data is 82% which is somewhat close to R^2value for test set

### We can see the equation of the best fitted line as follows:
cnt = .0989 + 0.2315*yr + 0.0530*workingday + 0.4667*temp - 0.1486*hum - .1909*windspeed + 0.0835*summer + 0.1438*winter + 0.0466*aug - 0.0467*dec - 0.0411*feb - jan*.0696 + nov*.0441 + sep*.1045 - mon*.0183 + sat*.0580 - bad*.1170 + .1373*good + .0787* moderate

Overall, the entire model is a good fit basis test data validation analysis


#Technologies Used:
Python - Version 3.12.0
numpy - Version 1.26.0
pandas - Version 2.1.1
Jupyter Notebook - Version 6.5.2
JupyterLab - Version 3.5.3
Anaconda - Version 2.4.2


#Acknowledgements and References:
The project references insights and inferences from Stackoverflow
The project reference course materieals from upGrads curriculm


Submitted By:
Bharat Kalra

This project is open source

