# Python Project

## Goals
For this project I first used the citybikes API to get the location of each bike station in Toronto, as well as the number of bikes available.  Then we will use that location data with the yelp and foursquare API's to retrieve the number of businesses within a 500 meter radius of each bike station. After gathering and joining all the data, I will test if there is any relationship to be found between the locations, number of free bikes, and number of nearby businesses. 

## Process
Step 1: Gather bike station data (city_bikes.ipynb)

- Query the citybike API to get the latitude,longitude, and free bikes for all stations in Toronto and put them in a dataframe, which we then saved to our sql database for later use

Step 2: Gather Yelp and Foursquare data (yelp_foursquare_EDA.ipynb)

- Using the latitude/longitude from the bike dataframe, we create a new dataframe with the amount of nearby businees according to the yelp and foursquare API.
- EDA will be done in step 3


Step 3: Joining The data together (joining_data.ipynb)

- Here we  join all the data together 
- We also do some initial cleaning and EDA, but not much is needed


Step 4: Model Building ( model_building.ipynb)

- We ran the first linear regression model with available bikes predicting total nearby businesses
- The second model has latitude and longitude predicting total nearby businesses

## Results
Using the amount of available bikes as the independent variable to predict the number of nearby businesses has a p-score of .284 which is not statistically significant.
Latitude and Longitude, however, are correlated with the number of nearby businesses, and this could probably be extrapolated to predict the amount of nearby businesses using any Lat/Long, not just those of bike stations.


## Challenges 
- CityBike API worked perfect, but the yelp and foursquare ones didnt always, and the jsons they returned were hard to read
- There were sometimes hundreds of businesses near each bike station.  To help with this I reduced the search radius from 1000 to 500 meters.
- They yelp api has a limit of 500/day , which isnt enough for the 717 bike stations in toronto.  I ended up using only 400 stations.

