# CS5010_Group8
## Semester Project Report
## by Amanda Maruca (), Allison Hansen (), Colin Warner (ynq9ya)


### INTRODUCTION

Our group decided to investigate patterns in submitted applications and ultimate decisions received by individuals seeking refugee status around the world. 

The United Nations defines a refugee as, “someone who is unable or unwilling to return to their country of origin owing to a well-founded fear of being persecuted for reasons of race, religion, nationality, membership of a particular social group, or political opinion.” 

In 2019, there were 2,245,378 applications filed across the world by individuals seeking refugee status in another country. This an incredibly large number of vulnerable people in our world seeking assistance, and it is important that other countries and individuals with the available resources offer their support. 

It is due to this responsibility that we believe countries and individuals have to support refugees around the world that we created a program that allows users to learn about the refugee landscape. A few practical use cases that we believe this program could help with are:

1.	Allow refugee case works to know which countries accept the highest percentage of refugees from each country so that they can advise families where to apply for refugee status. 
1.	Enable churches or nonprofits to understand which countries are seeing the most individuals applying for refugee status so that they can provide resources to the most vulnerable of our world. 
1.	Give churches or nonprofits insight into the demographics of the people arriving in their country as refugees so that they can design their services around serving the arriving population.
1.	Use time series to show policy makers trends in the number of refugees that each country accepts over time in order to identify when countries may be failing in their responsibility to care for the most vulnerable.

Below, we will dive deeper into the data set that we received from the United Nations and demonstrate the ways in which users can use our program to solve their problems. 


### DATA SET

The base datasets we use for our project are made available by the UN Refugee Agency, and can be obtained in CSV format from the following website: [UNHCR Refugee Statistics](https://www.unhcr.org/refugee-statistics/download/?url=2w5FZk). 

From this website, we were able to download the following primary datasets that would be read into our python file as a pandas data frame:

* Df_applications (66,113 rows, 7 variables) - Each row provides the number of refugee applications submitted for every country of origin, country of asylum, and year combination.
* Df_decisions (59,306 rows, 11 variables) - Each row provides the number of refugee applications that end up in each decision category for every country of origin, country of asylum, and year combination. Decision categories include Recognized, Complementary Protection, Rejected, and Otherwise Closed. 
* Df_demographics (62,447rows, 24 variables) – Each row provides the demographic information of the refugees accepted for every country of origin, country of asylum, and year combination.

After reading these files into pandas data frames, we were able to join them together using a newly created unique ID field. We created this ‘ID’ field to be a combination of the Country of Origin Code, Country of Asylum Code, and the Year. 

In addition to joining the tables together, we also had to decide what to do with blank values that were present in the country of origin columns. At first, we were planning to drop these rows altogether. However, we learned that it actually is possible for the country of origin to be unknown for an individual seeking asylum. We decided it is best to keep these rows in the data so as to not miss out on any insight regarding this population.

Ultimately, we ended up with a primary data set containing 34,760 rows. This data set was used as our launching point for other queries that feed into our data visualizations. 

One additional data set that is worth mentioning is our use of the geopandas ‘naturalearth’ dataset. We joined our original refugee data set to this source in order to access each country’s geolocation for plotting on the world map. An ancillary benefit to using the naturalearth data set was the inclusion of their population and gdp metrics that we can also layer into our visualizations. 

### EXPERIMENTAL DESIGN

Our project was based on an experimental design from the beginning. We studied the relationship between refugee locations and quantity of refugees. We started by identifying the top ten countries of origin and destination. We then studied further metrics on each country based on whether it was a top ten country of origin or asylum. We explored the potential statistics that could be displayed and chose a select few that were both meaningful and interesting. 

### RESULTS

Our results are largely interactive. While the program looks to highlight certain trends and statistical findings, the goal is to involve the user and allow 
the user to pose questions to the program. Thus, while our findings include the reporting of various numbers, statistics, aggregates, and graphs drom the data we compiled regarding world refugees, the findings are also open ended to many possibilities of what the program will enable the user to do to help refugees around the world by understanding patterns and demographics.

Below are a few examples of how each of the four users from our introduction may benefit from diving into both countries of asylum and countries of origin:

#### Country of Asylum Use Case - Germany 

1.	Refugee Case Workers: 
1.	Churches or Nonprofits:  
1.	Policy Makers:


#### Country of Origin Use Case - Venezuela 

1.	Refugee Case Workers: 
1.	Churches or Nonprofits:  
1.	Policy Makers:


### CONCLUSIONS


