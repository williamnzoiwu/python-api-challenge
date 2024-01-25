# python-api-challenge
## APIs Module 6 Challenge

This script contains two notebooks using the OpenWeatherMap API and the Geoapify API to find weather information for different cities around the world.

### Part 1:WeatherPy
The WeatherPy notebook first generates a litst of cities using the citipy library. It then uses the OpenWeatherMap API to retrieve weather data from the cities list generated in the started code. After it loads all the cities it then stores them in a DataFrame, which it then exports to a csv file. Using the information from the Dataframe, it then creates four scatterplots to display the following relationships for all the cities:

Latitude vs. Temperature
Latitude vs. Humidity
Latitude vs. Cloudiness
Latitude vs. Wind Speed

After creating the four plots, a linear regression model is created for each relationship. Eight more scatterplots are then created, displaying each of the four previous relationships for both the northern and southern hemispheres. These plots each include the linear regression line, the model's formula, the r values, and a description of the relationship underneath. 

### Part 2: VacationPy
In this deliverable, you'll use your weather data skills to plan future vacations. Also, you'll use Jupyter notebooks, the geoViews Python library, and the Geoapify API.
The code needed to import the required libraries and load the CSV file with the weather and coordinates data for each city created in Part 1 is provided to help you get started.
Your main tasks will be to use the Geoapify API and the geoViews Python library and employ your Python skills to create map visualizations.
To succeed on this deliverable of the assignment, open the VacationPy.ipynb starter code and complete the following steps:
Create a map that displays a point for every city in the city_data_df DataFrame as shown in the following image. The size of the point should be the humidity in each city.
Humidity map
Narrow down the city_data_df DataFrame to find your ideal weather condition. For example:
A max temperature lower than 27 degrees but higher than 21
Wind speed less than 4.5 m/s
Zero cloudiness
Feel free to adjust your specifications but make sure to set a reasonable limit to the number of rows returned by your API requests.
Create a new DataFrame called hotel_df to store the city, country, coordinates, and humidity.
For each city, use the Geoapify API to find the first hotel located within 10,000 meters of your coordinates.
Add the hotel name and the country as additional information in the hover message for each city on the map as in the following image:
