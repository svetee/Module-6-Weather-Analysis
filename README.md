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
