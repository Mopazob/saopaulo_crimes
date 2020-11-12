# IBM Proffesional Data Science Certificate Final Project: Sao Paulo Crimes
Repo for part2 of capstone project from IBM Coursera Data Science Proffesional Certificate.

# Introduction: Business Problem
The focus of this project is to find a location for opening a safe comercial store in the city of Sao Paulo, Brazil. The report aims to different stakeholders interested in opening any business type. The first step will be to chose a safe borough, analysing the crimes and listing the amount of it committed per borough in Sao Paulo, where grocery stores are not amongst the most commom venues.

# About the data
We have the next tasks to do: Find the safest borough based on crime statistics in Saop Paulo, find the most common venues for stores abd choose the right neighbourhood within the borough for a future safe store. I will be using the geographical coordinates of Sao Paulo, obtained from Kaggle, to plot the different neighbourhood, and finally cluster our neighborhoods and present our findings. The next steps and the data i will be using:

1. Data set from Kaggle containing the Sao Paulo crimes from 2010 to 2018. On this dataset, we have an data about crime incidents on Sao Paulo which specifies what has happened in the victim's view, as well as field indicating what objects were lost. Plus we have the location cords, so we can plot it.

2. Additional information of the list of officially categorized boroughs in Sao Paulo from Wikipedia. Borough information will be used to map the existing data where each neighbourhood can be assigned with the right borough.

3. Create a new dataset of the neighborhoods, crime data and the respective neighbourhood cords. This data will be bring us using Geopy to find the safest borough and explore the neighbourhood by plotting it on maps using folium and perform exploratory data analysis.

4. Re-do our dataset of the neighborhoods, and the most common venues and the respective neighbourhood along with property cords: Using Four Square API to explore the neighbourhood venues and to apply cluster algorithm to the neighbourhoods and present the findings by plotting it on maps using folium.

