# KDD Project
This repository is my course project in Knowledge Discovery in Databases Course. In this project 
I will apply the CRISP-DM process and standard data mining techniques to ["US Accidents"](https://www.kaggle.com/sobhanmoosavi/us-accidents) which is a Countrywide Traffic Accident Dataset (2016 - 2020).

## Introduction to Problem or Opportunity
Accidents are the fourth leading cause of death in the US after heart disease, cancer, and strokes. 
This ranking is based on all types of accidents. Also, more than 32,000 people are killed and 2 million are injured each year from motor vehicle crashes.
looking at this data will show us a big problem. Many people are dying or injured on the roads because 
of bad weather, road condition and drivers behaviour and reducing motor vehicle crash deaths is one of the great public health challenge in the US. 
Suppose there is an application to alerting the probability of accidents and their severity. In that case, 
people might change their decision to travel or choose a substitution road. This project will use previous 
accident data and dependent conditions to design a model to predict 
an accident’s probability and severity according to the mentioned conditions.

## Domain and Dataset
US Accidents data can be used for numerous applications such as real-time accident prediction, 
studying accident hotspot locations, casualty analysis, and extracting cause and effect rules to predict accidents, 
or studying the impact of precipitation or other environmental factors on accident occurrence.

This is a countrywide traffic accident dataset, which covers 49 states of the United States. The data is 
collected from February 2016 to December 2020, using several data providers, including multiple APIs that provide streaming 
traffic event data. These APIs broadcast traffic events captured by a variety of entities, such as the US and state 
departments of transportation, law enforcement agencies, traffic cameras, and traffic sensors within the road-networks. 
Currently, there are about 3 million accident records in this dataset.  

### Data Format and Attributes
The data is provided in a CSV file. Following table describes the data attributes

|Attribute     |  Description   | 
|---------|-----------------|
|ID| This is a unique identifier of the accident record. |
|Severity| Shows the severity of the accident, a number between 1 and 4, where 1 indicates the least impact on traffic (i.e., short delay as a result of the accident) and 4 indicates a significant impact on traffic (i.e., long delay). |
|Start_Time| Shows start time of the accident in local time zone. |
|End_Time| Shows end time of the accident in local time zone. End time here refers to when the impact of accident on traffic flow was dismissed. |
|Start_Lat| Shows latitude in GPS coordinate of the start point. |
|Start_Lng| Shows longitude in GPS coordinate of the start point. |
|End_Lat| Shows latitude in GPS coordinate of the end point. |
|End_Lng| Shows longitude in GPS coordinate of the end point. |
|Distance(mi)| The length of the road extent affected by the accident. |
|Description| Shows natural language description of the accident. |
|Number| Shows the street number in address field. |
|Street| Shows the street name in address field. |
|Side| Shows the relative side of the street (Right/Left) in address field. |
|City| Shows the city in address field. |
|County| Shows the county in address field. |
|State| Shows the state in address field. |
|Zipcode| Shows the zipcode in address field. |
|Country| Shows the country in address field. |
|Timezone| Shows timezone based on the location of the accident (eastern, central, etc.). |
|Airport_Code| Denotes an airport-based weather station which is the closest one to location of the accident. |
|Weather_Timestamp| Shows the time-stamp of weather observation record (in local time). |
|Temperature(F)| Shows the temperature (in Fahrenheit). |
|Wind_Chill(F)| Shows the wind chill (in Fahrenheit). |
|Humidity(%)| Shows the humidity (in percentage). |
|Pressure(in)| Shows the air pressure (in inches). |
|Visibility(mi)| Shows visibility (in miles). |
|Wind_Direction| Shows wind direction. |
|Wind_Speed(mph)| Shows wind speed (in miles per hour). |
|Precipitation(in)| Shows precipitation amount in inches, if there is any. |
|Weather_Condition| Shows the weather condition (rain, snow, thunderstorm, fog, etc.) |
|Amenity| A POI annotation which indicates presence of amenity in a nearby location. |
|Bump| A POI annotation which indicates presence of speed bump or hump in a nearby location. |
|Crossing| A POI annotation which indicates presence of crossing in a nearby location. |
|Give_Way| A POI annotation which indicates presence of give_way in a nearby location. |
|Junction| A POI annotation which indicates presence of junction in a nearby location. |
|No_Exit| A POI annotation which indicates presence of no_exit in a nearby location. |
|Railway| A POI annotation which indicates presence of railway in a nearby location. |
|Roundabout| A POI annotation which indicates presence of roundabout in a nearby location. |
|Station| A POI annotation which indicates presence of station in a nearby location. |
|Stop| A POI annotation which indicates presence of stop in a nearby location. |
|Traffic_Calming| A POI annotation which indicates presence of traffic_calming in a nearby location. |
|Traffic_Signal| A POI annotation which indicates presence of traffic_signal in a nearby loction. |
|Turning_Loop| A POI annotation which indicates presence of turning_loop in a nearby location. |
|Sunrise_Sunset| Shows the period of day (i.e. day or night) based on sunrise/sunset. |
|Civil_Twilight| Shows the period of day (i.e. day or night) based on civil twilight. |
|Nautical_Twilight| Shows the period of day (i.e. day or night) based on nautical twilight. |
|Astronomical_Twilight| Shows the period of day (i.e. day or night) based on astronomical twilight. |

### Research Questions
The goal of this research is developing an accident prediction models based on scope of the dataset. Prediction could be created by 
features such as time, location, whether condition and infrastructure(traffic lights, road,...).

Therefore, the following research questions are proposed:
* How do different conditions affect accident’s severity probability?
* How does the relative risk of different severity vary with infrastructure?
* How much does predictive modeling reduce the occurrence of the accidents?

## Technologies & Process
### Methods Used
* Inferential Statistics
* Machine Learning
* Data Visualization
* Predictive Modeling

### Technologies
* Python
* jupyter

### Needs of this project Based on CRISP
- Business understanding – What does the business need?
- Data understanding – What data do we have / need? Is it clean?
- Data preparation – How do we organize the data for modeling?
- Modeling – What modeling techniques should we apply?
- Evaluation – Which model best meets the business objectives?
- Deployment – How do stakeholders access the results?  

### Code Parts
- Date Preprocessing, Understanding.
  - Load and browsing data.
  - Data Description.
- Data Cleaning
  - Drop useless features.
  - Filling missing value based on feature structure.
  - Drop the rest of missing value.
- Data Exploration
  - Data balancing and distribution.
  - Weather Condition Analysis.
  - Time Analysis.
  - Infrastructure Analysis.
  - Geographical Analysis.
- Feature Engineering
  - Handling Categorical features.
  - Features Correlation.
- Data Preparation for Modeling
  - Turning target values (Severity) to binary class.
  - Splitting train and test set.
  - Using under-sampling technique to deal with imbalanced data.
- Modeling
  - Compare different algorithm and select best model.
  - Tuning the model.
- Evaluating
  - Confusion Matrix.
  - ROC Curve and AUC Scores.
  - Classification Report.
- Feature Importance
  - Finding feature importance based on built-in, permutation and Shap methods.


## Getting Started

1. Clone this repo.
2. Download the Raw Data [here](https://www.kaggle.com/sobhanmoosavi/us-accidents) and put it into data folder.
3. Install requirements by: `pip install -r requirements.txt`

## Conclusion



## Future Work
Developing a real-time Data-Driven model to predict and make a real-time feedback to drivers to avoid accidents.