# World_Weather_Analysis

Part 1 WeatherPy

In this assignment I created a Python script to visualize the weather of over 500 cities of varying distances from the equator. I used the citipy Python libraryLinks to an external site., and the OpenWeatherMap APILinks to an external site.


Requirement 1 :Create Plots to Showcase the Relationship Between Weather Variables and Latitude

To fulfill the first requirement, I used OpenWeatherMap API to retrieve weather data from the cities list generated in the starter code. 
Next, created a series of scatter plots to showcase the following relationships:

Latitude vs. Temperature

Latitude vs. Humidity

Latitude vs. Cloudiness

Latitude vs. Wind Speed

From the analysis, the following conclusions can be drawn:
Temperature seems to have a clear correlation with latitude
As expected, the weather becomes significantly warmer as one approaches the equator (0 Deg. Latitude). The southern hemisphere tends to be warmer this time of year than the northern hemisphere.
There is no strong relationship between latitude and humidity. however there is a slightly larger cluster of northern hemisphere cities with high humidity (above 60% humidity)
There is no strong relationship between latitude and cloudiness. However, it is interesting to see that a strong band of cities near 0, 80, and 90% cloudiness
There is no strong relationship between latitude and wind speed. However, in northern hemispheres there is a flurry of cities with over 20 mph of wind
Wind speed tends to generally be between 0 and 15 mph regardless of latitude


After each plot, you will find a mini summary about the code and what it is analyzing.

I then conducted a linear regression on each relationship. But, this time, I separated them into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude).

Northern Hemisphere - Temperature (F) vs. Latitude
Southern Hemisphere - Temperature (F) vs. Latitude
Northern Hemisphere - Humidity (%) vs. Latitude
Southern Hemisphere - Humidity (%) vs. Latitude
Northern Hemisphere - Cloudiness (%) vs. Latitude
Southern Hemisphere - Cloudiness (%) vs. Latitude
Northern Hemisphere - Wind Speed (mph) vs. Latitude
Southern Hemisphere - Wind Speed (mph) vs. Latitude


Temperature vs. Latitude Linear Regression Plot

As expected, the weather becomes significantly warmer as one approaches the equator (0 Deg. Latitude). The southern hemisphere tends to be warmer this time of year than the northern hemisphere.

Humidity vs. Latitude Linear Regression Plot:

There is no strong relationship between latitude and humidity. however there is a slightly larger cluster of northern hemisphere cities with high humidity (above 60% humidity).

Cloudiness vs. Latitude Linear Regression Plot:

There is no strong relationship between latitude and cloudiness. However, it is interesting to see that a strong band of cities near 0, 80, and 90% cloudiness.

Wind Speed vs. Latitude Linear Regression Plot:

There is no strong relationship between latitude and wind speed. However, in northern hemispheres there is a flurry of cities with over 20 mph of wind
 



VacationPy
For the second part of this project (VacationPy), I used the weather data gathered from part one to help plan for future vacations. Specifically, I used jupyter-gmaps and the Google Places API to create a heatmap that displays the humidity for every city from part one. I then narrowed down the list of cities to find the ideal weather conditions, including:

A max temperature lower than 80 degrees but higher than 70.
Wind speed less than 10 mph.
Zero cloudiness.
I ended up dropping any rows that didn't contain all three conditions.

I then used the Google Places API to find the first hotel for each city located within 10000 meters of the coordinates. Finally, I plotted the hotels on top of the humidity heatmap with each pin containing the hotel name, city, and country.

After further analysis i am unable to use hvplot due to some error messages stating

" ImportError: Geographic projection support requires GeoViews, pyproj and cartopy."


I contacted the TA's and instructor to resolve the issue but unable to resolv
