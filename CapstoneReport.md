# Analysis of how the immigration demographics of a city effect its Restaurant cuisines #


### 1.0 Introction to the project ###


** 1.1 What will this project do?**
It is a well known fact that *immigration* has an impact on available *cuisines*, what this project tries to show is whether or not that impact is fully compatible with the data. 
1. How strongly do the two *relate*? 
2. Are there anomylous regions' cuisines that are not reflected within the population Toronto, Ca.

**1.2 How will we do this?**
We will do this by creating a simple *visualisation* of Venue type, based on *Foursquare* data that would be used to gain insights into the number of restaurants that are within each specific postal code. This woudld give an excellent blanket representation of Toronto's food scene and the make up of its *various cuisines*. and then plotting it with *Immigrant numbers* in the Toronto, Ca population. Both will be *normalised into a percentile* of total restaurants and total population respectively. 

**1.3 Who would be interested in this idea**
The audience of this analysis would be stakeholders in a *Restaurant chai*n that is looking *to diversify* their cuisines to reflect thier *customer demographic*. The Restaurant business is one fo the most clear cut cases of supply and demand in the economic word. By having a large macro overview of a city populations demographic comparing it to the relative amount of restaurants it would allow for a more informed decision when it comes to diversification. 


### 2.0 Description of Data, and how it will be used ###


**2.1 The Data that I will use**
The data that I will need to use is twofold. The first will be Immigration Data, that will be sourced from a Canadian Cencus (2016) and cleaned to show a simplified image of immigration from certain regions. 

I will then use Foursquare Venue data to gain an overview of the cuisines used in Toronto, by completing a search using postcodes and a 500m area surrounding thier longitude and latitudes. 

The hope will be that the combination of these two things will give me enough data to create a visually sturdy bar graph that will allow for a direct comparison. The problems that I may face is trying to seperate immigration and venue data into a large enough number of regions to produce a useable graph. 

**2.2 How will this data be used to solve my problem?**
This data will allow me to create a dataframe containing normalised percentiles of the venues' cuisines and immigrants' origin to visually compare the two ideas. This will then allow us to determine whether there is any correlation. If I am able to create a graph that shows genuine immigration demographics and genuine cuisine demographics in a comparable manner I should be able to visually determing whether the ideas that this project are based on are true and make statements about whether or not certain regions


### 3.0 Methodology ###

**3.1 Getting data for population of Immigrants within Toronto, Ca**
In order to find the percentile amount of Immigrants in Toronto I had to use the website ww12.statcan.gc.ca in order to view the 2016 Canadian Cencus. This allowed me to get a large dataset that contained the total number of immigrants from each of the continents and then process them, using numpy and pandas into a dataframe giving an ethnic demographic of Torono.

I also computed the total number of Non-Immigrants through the subtraction of total immigrants from the total population of Toronto. 

I finished this dataframe by converting each population into a percentage of the total population, allowing me to use this normalised values to compare to the normalised number of venues, which i will discuss next. 

https://www12.statcan.gc.ca/census-recensement/2016/dp-pd/prof/details/page.cfm?Lang=E&Geo1=CSD&Code1=3520005&Geo2=PR&Code2=01&SearchText=&SearchType=Begins&SearchPR=01&B1=Immigration%20and%20citizenship&TABID=1&type=0

**3.2 Getting data for the number of vanues of various cuisines**
I then had to gather data from Foursquare on venues. I used a dataset that contained the latitudes and longitudes of each postcode, before cleaning the data into a usable format. 

I then continued on to create a simplified dataframe which contained the total number of restaurants from each continent, using the sum function.

I then normalised this data into a percentile amount of the total venues recorded, this allowed me to compare these values to those of percetile population.

**3.3 creating a single dataframe that allows you to compare the two**
The final stage of my data processing was to merge the two dataframes to create one dataframe that allowed me to view the two in tandem, allowing me to visually discern ideas.

**3.4 Visualisation of my data**
My next task was to visually compare the two. This is perhaps the most important part of my project as I am not seeking a specific answer (IE I am looking at a trend as oppossed to definitive answer).

I therefore produced two graphs that allow me to compare with only immigrants, in order to view whether the percentile of venues correlated to the number of immigrants, and a graph that included Non-Immigrants, in order to determine whether the native Canadian cuisine was relevant in the number of Restaurants. It also allowed us to create a comparison to determine whether it was as simple as the demographic of the city or wether it was specifically about immigration. 


### 4.0 Results ###

The results were reasonably clear in indicating that the number of immigrants compared to venues was positively correlated. Whenever the immigrant population was higher, so too was the perntage of venues. 

fig.1 ![](fig1.png)

As you can see, the large population of Non-Immigrants had a relitively little impact on the number of restaurants, in fact being half of the relative size, making up 21% of the venues and 52% of the population.

fig.2 ![](fig2.png)

By taking out the large population of Non-Immigrants You can clearly see that the trend is very clearly relational with the number of immigrants in the population. This trend is consistent, however the amount of venues compared to the amount of population varies slightly, suggesting a more complicated relationship.

### 5.0 Discussion of Results###

As can be clearly seen, the relationship between immigration and restaurant cuisines are very definitely related. The simple fact that the higher the percentage that particular demographic represents the higher the demand for their respective cuisine.

However this simplistic aalysis disproves the idea that the varience of a cuisine is based on the percentage of the population that it represents. If that was the case the local Non-Immigrants cuisines would be far higher, however as seen in fig.2 this is not the case. It suggests that the relationship is far more complex, with the immigration to Canada and Toronto pushing the creation itself of Restaurants of similar cuisine.

It also shows a huge amount of European origin Restaurants when compared to the relative population. This would assumedly be caused by the high level of ethnic origin of Non-Immigrant canadians, being of European descent due to the French and British Occupation of North America. 

A final layer that may be extracted is the lack of venues for small immigrant populations. For instance the African and Oceania communities have shown to have virtually no restaurants in widespread use, despite having discernable populations (African moreso than Oceanian) which would suggest that despite the fact that immigrant pushes the creation of resturants with familiar cuisines you may have a cultural delay is it creates a larger apeal within the wider population.

### 6.0 Conclusion ###

In conclusion this analysis has shown that we have a very clear relationship between immigrant populatioin and relative cuisines however further analysis would be required to try and identify the size of the relationship and whether there are more nuanced cultural ideas in play.