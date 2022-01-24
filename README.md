## **Improving Access to NYC Health + Hospital Centers**

By Devra Alper



#### **Abstract**

This analysis seeks to identify accessible, high-traffic MTA stations that do not have NYC Health & Hospital (H+H) centers nearby. Results will recommend areas in need of H+H centers, which will improve patient compliance with less “no show” or late arrivals to appointments. This will of course also benefit those who require use of a wheelchair or other assistive devices, and/or are unable to manage stairs. Analysis originally limited proximity to ¼ mile radius; however, data indicates greater need in areas of less proximity.

#### **Design**

Three datasets inclusive of MTA turnstile data, accessible MTA stations with latitude and longitude, and H+H center location data were cleaned. The MTA turnstile data was filtered for only accessible stations, then sorted by high-traffic stations. Latitude and longitude information was then merged onto this filtered dataset. Haversine distance was calculated between all H+H centers and accessible MTA stations.

#### **Data**

The resulting dataset includes accessible MTA stations, organized by sum of daily entries between March 2021 - June 2021, and by distance from its nearest H+H center. While ¼ mile distance was presumed to be a tolerable distance to travel for those with limited mobility, one must consider that bus and other transportation options exist to fill the gap; only 9 of 99 accessible stations were within ¼ mile distance from its nearest H+H center. Data was then filtered to include only stations that did not have an H+H center <2 miles away. Nine stations fulfilled this criteria.

#### **Algorithms**

1. Combine MTA turnstile data in SQL, then open in Jupyter notebook

2. Clean MTA turnstile data

3. Clean accessible MTA data

4. Filter MTA turnstile data for only accessible stations

5. Calculate sum of daily entries

6. Merge latitude and longitude information

7. Clean H+H data, inclusive of latitude and longitude information

8. Calculate distance between accessible stations and H+H centers

#### **Tools**

- Pandas - analyses
- NumPy - analyses
- Scikit-learn - calculate haversine distance
- Matplotlib - visualizations
- Seaborn - visualizations
- Plotly - visualizations

#### **Communication**

Visualizations include two bar graphs. The first graph visualizes 10 accessible stations that are closest to an H+H center with a colormap indicating the sum of daily entries per station. The second bar graph visualizes the accessible stations that do not have an H+H center less than 2 miles away, also presented with a colormap of entries. Plotly was then used to visualize the distance between these stations and their nearest H+H center on a map.
