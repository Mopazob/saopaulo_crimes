# IBM Professional Data Science Certificate Final Project: Sao Paulo Crimes Overview
* Final project for IBM Coursera Data Science Professional Certificate.
* Found two safest locations for a commercial store in Sao Paulo starting from a crimes database. These boroughs are North West and East 2.
* This project aims to manage differents tools about data world and does not have a commercial focus. Theres many commercial studies that have to be done before taking the best decision for a commercial store location.
* Data from Kaggle platform.
* Applied unsupervised machine learning K-means algorithm clustering model for two boroughs of Sao Paulo.
* Used folium package and FourSquare API to explore these boroughs and segment them.

# Code and libraries used
* **Data from:** https://www.kaggle.com/danlessa/geospatial-sao-paulo-crime-database
* **Python version**: 3.8
* **Libraries**: pandas, numpy, matplotlib, seaborn, folium

# Business Problem
The focus of this project is to find a location for opening a safe commercial store in the city of Sao Paulo, Brazil. The report aims to different stakeholders interested in opening any business type. The first step will be clean the data for explore this next. After we have to to chose a safe borough, analysing the crimes and listing the amount of it committed per borough in Sao Paulo, where grocery stores are not amongst the most commom venues.

# About the data
We have the next tasks to do: Check if the data is clean, explore the data to understand the variables used, then find the safest borough based on crime statistics in Sao Paulo, find the most common venues for stores and choose the right neighbourhood within the borough for a future safe store. I will be using the geographical coordinates of Sao Paulo obtained from geocoder service, to plot the different neighborhoods, and finally cluster our neighborhoods and present our findings. 

This will be our data and the route:

1. Data set from Kaggle containing the Sao Paulo crimes from 2010 to 2018. On this dataset we have a data about crime incidents on Sao Paulo which specifies what has happened in the victim's view, as well as field indicating what objects were lost. Plus we have the location cords, so we can plot it.

2. Additional information of the list of officially categorized boroughs in Sao Paulo from Wikipedia. Borough information will be used to map the existing data where each neighborhood can be assigned with the right borough.

3. Create a new dataset of the neighborhoods, crime data and the respective neighborhood cords. This data will be bring us using Geopy to find the safest borough and explore the neighborhood by plotting it on maps using folium and perform exploratory data analysis.

4. Re-do our dataset of the neighborhoods, and the most common venues and the respective neighbourhood along with property cords: Using Four Square API to explore the neighbourhood venues and to apply cluster algorithm to the neighbourhoods and present the findings by plotting it on maps using folium.

# Methodology

- Exploratoy Data Analysis : Visualise the crime repots in different Sao Paulo boroughs to idenity the safest borough and check the neighborhoods of that borough. Looking for different types of analysis like which is then most common object robbed, what are the sex of the majority victims or what are the type of assault most used. We will Use the resulting data and find 10 most common venues in each neighborhood.

