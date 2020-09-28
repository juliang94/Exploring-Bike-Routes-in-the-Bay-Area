# Exploring Bike Routes in the Bay Area
## by Julian Gomez
Fourth and final project of the Data Analysis Nanodegree


## Dataset

> Provide basic information about your dataset in this section. If you selected your own dataset, make sure you note the source of your data and summarize any data wrangling steps that you performed before you started your exploration.

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

> Summarize all of your findings from your exploration here, whether you plan on bringing them into your explanatory presentation or not.


## Key Insights for Presentation

> Select one or two main threads from your exploration to polish up for your presentation. Note any changes in design from your exploration step here.
