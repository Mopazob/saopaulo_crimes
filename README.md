# IBM Professional Data Science Certificate Final Project: Sao Paulo Crimes
Repo for part2 of capstone project from IBM Coursera Data Science Proffesional Certificate.

# Introduction: Business Problem
The focus of this project is to find a location for opening a safe comercial store in the city of Sao Paulo, Brazil. The report aims to different stakeholders interested in opening any business type. The first step will be to chose a safe borough, analysing the crimes and listing the amount of it committed per borough in Sao Paulo, where grocery stores are not amongst the most commom venues.

# About the data
We have the next tasks to do: Find the safest borough based on crime statistics in Saop Paulo, find the most common venues for stores and choose the right neighbourhood within the borough for a future safe store. I will be using the geographical coordinates of Sao Paulo, obtained from Kaggle, to plot the different neighbourhood, and finally cluster our neighborhoods and present our findings. The next steps and the data i will be using:

1. Data set from Kaggle containing the Sao Paulo crimes from 2010 to 2018. On this dataset, we have an data about crime incidents on Sao Paulo which specifies what has happened in the victim's view, as well as field indicating what objects were lost. Plus we have the location cords, so we can plot it.

2. Additional information of the list of officially categorized boroughs in Sao Paulo from Wikipedia. Borough information will be used to map the existing data where each neighbourhood can be assigned with the right borough.

3. Create a new dataset of the neighborhoods, crime data and the respective neighbourhood cords. This data will be bring us using Geopy to find the safest borough and explore the neighbourhood by plotting it on maps using folium and perform exploratory data analysis.

4. Re-do our dataset of the neighborhoods, and the most common venues and the respective neighbourhood along with property cords: Using Four Square API to explore the neighbourhood venues and to apply cluster algorithm to the neighbourhoods and present the findings by plotting it on maps using folium.

# Methodology

- Exploratoy Data Analysis : Visualise the crime repots in different Sao Paulo boroughs to idenity the safest borough and check the neighborhoods of that borough. We will Use the resulting data and find 10 most common venues in each neighborhood.

- Modeling : We will choose the right neighborhood within a borough. Next we will be clustering similar neighborhoods using K-means clustering which is a form of unsupervised machine learning algorithm that clusters data based on predefined cluster size. We will use K-Means clustering to address this problem so as to group data based on existing venues which will help in the decision making process.

# Analysis

1. First we can visualise the quantity of crimes among the Boroughs in Sao Paulo and then pick the safest ones. In this case we can see that NorthWest and East2 boroughs were the safest.

![](hhttps://github.com/Mopazob/saopaulo_crimes/blob/master/Saopaulo.boroughs.PNG)
