# Exploring Bike Routes in the Bay Area
## by Julian Gomez
Fourth and final project of the Data Analysis Nanodegree


## Dataset

  The dataset for this project is trip data of Bay Wheels, a bike share service from Lyft in the San Francisco Bay Area. The data is publicly available in the [Lyft website](https://www.lyft.com/bikes/bay-wheels/system-data). The data for this analysis focuses on all bike trip records from the year 2019. The downloaded csv files contained monthly data so the wrangling process started by concatenating all 12 files into one. This dataframe consisted of 15 columns and over 2.5 million observations.

The variables in the dataset include:
- Trip Duration in seconds
- Start/End time and date
- Start/End station ID
- Start/End latitude and longitude
- Bike ID
- User Type (Subscriber or Customer)
- Bike Share for all (yes, no)
- Rental access method

  The data wrangling mostly consisted on handling missing and invalid values.        
  1 - Dropped observations with missing start/end station IDs.     
  
  2 - Dropped observations with missing bike share entries.      
  
  3 - Dropped latitude/longitude obsevations with coordinates of 0 as well as others that have a latitude greater than 38, which point to other locations. 
  
  4 - Dropped the rental access method columns since it was almost empty of data.      
  
  The cleaned dataset resulted in 14 columns and 2.2 million observations, which is a small decrease in data size. 
  
  The variable of interest in this dataset is the trip duration, which can be observed in both seconds and minutes. Also, the visualizations for this exploration will also involve spatial data visualization with Folium.

## Summary of Findings

- The distribution of the trip duration in seconds resuted in a heavily right-skewed distribution spanning up to 80000 seconds, which is about 22 hours. However, its log-transformed histogram showed a roughly symmetric and unimodal distribution. 
- About 82% of rides are from members subscribed to the Lyft app, while 18% are form customers who just go for single rides, which cost $3 per 15 minutes after $2 for the first half hour.
- The stations are mostly located in the eastern part of San Francisco as well as other cities in the Bay Area including Berkeley, Oakland, and San Jose.
- Since there are thousands of stations, I plotted the 15 most used in 2019. Most of these stations are in the areas surrounding Market St., one of the most famous places in the city. The most common bike stations include the Embarcadero at Sandome St, the San Francisco Ferry Building, the San FRancisco Caltrain, Motghomery BART Station, etc.
- I created a new variable named `route`, which is a combination of start station and end station name. Like the previous observation, I plotted the 15 most common routes. Among them include the San Francisco Ferry building to the Embarcadero at Sansome St and Market St. at 10th St to Powell St BART Station. Three of those routes are from outside San Francisco, one in central San Jose and two in Oakland.
- Of all rides in the data, less than 3% are round-trips where users leave their bikes at the same station they picked them up from.
- Bike durations for casual customers average 24 minutes and typically last 42 minutes while for subscribers, durations average 11 minutes and typically last 25 minutes.
- From a heatmap, I observed that the longest routes by average duration are round trips to the San Francisco Caltrain and Ferry Building. Time distributions are different comparing casual customers and subscribers.

## Key Insights for Presentation

- Although rare, trips with the largest average durations are round trips when it comes to the 15 most common start and end stations in 2019.

