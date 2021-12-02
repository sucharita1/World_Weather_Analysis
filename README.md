# World_Weather_Analysis
Use  analysis, visualization, and statistical skills to retrieve and analyze weather data for a hypothetical travel company, PlanMyTrip.

## Overview of the Analysis
Plan My Trip is a top travel technology company that specializes in internet related services in the hotel and lodging industry. Jack is the head of analysis for the user interface team. 
* We help Jack to build a database of 690 cities across the world and present data for customers which they will then filter based on their preferred temperature range using OpenWeather API.
* Based on the cities remaining they can select upto 4 destinations to visit which are nearby we can curate an itenerary for them letting them know about the hotel in the city, city name, country, current weather and temperature, marked in google maps using places API.
* Using directions API they will be provided in the driving route that includes all the places that they selected. 

## Resources
* Data Source: Google Maps Platform APIs, OpenWeather API
* Software: Python 3.7.10, Jupyter notebook 6.3.0

## Results:
#### Weather_Database folder:
1. A jupyter notebook [Weather_Database.ipynb](https://github.com/sucharita1/World_Weather_Analysis/blob/f23feac739d69a0408e18180f36efcee68b9b21d/Weather_Database/Weather_Database.ipynb) to generate the data for the cities using random, citipy and OpenWeather API.
2. A csv file [WeatherPy_Database.csv](https://github.com/sucharita1/World_Weather_Analysis/blob/f23feac739d69a0408e18180f36efcee68b9b21d/Weather_Database/WeatherPy_Database.csv) containing the 690 citites with their country, latitude, longitude, maximum temperature, % Humidity, % Cloudiness, Wind speed and current weather description.

####  Vacation_Search folder:
1. A jupyter notebook [Vacation_Search.ipynb](https://github.com/sucharita1/World_Weather_Analysis/blob/f23feac739d69a0408e18180f36efcee68b9b21d/Vacation_Search/Vacation_Search.ipynb) to that takes user input about their preferred minimum and maximum temperature requirements and creates a dataframe of cities with preffered temperatures using the dataframe created from WeatherPy_Database.csv. 
2. Using places API to finds hotels near cities at those preferred temperatures and saves the new dataframe to csv as [WeatherPy_vacation.csv](https://github.com/sucharita1/World_Weather_Analysis/blob/f23feac739d69a0408e18180f36efcee68b9b21d/Vacation_Search/WeatherPy_vacation.csv) with their city, country, latitude, longitude, maximum temperature, weather description and hotel name.
3. Using maps API to add a pop marker for each city showing hotel name, city, country and current weather and max temperature. It is saved as 
![WeatherPy_vacation_map.png](https://github.com/sucharita1/World_Weather_Analysis/blob/f23feac739d69a0408e18180f36efcee68b9b21d/Vacation_Search/WeatherPy_vacation_map.png?raw=true)

#### Vacation_Itinerary folder:
1. a jupyter notebook [Vacation_Itinerary.ipynb](https://github.com/sucharita1/World_Weather_Analysis/blob/f23feac739d69a0408e18180f36efcee68b9b21d/Vacation_Itinerary/Vacation_Itinerary.ipynb) to that takes data from WeatherPy_vacation.csv and converts to a dataframe then we choose four cities to plan a vacation itinerary and create four dataframes for four cities
2. Using Directions API we plot the route across these four cities in the 'DRIVING' mode. And save the route in ![WeatherPy_travel_map.png](https://github.com/sucharita1/World_Weather_Analysis/blob/f23feac739d69a0408e18180f36efcee68b9b21d/Vacation_Itinerary/WeatherPy_travel_map.png?raw=true)
3. Using maps API to add a pop marker for each of the four chosen cities showing hotel name, city, country and current weather and max temperature. It is saved as 
![WeatherPy_travel_map_markers.png](https://github.com/sucharita1/World_Weather_Analysis/blob/f23feac739d69a0408e18180f36efcee68b9b21d/Vacation_Itinerary/WeatherPy_travel_map_markers.png?raw=true)



