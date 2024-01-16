# World Weather Analysis

In this challenge I am using weather description data to enhance the PlanMyTrip app where I get the user weather preferences and plan their itinerary based of the nearby hotels of the respective cities .

Overview of the project
 The focus of the project lies in
 
 1. Retrieving 2,000 random pairs of cordinates using numpy function
 2. Use OpenWeatherMap api to retrieve the nearby cities for each pair of coordinates
 3. Use OpenWeatherMap api to retrieve the weather inofrmation of each city
 4. Delete the corodinate pairs that do not have city associated with them.
 5. Use Google Maps to retieve the hotel information for each city within a 5,000 meter radius
 6. Plot a world map with markers showing the locations of each hotel obtained from Google Map serach.
 7. Plot a map showing the travel itinerary between four cities among the list of cities generated by the program


Software :
Python 3.7.6, Panda Library, MatplotLib,Jupyter Notebook, APIs and JSON Traversals
 
 Tools/Libraries Used:
- numpy library
- zip object packs
- citipy library
- OpenWeatherMap APIs and Google Maps APIs 
- Parse Api responses
- datetime library
- use of JSON standard format
- usage of try except block
- use of googlemaps
- adding markers and info box templates
- getting inputs from user

## 1.  Create Weather Database
 The weather Data was retrieved based on a set of 2,000 random latitudes and longitudes using numpy library.
 Using the citipy API, the cities weather data like name, country, latitude, longitude, max temperature, humidity, cloudinessand the current weather description were collected and saved into Cities DataFrame and exported to a csv file as WeatherPy_Database.csv
 
 ### Cities DataFrame
  ![img](https://github.com/hsurisetti/World_Weather_Analysis_Challenge/blob/main/Weather_Database/City_DataFrame.png)
  
 ## 2. Vacation Search
- Applying the user weather preferences the cities count were narrowed down
- A new DataFrame was created based on the minimum and maximum temperature and empty rows were dropped
- Using the gmaps API, the nearby hotels were extracted from each cities in our city list and created DataFrame to hold the destination information and the hotel names. The rows that don't have a hotel name are dropped The DataFrame was exported to csv file as WeatherPy_vacation.csv
- The world map was created with markers and info box for the vacation search

### Hotels DataFrame
  ![img](https://github.com/hsurisetti/World_Weather_Analysis_Challenge/blob/main/Vacation_Search/Clean_Hotel_DataFrame.png)
  
## 3. Vacation Itinerary
- Finally, using google directions API , travel itinerary was created to show the route between four cities from the customer's possible travel destinations.
- Then a marker layer map was added with a pop-up marker for each city on the itinerary

### Trip Itinerary
![img](https://github.com/hsurisetti/World_Weather_Analysis_Challenge/blob/main/Vacation_Itinerary/Trip_itinerary.png)

### Itinerary hotels with marker pop-ups
![img](https://github.com/hsurisetti/World_Weather_Analysis_Challenge/blob/main/Vacation_Itinerary/ItineraryHotels_with_marker_popups.png)

## Conclusion:
  With the help of OpenWeatherMaps API and GoogleMaps API,I was able to generate my own travel plan with the choice of weather selections , city and country I prefer to travel and plan my own travel itinerary. I find this project very interesting, practical and api friendly, where I can see a lot more potential in developing and exploring many more projects like this using the different functionalities of the APIs.


  
  
 

    

