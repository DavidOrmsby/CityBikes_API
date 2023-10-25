

- In this project I will connect to the citybikes API to get info for all  the bike stations in Toronto

- Then I will use the location data from the  stations to get the number of nearby businesses from the yelp and foursquare APIs



bikedata.csv - Data for all 717 bike stations in toronto
venuedata.csv - Number of results (nearby businesses) from yelp and foursquare, in the same order as bikedata.csv, but shortened to 400 due to yelp api limit.
These will  be combined in the joining_data notebook and then saved into a sql database (mydatabase)

After that, we will run some models in the model_building notebook

EDA and data cleaning are also done in the model_building notebook