![](https://github.com/Mopazob/saopaulo_crimes/blob/master/images/type1.png)
![](https://github.com/Mopazob/saopaulo_crimes/blob/master/images/sex1.png)
![](https://github.com/Mopazob/saopaulo_crimes/blob/master/images/word.png)

- Modeling : We will choose the right neighborhood within a borough. Next we will be clustering similar neighborhoods using K-means clustering which is a form of unsupervised machine learning algorithm that clusters data based on predefined cluster size. We will use K-Means clustering to address this problem so as to group data based on existing venues which will help in the decision making process.

1. First we can visualise the quantity of crimes among the Boroughs in Sao Paulo and then pick the safest ones. In this case we can see that NorthWest and East2 boroughs were the safest.

![](https://github.com/Mopazob/saopaulo_crimes/blob/master/Saopaulo.boroughs.PNG)

2. Then I used **folium** library to visualize geographics details of these two boroughs in Sao Paulo. We clearly can see the North West and the East 2 borough in Sao Paulo.  I used latitude and longitude values to get the visual.

![](https://github.com/Mopazob/saopaulo_crimes/blob/master/mapa1.PNG)

3. Utilized **Foursquare API** to explore the boroughs and segment them. This helps to fetch top 10 venues around each neighborhood. Here is a head of the list Venues name, category, latitude and longitude informations from Forsquare API. 

![](https://github.com/Mopazob/saopaulo_crimes/blob/master/venues.PNG)

4. Foursquare returned 184 unique categories, then I created a table which shows list of top 10 venue category for each borough in below table.

![](https://github.com/Mopazob/saopaulo_crimes/blob/master/commonvenues.PNG)

# Results

- Using unsupervised learning K-means algorithm to cluster the boroughs. K-Means algorithm is one of the most common cluster method of unsupervised learning. I used this clusters and folium to make a map wich shows us the two boroughs already clustered.

![](https://github.com/Mopazob/saopaulo_crimes/blob/master/mapa2.PNG)

As I mentioned the objective of the problem was to help stakeholders to identify the safest borough in Sao Paulo, and an good neighborhood within the borough to set up a commercial store.

This has been achieved by first making use of Sao Paulo crime data to identify a safe borough with variety of neighborhoods for any type of business. After selecting the borough it was imperative to choose the right neighborhood where the commercial stores were not among venues in a close proximity to each other. We made this by grouping the neighborhoods into clusters to assist the stakeholders by providing them with relevant data about venues and safety of a given neighborhood.

Its clearly to see that venues like Bakery, Pizza Place and Gyms are the most crowded venues to go. This show us that some business of this three types will work in some of these neighborhoods. 

# Conclusions

* Looking the quantity of crimes committed in Sao Paulo wen can see that North West and East 2 are the last in this count so we can assume that this two are the safest.
* Checking the objects stolen in Sao Paulo phones are the most common one. Next we can see the "other" category which we can conclude that is relationed with cars stolen if we check the WordCloud made.
* Males are the most common victims of assaults in Sao Paulo with 60% of the cases.
* The quantity of crimes commited in Sao Paulo increase aproximatly three times between 5 pm and 11 pm.
* The most common type of assault are the type "2" with 5800 assaults followed by the type "1" with 2980 samples.
* Tried to figure what are these types of assaults but no pattern was shown in the WordClouds for the description and title of each type. The most common word were car and phone.
* The highest mean value of stolen objects by assult type are aproximatly 9.5k USD for assault type "9". If we check the WordCloud for this assault type we can assume a car theft for this type. 

We used the crime data to take a look of all neighborhoods of Sao Paulo and later categorized them into different boroughs, this helped us grouping the neighborhoods into boroughs and choose the safest boroughs first. We achieve this picking the two safest boroughs in Sao Paulo and then checking the most common venues for both. Finally we use K-means to cluster these two boroughs and this way we can take a look for choosing the best neighborhood for any type of commercial business.

Once we confirmed the borough the number of neighborhoods for consideration also comes down, we further shortlist the neighborhoods based on the common venues, to choose a neighborhood which best suits the business problem.

* If we check the top venues by neighborhoods we can see for Brasilandia neighborhood Bakeries are the top here with an 8% of venues. If our commercial store its a Bakery this might be not a good place because there are too many of this type.
* In almost all neighborhoods in these two boroughs bakeries are in the top 5 venues. Maybe neither of these two boroughs are good for a new bakery commercial store.
* Looking into the clustering model we can see that in North West borough all of the neighborhoods are in the first cluster. This means that all of these neighborhoods have a similar quantity of venues percentage.
* If our new commercial store type are not in the top ten venues for this cluster, might be a good idea to open this venue in North West borough.
* We can see an significant ammount of gym venues in all these neighborhoods. This explain why Brazil is considerated a country which promotes a healthy lifestyle.

Theres a lot of other conclusions that we can assume of this little proyect but this were which made me sense. Depends of what type of commercial store we want to open in Sao Paulo the conclusions might be different. I repeat this is a proyect which aims to manage variety of data tools and does not have a commercial focus.

Thank you for reading.

**Matias S. Opazo Barrientos.**
