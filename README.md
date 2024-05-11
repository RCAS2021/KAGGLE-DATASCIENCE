# KAGGLE-DATASCIENCE
Notebooks created while learning data science in Kaggle Learn.

To see the maps created in the notebooks, click on the button that says Open in Kaggle inside the .ipynb file preview

My profile on Kaggle:
https://www.kaggle.com/rafaelcruza
---|

# Geospatial Analysis Course on Kaggle:
The next notebooks are part of the Geospatial Analysis course on Kaggle:
https://www.kaggle.com/learn/geospatial-analysis
------|

### US VACCINE TRACKER
This exercise demonstrates how to create an interactive map to track the percentage of inhabitants vaccinated against COVID-19 for each state in the US. Here's a summary of what the code does:

1- Data Loading and Preprocessing: Two datasets are used - one containing population data for each state and another containing vaccination data. The vaccination data is cleaned to correct the state name for New York and merge it with the population data. The percentage of vaccinated population for each state is calculated.

2- Total Percentage Vaccinated: The total percentage of vaccinated population in the US is calculated.

3- Vaccination Percentage by State: The percentage of vaccinated population is calculated for each state. Additionally, the overall percentage vaccinated across all states is calculated.

4- Filtering States with Percentage Above 100%: Some states may have vaccination percentages above 100% due to discrepancies in the datasets or individuals being vaccinated in states other than their state of origin.

5- Creating a Choropleth Map: Using Folium, a choropleth map is created to visualize the vaccination percentage by state. The map displays the percentage of vaccinated population for each state, with a color gradient indicating different levels of vaccination coverage.

Overall, this exercise provides a practical example of using geospatial analysis techniques to visualize and analyze COVID-19 vaccination data at the state level in the US.
---|

### PROXIMITY ANALYSIS
This lesson focuses on analyzing motor vehicle collision data in New York City and understanding hospital coverage in response to these incidents.

1- Visualizing Collision Data: The first task involves visualizing major motor vehicle collisions in New York City from 2013 to 2018. Using the latitude and longitude coordinates provided in the dataset, an interactive map with marker clusters is created to visualize the collision data.

2- Understanding Hospital Coverage: Next, hospital locations in New York City are loaded and visualized on the map. This step provides insight into the distribution of hospitals across the city.

3- Identifying Distant Collisions: A buffer of 10 kilometers is created around each hospital to represent their coverage area. Collisions occurring outside of these buffer zones are identified, indicating instances where injured persons may be more than 10 kilometers away from the nearest hospital.

4- Recommending the Closest Hospital: A function is created to recommend the closest hospital to a given collision location. This function calculates the distances between the collision location and each hospital, selecting the hospital with the shortest distance.

5- Determining Highest Demand: Considering collisions occurring more than 10 kilometers away from the closest hospital, the hospital with the highest demand is identified based on the frequency of collisions nearby.

6- Recommending New Hospital Locations: Based on the analysis, two new hospital locations are proposed to reduce the percentage of collisions more than 10 kilometers away from the nearest hospital to less than ten percent. Proposed latitude and longitude coordinates for the new hospital locations are provided, and the impact of these new hospitals on the coverage area is visualized on the map.

By completing these exercises, I've gained valuable experience in geospatial analysis, including visualizing data, understanding spatial relationships, and making data-driven recommendations for infrastructure planning and emergency response.
---|

### MANIPULATING GEOSPATIAL DATA
In this exercise, the task was to explore potential locations for the next Starbucks Reserve Roastery in California. As a Starbucks big data analyst, the goal was to analyze county demographics to identify suitable areas for this expansion.

1- Geocoding Missing Locations: The first step involved identifying missing latitude and longitude values for Starbucks locations in Berkeley. Using the Nominatim geocoder, the missing values were filled in, ensuring the completeness of the dataset.

2- Visualizing Berkeley Locations: Once the missing locations were geocoded, the Berkeley locations were visualized on a map using markers. This visualization provided insight into the correctness of the newly added latitude and longitude values.

3- Consolidating Data: Various datasets, including county boundaries, population estimates, household income data, and median age information, were consolidated. This consolidation facilitated the calculation of population density and enabled further analysis.

4- Selecting Promising Counties: Leveraging the consolidated data, counties were selected based on specific criteria related to household income, median age, and population density. This selection aimed to identify counties with demographics conducive to Starbucks Reserve Roastery expansion.

5- Identifying Stores in Selected Counties: The analysis determined the number of Starbucks stores within the selected counties, providing insight into the availability of existing infrastructure in potential expansion locations.

