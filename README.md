# KAGGLE-DATASCIENCE
Notebooks created while learning data science in Kaggle Learn.

To see the maps created in the notebooks, enter my profile, then code, then select the notebook to view it.

My profile on Kaggle:
https://www.kaggle.com/rafaelcruza
---|

---

# 1. Data Cleaning
The next notebooks are part of the Data Cleaning course on Kaggle:
[Data Cleaning on Kaggle](https://www.kaggle.com/learn/data-cleaning)
---|

## 1.1 Handling Missing Values
In this exercise, I worked with the San Francisco Building Permits dataset to practice handling missing values.

1. Data Exploration: I began by loading the dataset and examining its structure. The dataset contained several columns with missing values, such as "Street Number Suffix", "Proposed Construction Type", and "Site Permit".

2. Identifying Missing Data: I calculated the percentage of missing values in the dataset. It was found that approximately 26.26% of the values were missing.

3. Understanding Missing Data: I analyzed the columns "Street Number Suffix" and "Zipcode" to understand why data was missing. It was determined that missing values in the "Street Number Suffix" column likely indicated non-existence, while missing values in the "Zipcode" column were due to lack of recording.

4. Handling Missing Data: I experimented with different methods to handle missing values. I dropped all rows with missing values, resulting in no rows remaining in the dataset. Additionally, I dropped columns with missing values, removing 31 columns from the original dataset. Finally, I filled missing values using a backward fill method followed by replacing remaining missing values with zeros.

5. Further Practice: The exercise concluded with suggestions for further practice, including exploring scikit-learn's imputer for handling missing values and considering additional datasets to impute missing zip codes.

Overall, this exercise provided hands-on experience in identifying, understanding, and handling missing data in a real-world dataset.
---|

## 1.2 Scaling and Normalization
In this exercise, I practiced scaling and normalization using a dataset of Kickstarter campaigns.

1. Scaling Goals: I began by scaling the "usd_goal_real" column to values between 0 and 1 using min-max scaling. The original and scaled data were compared to understand the transformation. Then, I applied the same scaling to the "goal" column.

2. Normalization of Pledges: Next, I normalized the amount of money pledged to each campaign using the Box-Cox transformation. Positive pledges were selected, and then normalization was performed. The original and normalized data were compared, and it was observed that the distributions looked mostly the same for both "usd_pledged_real" and "pledged" columns after normalization.

Overall, this exercise provided hands-on experience in scaling and normalization techniques, essential for preparing data for analysis, especially in scenarios like regression analysis.
---|

## 1.3 Parsing Dates
In this exercise, I applied what I've learned in the Parsing dates tutorial.:

1. Checked the data type of the "Date" column in the earthquakes DataFrame, finding that it contains dates represented as strings with dtype "object".

2. Converted the "Date" column to datetime format, addressing the issue of different date formats in some entries by amending them before parsing.

3. Created a new column named "date_parsed" containing correctly parsed dates.

4. Extracted the day of the month from the "date_parsed" column to create a Pandas Series named "day_of_month_earthquakes".

5. Plotted the distribution of days of the month from the earthquake dataset to visualize the date parsing.

Overall, these steps helped ensure the accurate parsing of dates in the earthquakes dataset, enabling further analysis and visualization of temporal patterns.
---|

## 1.4 Character Encodings
In this exercise, I applied what I learned in the Character encodings tutorial.

1. Understanding Encodings: I began by working with a dataset composed of bytes and examined a sample entry to identify its encoding. This step helped me understand the importance of correctly specifying encodings when dealing with text data.

2. Reading Files with Encoding Problems: Next, I encountered a file with encoding issues and used the charset_normalizer module to detect the correct encoding. By determining the correct encoding (windows-1250), I successfully read the file into a DataFrame, ensuring that the text data was interpreted accurately.

3. Saving Files with UTF-8 Encoding: Finally, I saved a version of the police killings dataset to CSV with UTF-8 encoding. This step ensures compatibility and prevents encoding-related issues when sharing or further processing the data.

By addressing encoding challenges and ensuring that text data is correctly encoded, I set the foundation for seamless data processing and analysis, reducing the risk of errors and inconsistencies in the dataset.
---|

## 1.5 Inconsistent Data Entry
In this exercise, I applied the concepts learned in the Inconsistent data entry tutorial to clean up inconsistencies in a dataset.

1. Examine another Column: Initially, I examined the "Graduated from" column to identify any inconsistencies. I observed various entries with white spaces at the beginning and end of cells, which could lead to data inconsistencies.

2. Text Pre-processing: To address the white space inconsistencies, I performed text pre-processing by removing leading and trailing white spaces from every entry in the "Graduated from" column.

3. Continued Working with Countries: I revisited the "Country" column, which was previously cleaned for inconsistencies. However, I noticed that "usa" and "usofa" should represent the same country. To rectify this, I used fuzzy string matching to identify similar strings and replaced "usofa" with "usa" in the "Country" column.

By implementing these steps, I ensured that the dataset was cleaned of inconsistencies, facilitating accurate analysis and interpretation of the data.
---|

---

# 2. Geospatial Analysis Course on Kaggle:
The next notebooks are part of the Geospatial Analysis course on Kaggle:
[Geospatial Analysis on Kaggle](https://www.kaggle.com/learn/geospatial-analysis)
---|

## 2.1 Your First Map
In this exercise, I conducted geospatial analysis using Python libraries such as GeoPandas to investigate Kiva.org's loan distribution in the Philippines. 

Kiva.org is an online crowdfunding platform that extends financial services to underserved communities globally.

I went through these steps:

1. Data Loading and Visualization: Loaded shapefile data containing Kiva loan information and plotted loan locations across the world and within the Philippines using GeoPandas. This initial visualization provided insights into the geographical distribution of loans.

2. Focus on the Philippines: Narrowed down the analysis to loans based in the Philippines by creating a GeoDataFrame specifically for Philippine loans. This step facilitated a more targeted examination of loan distribution within the country.

3. Island-Level Analysis: Utilized additional shapefile data containing island boundaries of the Philippines to visualize loans at a more granular level. By overlaying loan locations onto the island boundaries, I identified specific islands where it might be beneficial to recruit new Field Partners for Kiva.

Overall, this exercise aimed to identify regions outside of Kiva's current network in the Philippines, with the goal of pinpointing opportunities for recruiting new Field Partners to expand Kiva's reach and impact in providing financial services to underserved communities.
---|

## 2.2 Coordinate Reference Systems

In this exercise, I embarked on an exploration of purple martins' migration patterns, employing geospatial analysis techniques. Tracking the year-round movements of eleven purple martins via GPS data, my aim was to decipher their behaviors and potential interactions with protected areas in South America.

1. Data Setup: Initially, I ingested GPS data into a pandas DataFrame, swiftly transforming it into a GeoDataFrame to enable spatial analysis. Ensuring alignment with geographic coordinates, the GeoDataFrame was configured with the appropriate coordinate reference system (CRS).

2. Visualization: I embarked on visualizing purple martins' distribution across the Americas by juxtaposing their locations with country boundaries. This visual representation offered a preliminary insight into the extent of their geographical range.

3. Path Analysis: Delving deeper, I crafted GeoDataFrames to map the migration paths of individual birds. This granular analysis enabled a closer examination of their journeys, from inception to culmination.

4. Protected Areas: Venturing into assessing habitat preferences, I pinpointed and plotted the locations of protected areas in South America. Furthermore, I quantified the extent of South America's landmass safeguarded by protected areas, shedding light on potential conservation hotspots.

5. Final Visualization: Synthesizing all data layers, I generated a holistic map illustrating purple martins' presence in South America alongside protected areas. This comprehensive visualization fostered insights into habitat preferences and conservation implications for the species.

Through this immersive exercise, I honed my skills in applying geospatial analysis techniques to ecological research, fostering continuous growth in my learning journey on Kaggle.
---|

## 2.3 Interactive Maps
In this geospatial analysis lesson, I explored various aspects of earthquake vulnerability and population density in Japan. By applying geospatial analysis techniques to real-world data, I gained insights into the spatial relationships between seismic activity, tectonic plate boundaries, and population distribution.

1. Understanding Earthquake Patterns: Initially, I investigated the coincidence of earthquakes with tectonic plate boundaries globally. Through visualizations, I assessed whether seismic events tend to occur along plate boundaries, providing foundational insights into earthquake dynamics.

2. Analyzing Depth and Proximity: Next, I delved into the relationship between earthquake depth and proximity to plate boundaries, focusing particularly on Japan. By mapping earthquake depths relative to plate boundaries, I sought to uncover potential correlations that could inform seismic hazard assessments.

3. Identifying High-Density Areas: I then turned my attention to population density in Japanese prefectures. By creating choropleth maps, I visualized population density distributions, aiding in the identification of densely populated regions vulnerable to earthquake impacts.

4. Recommending Reinforcement Strategies: Finally, I integrated population density data with earthquake magnitude information to propose priority areas for earthquake reinforcement measures. Through spatial analysis, I identified prefectures most susceptible to high-magnitude earthquakes, facilitating targeted intervention strategies for urban safety planning.

Overall, this lesson equipped me with valuable geospatial analysis skills applicable to urban safety planning and disaster risk reduction efforts, contributing to my understanding of geographic information science and its practical applications.
---|

## 2.4 Manipulating Geospatial Data
In this exercise, the task was to explore potential locations for the next Starbucks Reserve Roastery in California. As a Starbucks big data analyst, the goal was to analyze county demographics to identify suitable areas for this expansion.

1. Geocoding Missing Locations: The first step involved identifying missing latitude and longitude values for Starbucks locations in Berkeley. Using the Nominatim geocoder, the missing values were filled in, ensuring the completeness of the dataset.

2. Visualizing Berkeley Locations: Once the missing locations were geocoded, the Berkeley locations were visualized on a map using markers. This visualization provided insight into the correctness of the newly added latitude and longitude values.

3. Consolidating Data: Various datasets, including county boundaries, population estimates, household income data, and median age information, were consolidated. This consolidation facilitated the calculation of population density and enabled further analysis.

4. Selecting Promising Counties: Leveraging the consolidated data, counties were selected based on specific criteria related to household income, median age, and population density. This selection aimed to identify counties with demographics conducive to Starbucks Reserve Roastery expansion.

5. Identifying Stores in Selected Counties: The analysis determined the number of Starbucks stores within the selected counties, providing insight into the availability of existing infrastructure in potential expansion locations.

6. Visualizing Store Locations: Finally, the identified store locations within the selected counties were visualized on a map using marker clusters, offering a clear overview of potential expansion areas.

Through these exercises, one could gain practical experience in geospatial analysis and data-driven decision-making, essential skills for strategic business planning in the retail sector.
---|

## 2.5 Proximity Analysis
This lesson focuses on analyzing motor vehicle collision data in New York City and understanding hospital coverage in response to these incidents.

1. Visualizing Collision Data: The first task involves visualizing major motor vehicle collisions in New York City from 2013 to 2018. Using the latitude and longitude coordinates provided in the dataset, an interactive map with marker clusters is created to visualize the collision data.

2. Understanding Hospital Coverage: Next, hospital locations in New York City are loaded and visualized on the map. This step provides insight into the distribution of hospitals across the city.

3. Identifying Distant Collisions: A buffer of 10 kilometers is created around each hospital to represent their coverage area. Collisions occurring outside of these buffer zones are identified, indicating instances where injured persons may be more than 10 kilometers away from the nearest hospital.

4. Recommending the Closest Hospital: A function is created to recommend the closest hospital to a given collision location. This function calculates the distances between the collision location and each hospital, selecting the hospital with the shortest distance.

5. Determining Highest Demand: Considering collisions occurring more than 10 kilometers away from the closest hospital, the hospital with the highest demand is identified based on the frequency of collisions nearby.

6. Recommending New Hospital Locations: Based on the analysis, two new hospital locations are proposed to reduce the percentage of collisions more than 10 kilometers away from the nearest hospital to less than ten percent. Proposed latitude and longitude coordinates for the new hospital locations are provided, and the impact of these new hospitals on the coverage area is visualized on the map.

By completing these exercises, I've gained valuable experience in geospatial analysis, including visualizing data, understanding spatial relationships, and making data-driven recommendations for infrastructure planning and emergency response.
---|

## 2.6 US Vaccine Tracker
This exercise demonstrates how to create an interactive map to track the percentage of inhabitants vaccinated against COVID-19 for each state in the US. Here's a summary of what the code does:

1. Data Loading and Preprocessing: Two datasets are used - one containing population data for each state and another containing vaccination data. The vaccination data is cleaned to correct the state name for New York and merge it with the population data. The percentage of vaccinated population for each state is calculated.

2. Total Percentage Vaccinated: The total percentage of vaccinated population in the US is calculated.

3. Vaccination Percentage by State: The percentage of vaccinated population is calculated for each state. Additionally, the overall percentage vaccinated across all states is calculated.

4. Filtering States with Percentage Above 100%: Some states may have vaccination percentages above 100% due to discrepancies in the datasets or individuals being vaccinated in states other than their state of origin.

5. Creating a Choropleth Map: Using Folium, a choropleth map is created to visualize the vaccination percentage by state. The map displays the percentage of vaccinated population for each state, with a color gradient indicating different levels of vaccination coverage.

Overall, this exercise provides a practical example of using geospatial analysis techniques to visualize and analyze COVID-19 vaccination data at the state level in the US.
---|






