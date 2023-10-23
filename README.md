# Final-Project-Statistical-Modelling-with-Python

## Project/Goals
-combine data from 3 seperate APIs
-do some EDA
-gain some insighst

## Process
### (your step 1)
-Get latitude, longitude, and free bikes from the citybike api
-Put it in a DataFrame
### (your step 2)
-Use the latitude/longitude dataframe to get nearby POIs from the other 2 apis and add them to the data in new columns

## Results
-The yelp API is more detailed and easier to read
## Challenges 
-Its hard for me to visualize the structure of jsons in my head, and the text you get is so messy its hard to see whats going on sometimes
-The yelp api requires you to put "bearer" in front of the api key but doesnt say this anywhere
-yelp api has a limit of 500/day which is less than the 717 bike stations

## Future Goals
-If the api keys were more important, they should be in environment variables instead before pushing to GIT
