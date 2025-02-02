
# **Mapping the World's Most Polluted Cities Using Folium and Geopy**  

## **Introduction**  
Air pollution is a growing environmental and public health concern worldwide. The Air Quality Index (AQI) is a standardized measure used to indicate air pollution levels in different cities. Higher AQI values indicate worse air quality, which can have severe health effects, particularly for vulnerable populations. In this study, we utilize geospatial mapping techniques to visualize the world's most polluted cities based on AQI rankings.  

## **Objectives**  
- To obtain the geographic coordinates (latitude and longitude) of highly polluted cities using geocoding techniques.  
- To visualize these cities on an interactive map with markers indicating their pollution severity.  
- To categorize and color-code the cities based on their pollution rank for better interpretation.  

## **Methodology**  

### **1. Data Collection**  
The dataset comprises 20 cities ranked based on their AQI values. The AQI metric is used to quantify pollution levels, with higher values indicating more severe air pollution. The dataset includes information on each city's name, country, rank, and AQI value.

### **2. Geocoding City Locations**  
To plot cities on a map, we need their geographic coordinates. The `geopy` library, specifically the `Nominatim` geocoder, is used to convert city and country names into latitude and longitude values. Since geocoding services enforce rate limits, a delay is introduced between requests to prevent API restrictions.  

### **3. Creating an Interactive Map Using Folium**  
The `folium` library is utilized to generate an interactive world map with the following features:  
- A global base map centered at an approximate coordinate ([20,0]) with a zoom level of 2.  
- Markers representing the 20 most polluted cities.  
- Color-coded markers based on city rankings:  
  - **Red** (Ranks 1-5): Most polluted cities  
  - **Blue** (Ranks 6-10): Highly polluted  
  - **Green** (Ranks 11-15): Moderately polluted  
  - **Purple** (Ranks 16-20): Least polluted in the top 20  

Each marker contains a pop-up displaying city-specific information, including the name, country, rank, and AQI. Additionally, a tooltip feature allows users to see the city name by hovering over a marker.

### **4. Adding a Custom Legend**  
To enhance readability, a legend is added to the lower-right corner of the map, providing a color-based categorization of city pollution ranks. This legend allows users to quickly interpret the severity of pollution levels.

## **Results & Discussion**  
By running this script, we generate an interactive map showcasing the world's most polluted cities. The visual representation of the data allows for easy interpretation of pollution distribution across different regions. Notably:  
- South Asia has a significant concentration of the most polluted cities, with **India, Bangladesh, and Pakistan** leading the rankings.  
- Cities in **China, Iran, and Russia** also feature in the top 20, highlighting pollution concerns in these regions.  
- The presence of cities from **Africa (Senegal) and the Middle East (Afghanistan, Turkey, Iran)** indicates that air pollution is a global issue.  

Such visualizations are valuable for policymakers, researchers, and the general public, as they provide insights into pollution hotspots and trends that can guide mitigation strategies.

## **Conclusion**  
This study demonstrates the power of geospatial tools in visualizing environmental issues such as air pollution. The combination of `geopy` for geocoding and `folium` for mapping allows for the creation of an intuitive and informative representation of real-world data. Future research could extend this analysis by incorporating real-time AQI data, analyzing seasonal variations, or integrating satellite-based pollution measurements.

