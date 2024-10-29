# BikeSharingAssignment
> Outline a brief description of your project.


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
**Problem Statement**
A bike-sharing system is a service in which bikes are made available for shared use to individuals on a short term basis for a price or free. Many bike share systems allow people to borrow a bike from a "dock" which is usually computer-controlled wherein the user enters the payment information, and the system unlocks it. This bike can then be returned to another dock belonging to the same system.


A US bike-sharing provider BoomBikes has recently suffered considerable dips in their revenues due to the ongoing Corona pandemic. The company is finding it very difficult to sustain in the current market scenario. So, it has decided to come up with a mindful business plan to be able to accelerate its revenue as soon as the ongoing lockdown comes to an end, and the economy restores to a healthy state. 


In such an attempt, BoomBikes aspires to understand the demand for shared bikes among the people after this ongoing quarantine situation ends across the nation due to Covid-19. They have planned this to prepare themselves to cater to the people's needs once the situation gets better all around and stand out from other service providers and make huge profits.


They have contracted a consulting company to understand the factors on which the demand for these shared bikes depends. Specifically, they want to understand the factors affecting the demand for these shared bikes in the American market. The company wants to know:

Which variables are significant in predicting the demand for shared bikes.
How well those variables describe the bike demands
Based on various meteorological surveys and people's styles, the service provider firm has gathered a large dataset on daily bike demands across the American market based on some factors. 


**Business Goal:**
You are required to model the demand for shared bikes with the available independent variables. It will be used by the management to understand how exactly the demands vary with different features. They can accordingly manipulate the business strategy to meet the demand levels and meet the customer's expectations. Further, the model will be a good way for management to understand the demand dynamics of a new market. 


**Data Preparation:**

You can observe in the dataset that some of the variables like 'weathersit' and 'season' have values as 1, 2, 3, 4 which have specific labels associated with them (as can be seen in the data dictionary). These numeric values associated with the labels may indicate that there is some order to them - which is actually not the case (Check the data dictionary and think why). So, it is advisable to convert such feature values into categorical string values before proceeding with model building. Please refer the data dictionary to get a better understanding of all the independent variables.
 
You might notice the column 'yr' with two values 0 and 1 indicating the years 2018 and 2019 respectively. At the first instinct, you might think it is a good idea to drop this column as it only has two values so it might not be a value-add to the model. But in reality, since these bike-sharing systems are slowly gaining popularity, the demand for these bikes is increasing every year proving that the column 'yr' might be a good variable for prediction. So think twice before dropping it. 
 

**Model Building**

In the dataset provided, you will notice that there are three columns named 'casual', 'registered', and 'cnt'. The variable 'casual' indicates the number casual users who have made a rental. The variable 'registered' on the other hand shows the total number of registered users who have made a booking on a given day. Finally, the 'cnt' variable indicates the total number of bike rentals, including both casual and registered. The model should be built taking this 'cnt' as the target variable.


**Model Evaluation:**
When you're done with model building and residual analysis and have made predictions on the test set, just make sure you use the following two lines of code to calculate the R-squared score on the test set.

 

from sklearn.metrics import r2_score
r2_score(y_test, y_pred)
 

where y_test is the test data set for the target variable, and y_pred is the variable containing the predicted values of the target variable on the test set.
Please don't forget to perform this step as the R-squared score on the test set holds some marks. The variable names inside the 'r2_score' function can be different based on the variable names you have chosen.
 

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Conclusions
**Best fitting equation for our model.**
y = 0.203679 + 0.491531 * x1 + 0.233727 * x2 + 0.084588 * x3 + 0.075934 * x4 + 0.047677 * x5 + 0.011757 * x6 - 0.046120 * x7 - 0.049633 * x8 - 0.065505 * x9 - 0.082161 * x10 - 0.102859 * x11 - 0.149066 * x12 - 0.289513 * x13 Influence of Interaction Variables:

**Positive Effect:**
Temperature (temp): The higher the temperature, the higher the bike rental.
Year (yr): The trend for bike rental is positive with every year.
Season (Winter, Summer, Sep): Bike demand is high in these seasons compared to Spring and July.
Weekend (Saturday): Bike rentals are a little more on Saturdays compared to weekdays.
Negative Effect:
Weather Conditions (Mist & Cloudy, Light Snow & Rain): Bad weather conditions decrease the bike demand.
Day of Week (Sundays): The demand for bikes is relatively lesser on Sundays than on weekdays.
Wind Speed (windspeed): More wind speed actually lowers the demand for bikes.
Holidays (holiday): Bike rentals are lesser on holidays.
Model Performance:
The R-squared value means that the model captures an important percentage of the variance of bike demand. This means that the features chosen do well at predicting bike demand.

**Key Considerations:**
Undoubtedly, the model may bring forth other states or kinds of weather to produce various results.
The other considerations are public transportation and activities of local events.
Greater data analysis can be carried out along with calibrations or changes of the model in pursuit of increasing the prediction.

**Actionable Insights**
Weather-Based Strategies: Launch differential pricing or promotions that attract more rentals during the good days.
Seasonal Marketing : Form marketing strategies targeting specific seasons and months at peak demand.
Infrastructure: Bike lanes and bike parking facilities are to be encouraged for biking.
Data-driven decision making: To know the behavior of a user, the data is to be analyzed, so as to operate the bikes.
These results will make a bike sharing company increase the customer satisfaction and business.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Technologies Used
Python Libraries

1. numpy

2. pandas

3. matplot

4. seaborn

5. sklearn

6. statsmodels

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements
- This project was inspired by upGrad.


## Contact
Created by https://github.com/RohitKini - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project --># 