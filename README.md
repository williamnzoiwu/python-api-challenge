# python-api-challenge
## APIs Module 6 Challenge

This script contains two notebooks using the OpenWeatherMap API and the Geoapify API to find weather information for different cities around the world.

### Part 1:WeatherPy
The WeatherPy notebook first generates a litst of cities using the citipy library. It then uses the OpenWeatherMap API to retrieve weather data from the cities list generated in the started code. After it loads all the cities it then stores them in a DataFrame, which it then exports to a csv file. Using the information from the Dataframe, it then creates four scatterplots to display the following relationships for all the cities:

Latitude vs. Temperature,

Latitude vs. Humidity,

Latitude vs. Cloudiness,

Latitude vs. Wind Speed.

After creating the four plots, a linear regression model is created for each relationship. Eight more scatterplots are then created, displaying each of the four previous relationships for both the northern and southern hemispheres. These plots each include the linear regression line, the model's formula, the r values, and a description of the relationship underneath. 

### Part 2: VacationPy
This code first imports the city_data_df Dataframe from the WeatherPy notebook by reading the csv file. It then creates a map that displays a point for every city in the  DataFrame, with the size of the point being the humidity in each city. Each point has a box displaying the city stats when the point is hovered with the the mouse.

Next another data frame is created from the city_data_df DataFrame only containing cities with certain weather conditions, ideally spots for a vacation. The new DataFrame contains only the cities with the following parameters:

A max temperature lower than 30 degrees but higher than 10,

Wind speed of 3 m/s or less,

Zero cloudiness.

After the specifications are set, the new Dataframe only keeps the City, Country, Lat, Lng, and Humidity columns.
The Geoapify API is then used to find the first hotel located within 10,000 meters of your coordinates for each city. The hotels are then printed, with the text "no hotel found" appearting for cities without a hotel within the desired radius. Lastly, a second map is created with just the hotels appearing on the map, with hovertext for the hotel city and country for each point.
