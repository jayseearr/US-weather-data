# US-weather-data
A database of weather information for the US pulled from public sources, plus the R code for reproducing the data set and for running some basic analysis. The data set is formatted as tidyverse-compatible data frames (tibbles). 

The repository is broken into a 'data' folder and a 'src' folder. The csv files in 'data' were generated using the R code in 'src'. 

Detailed file structure and content description is below. 

/src
+-- weather_data.Rmd - literate programming descriptions and definitions of the functions used to generate the data set and CSV files. 
+-- weather_data.R - all of the functions in used to generate the data files, plus analysis functions. 
/data
+-- US_monthly_normals_by_zip.csv
+-- US_sunrise_sunset_by_zip.csv

Monthly normals data contains the average Tmin and Tmax values for every month for each of the ~30,000 zip codes in the US (based on a weighted averaging of weather stations in or near the zip code).
The monthly normals data can be used to generate a temperature profile. This file has about 30,000 x 12 = ~500,000 data points. 

The sunrise and sunset data set is the sunrise and sunset times for each zip code for every day of thr year. Daylight savings time is not taken into account in this data. This data set has ~30,000 x 365 = ~10M data points.

The "location" of a zip code is defined as the geographic centroid of the polygon that surrounds the zip code, for purposes of this work. 


