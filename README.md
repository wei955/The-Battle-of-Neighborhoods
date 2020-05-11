# Cousera Applied Data Science Capstone Project 
## The Battle of Neighborhoods
* Created a recommendation system to help migrants find a similar neighborhood in the new city as the one they live in before.
* Scraped data from wikipage using python and selenium.
* Used Foursquare API to locate nearby venues of each neighbourhoods.
* Applied K-Means model to segment and cluster all the neighborhoods based on the similarity of the venue types.


## Data Collection
Scraped wikipage that contains borough and neighbourhood information of Toronto and Shanghai:
* Toronto.csv:  consists of Toronto’s postcodes boroughs, neighborhoods.
* Shanghai.csv that consists of Shanghai’s city name, districts and subdistrict
* Geographical coordinates of each postal code for neighbourhoods in Toronto is provided.


## Methodology
* Obtain Coordinates: obtained latitude and longitude coordinates of each neighbourhood. 

*  Data Visualization: Used Folium library to plot a map of all the neighbourhoods in each city. cleaned out outliers that do not lie into their boroughs due to wrong location data.

*  Foursquare API Search Feature: Sent HTTP request by using Foursquare API and received venues information within 500 meters of each neighbourhood in json file. Only venue names and categories were extracted from the results.

*  Model Building
Applied K-Means model to segment and cluster all the neighborhoods in Toronto and Shanghai based on the similarity of the venue types. Used Elbow method to determine the right value of K. 


## Results
Folium maps of each cluster are created to facilitate the analysis results.

![alt text](https://github.com/wei955/The-Battle-of-Neighborhoods/blob/master/pic%201.png "pic 1")
![alt text](https://github.com/wei955/The-Battle-of-Neighborhoods/blob/master/pic%202.png "pic 1")

People in the world are nowadays moving more frequently than before, I hope this analysis will help you to make a decision of choosing the neighbourhood in the destination city that fit for your needs.

## Code and Resources Used
* Python Version: 3.7
* Packages: pandas, numpy, sklearn, matplotlib, folium, selenium, geopy
* City info: https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_M
https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_M
* Geo coordinates: http://cocl.us/Geospatial_data
