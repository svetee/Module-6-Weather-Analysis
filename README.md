# Weather Travel Analysis

## Project Overview

In this module, we practice our analysis, visualization, and statistical skills by retrieving and analyzing weather data for a hypothetical travel company, PlanMyTrip. Successfully completing the tasks will draw on our knowledge of Python, decision and repetition statements, data structures, Pandas, Matplotlib, and SciPy statistics.

## Resources
- Data Source: https://openweathermap.org/api
- Software: Jupyter Notebook, Pandas Library, CityPy, Python Request, APIs, JSON Traversals

## Challenge Overview
For the new modifications to the PlanMyTrip app, we are asked to add more data to the database, or cities DataFrame, so that customers know the weather in the cities when they click on a pop-up marker. We also added the amount of rainfall or snowfall within the last three hours so that customers can filter the DataFrame using input statements based on the temperature range and whether or not it is raining or snowing. Finally, we created a directions layer Google map that shows the directions between multiple cities for travel.

### Objectives:
Use nested try-except blocks
Use Pandas methods and attributes on a DataFrame or Series.
Create a new DataFrame from a new API search with new weather parameters.
Filter DataFrames based on input and nested decision statements, and logical expressions.
Create pop-up markers on a Google map from a filtered DataFrame.
Add a directions layer on a Google map between cities in the filtered DataFrame.

## Summary

### Part 1

Get the Weather Description and Amount of Precipitation for Each City
We generated a set of 2,000 random latitudes and longitudes.
Got the nearest city using the citipy module.
Performed an API call with the OpenWeatherMap.
Retrieved the following information from the API call:

- Latitude and longitude
- Maximum temperature
- Percent humidity
- Percent cloudiness
- Wind speed
- Weather description (e.g., clouds, fog, light rain, clear sky)
- Using a try-except block, if it is raining, get the amount of rainfall in inches for the last three hours. If it is not raining, add 0 inches for the city.
- Using a try-except block, if it is snowing, get the amount of snow in inches for the last three hours. If it is not snowing, add 0 inches for the city. Added the data to a new DataFrame.
- Our new DataFrame looks similar to the following image:

<img width="1077" alt="table1" src="https://user-images.githubusercontent.com/60243906/105417696-1353e800-5be0-11eb-95dc-3ccff26f1762.png">

### Part 2

Have Customers Narrow Their Travel Searches Based on Temperature and Precipitation
We imported the WeatherPy_vacation.csv file from Part 1 as a new DataFrame. Filter the DataFrame for minimum and maximum temperature preferences, and if the rain or snow accumulation is 0 inches or not using conditional statements. Doing the following:

- Prompt the customer for the minimum temperature preference.
- Prompt the customer for the maximum temperature preference.
- Prompt the customer to answer if he or she would like it to be raining or not, using input("Do you want it to be raining? (yes/no) ").
- Prompt the customer to answer if he or she would like it to be snowing or not, using input("Do you want it to be snowing? (yes/no) ").
- Our new hotel DataFrame looks similar to the following image:

<img width="819" alt="Screen Shot 2021-01-21 at 12 00 20 PM" src="https://user-images.githubusercontent.com/60243906/105417864-501fdf00-5be0-11eb-8e81-4a8f75cf39e4.png">

From the filtered DataFrame we added the cities to a marker layer map with a pop-up marker for each city that includes:

- Hotel name
- City
- Country
- Current weather description with the maximum temperature

![WeatherPy_vacation_map](https://user-images.githubusercontent.com/60243906/105417994-85c4c800-5be0-11eb-9cba-bce13b51ba81.png)

### Part 3

Create a Travel Itinerary with a Corresponding Map
We created a map (travel itinerary) that shows the route between four cities from the customer’s possible travel destinations, and then created a map with pop-up markers for the four cities, by:

Importing the WeatherPy_vacation.csv file as a new DataFrame. From the vacation search map, we chose four cities in close proximity on our map that are on the same continent that a customer might travel to, and then created a directions layer map.

We Filtered the DataFrame for each city we wanted to go to and created separate DataFrames for each city.
Used the directions Layer instructions from the gmaps documentation
Use the list indexing and Pandas methods to get the latitude-longitude pairs for each city DataFrame as tuples.

<img width="874" alt="Screen Shot 2021-01-21 at 12 07 20 PM" src="https://user-images.githubusercontent.com/60243906/105418514-595d7b80-5be1-11eb-9944-e986c9e8742b.png">

<img width="876" alt="Screen Shot 2021-01-21 at 12 07 13 PM" src="https://user-images.githubusercontent.com/60243906/105418523-5e222f80-5be1-11eb-8e06-4cba2892263c.png">