6- Visualizing Store Locations: Finally, the identified store locations within the selected counties were visualized on a map using marker clusters, offering a clear overview of potential expansion areas.

Through these exercises, one could gain practical experience in geospatial analysis and data-driven decision-making, essential skills for strategic business planning in the retail sector.
---|

### INTERACTIVE MAPS
In this geospatial analysis lesson, I explored various aspects of earthquake vulnerability and population density in Japan. By applying geospatial analysis techniques to real-world data, I gained insights into the spatial relationships between seismic activity, tectonic plate boundaries, and population distribution.

1- Understanding Earthquake Patterns: Initially, I investigated the coincidence of earthquakes with tectonic plate boundaries globally. Through visualizations, I assessed whether seismic events tend to occur along plate boundaries, providing foundational insights into earthquake dynamics.

2- Analyzing Depth and Proximity: Next, I delved into the relationship between earthquake depth and proximity to plate boundaries, focusing particularly on Japan. By mapping earthquake depths relative to plate boundaries, I sought to uncover potential correlations that could inform seismic hazard assessments.

3- Identifying High-Density Areas: I then turned my attention to population density in Japanese prefectures. By creating choropleth maps, I visualized population density distributions, aiding in the identification of densely populated regions vulnerable to earthquake impacts.

4- Recommending Reinforcement Strategies: Finally, I integrated population density data with earthquake magnitude information to propose priority areas for earthquake reinforcement measures. Through spatial analysis, I identified prefectures most susceptible to high-magnitude earthquakes, facilitating targeted intervention strategies for urban safety planning.

Overall, this lesson equipped me with valuable geospatial analysis skills applicable to urban safety planning and disaster risk reduction efforts, contributing to my understanding of geographic information science and its practical applications.
---|

### COORDINATE REFERENCE SYSTEMS

In this exercise, I embarked on an exploration of purple martins' migration patterns, employing geospatial analysis techniques. Tracking the year-round movements of eleven purple martins via GPS data, my aim was to decipher their behaviors and potential interactions with protected areas in South America.

1- Data Setup: Initially, I ingested GPS data into a pandas DataFrame, swiftly transforming it into a GeoDataFrame to enable spatial analysis. Ensuring alignment with geographic coordinates, the GeoDataFrame was configured with the appropriate coordinate reference system (CRS).

2- Visualization: I embarked on visualizing purple martins' distribution across the Americas by juxtaposing their locations with country boundaries. This visual representation offered a preliminary insight into the extent of their geographical range.

3- Path Analysis: Delving deeper, I crafted GeoDataFrames to map the migration paths of individual birds. This granular analysis enabled a closer examination of their journeys, from inception to culmination.

4- Protected Areas: Venturing into assessing habitat preferences, I pinpointed and plotted the locations of protected areas in South America. Furthermore, I quantified the extent of South America's landmass safeguarded by protected areas, shedding light on potential conservation hotspots.

5- Final Visualization: Synthesizing all data layers, I generated a holistic map illustrating purple martins' presence in South America alongside protected areas. This comprehensive visualization fostered insights into habitat preferences and conservation implications for the species.

Through this immersive exercise, I honed my skills in applying geospatial analysis techniques to ecological research, fostering continuous growth in my learning journey on Kaggle.
---|

### YOUR FIRST MAP
In this exercise, I conducted geospatial analysis using Python libraries such as GeoPandas to investigate Kiva.org's loan distribution in the Philippines. 

Kiva.org is an online crowdfunding platform that extends financial services to underserved communities globally.

I went through these steps:

1- Data Loading and Visualization: Loaded shapefile data containing Kiva loan information and plotted loan locations across the world and within the Philippines using GeoPandas. This initial visualization provided insights into the geographical distribution of loans.

2- Focus on the Philippines: Narrowed down the analysis to loans based in the Philippines by creating a GeoDataFrame specifically for Philippine loans. This step facilitated a more targeted examination of loan distribution within the country.

3- Island-Level Analysis: Utilized additional shapefile data containing island boundaries of the Philippines to visualize loans at a more granular level. By overlaying loan locations onto the island boundaries, I identified specific islands where it might be beneficial to recruit new Field Partners for Kiva.

Overall, this exercise aimed to identify regions outside of Kiva's current network in the Philippines, with the goal of pinpointing opportunities for recruiting new Field Partners to expand Kiva's reach and impact in providing financial services to underserved communities.
---|

