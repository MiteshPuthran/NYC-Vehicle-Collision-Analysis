# NYC Vehicle Collision Dataset Analysis with National Oceanic and Atmospheric Administration(NOAA) weather dataset

![](images/nyc.jpg?raw=true)
![](images/NOAA_emblem.png?raw=true)
<br>
<br>
The data for the project analysis were downloaded from the following sites:
* Vehicle collision dataset has been downloaded from [NYC Open Data](https://opendata.cityofnewyork.us/) using **Socrata Open Data API** - **API Request**
* Weather dataset was downloaded from [NOAA Weather Data](https://www.ncdc.noaa.gov/cdo-web/search?datasetid=GHCND) where a selection has to be made for the date range and type of data needed for the analysis. The processing of the data takes 2-3 days depending on the type and size of data you are requesting - **CSV File**
<br>

## Data Collection and Processing

### Fetching the data
* For the vehicle collision data, the data is downloaded using the API token key obtained after registering in their website. The data is in the form of JSON file.
* The weather data is downloaded after recieving a email from NOAA Weather Data with the download link.
* The notations in the weather datset are as follows: PRCP = Precipitation (inches as per user preference, inches on Daily Form)
* SNOW = Snowfall (inches as per user preference, inches on Daily Form)
* SNWD = Snow depth (inches as per user preference, inches on Daily Form)

### Storing the data
* The downloaded vehicle collision data JSON files are stored according to the different boroughs of NewYork(Manhattan, Queens, etc) and their respective zip codes. You can view the respective folder structure [here](https://github.com/MITESHPUTHRANNEU/puthran_mitesh_spring2017/tree/master/Final%20Project/ProcessedData).
* The weather dataset has been stored as a CSV file.

### Converting and merging the downloaded data
* The vehicle colision JSON file have been converted into CSV file by checking for each key value pair and are stored [here](https://github.com/MITESHPUTHRANNEU/puthran_mitesh_spring2017/tree/master/Final%20Project/ProcessedData). 
* The data from both the datasets are merged using Panda dataframes by selecting the common _'DATE'_ column available in both.

### Starting the Analysis:
The following analysis were made using the merged dataset.
<br>
## Analysis 1:
## _Factors that caused maximum collision in whole NYC from 2015-2017_
Finding out the top 10 factors that caused collision in NYC by using factors like Contibuting Factor and Number of Persons killed.
<br>
![](GeneratedImages/factor.png?raw=true)
<br>
#### Steps for the analysis:
1. Reading the raw data from the CSV file.
2. Taking the total count of the persons killed by grouping the factors responsible for collision.
3. Removing unwanted column where factors are not specified.
4. Inserting the data into the dataframe with the factors and the corresponding number of people that were killed by the collision.
5. Saving the data from the dataframe to a CSV file.
6. Plotting a graph to display the factors for the same.
7. Saving the plotted graph as a PNG file.
#### Outputs of Analysis:
![](GeneratedImages/factortable.png?raw=true)
1. [CSV File - Factor.csv](https://github.com/MITESHPUTHRANNEU/puthran_mitesh_spring2017/tree/master/Final%20Project/GeneratedCSV).
2. [Plot Files - Factor.png](https://github.com/MITESHPUTHRANNEU/puthran_mitesh_spring2017/tree/master/Final%20Project/GeneratedImages).

## Analysis 2:
## _Vehicle type involved in collision and number of people killed at each borough of NYC from 2015-2017_
Finding out the top vehicle types that caused collision in each borough of NYC by using factors like Borough, Vehicle Type and Number of Persons killed.
<br>
![](GeneratedImages/vehicle.png?raw=true)
<br>
#### Steps for the analysis:
1. Reading the raw data from the CSV file.
2. Taking the total count of the persons killed by grouping the vehicle type and borough involved in collision.
3. Selecting the date range for the collisions.
4. Inserting the data into the dataframe with the borough, vehicle type and the corresponding number of people that were killed by the collision.
5. Saving the data from the dataframe to a CSV file.
6. Plotting a graph to display the vehicle type and number of people killed in each borough for the same. 
7. Saving the plotted graph as a PNG file.
#### Outputs of Analysis:
![](GeneratedImages/vehicletable.png?raw=true)
1. [CSV File - Vehicle.csv](https://github.com/MITESHPUTHRANNEU/puthran_mitesh_spring2017/tree/master/Final%20Project/GeneratedCSV).
2. [Plot Files - Vehicle.png](https://github.com/MITESHPUTHRANNEU/puthran_mitesh_spring2017/tree/master/Final%20Project/GeneratedImages).


## Analysis 3:
## _Snowfall and Rainfall in inches causing injury to people in NYC from 2015-2017_
Finding out the highest snowfall and rainfall in inches which caused maximum number of injuries  from collision to the people of NYC
<br>
![](GeneratedImages/snowinjury.png?raw=true)
![](GeneratedImages/raininjury.png?raw=true)
<br>
#### Steps for the analysis:
1. Reading the raw data from the CSV file.
2. Selecting the date range from the raw data to do analysis.
3. Converting the date column to datetime format.
4. Merging the data together and calculating the mean date from collision data as it includes multiple entries for a single day.
5. Grouping by snowfall and the total persons injured calculated by adding all the injuries.
6. Saving the data from the dataframe to a CSV file.
7. Plotting a graph to display the snowfall in inches and the number of injuries for the same.
8. Saving the plotted graph as a PNG file.
9. Following the same steps as above for rainfall analysis.
#### Outputs of Analysis:
1. [CSV File - Snowinjury.csv](https://github.com/MITESHPUTHRANNEU/puthran_mitesh_spring2017/tree/master/Final%20Project/GeneratedCSV).
2. [CSV File - Raininjury.csv](https://github.com/MITESHPUTHRANNEU/puthran_mitesh_spring2017/tree/master/Final%20Project/GeneratedCSV).
3. [Plot Files - Snowinjury.png](https://github.com/MITESHPUTHRANNEU/puthran_mitesh_spring2017/tree/master/Final%20Project/GeneratedImages).
4. [Plot Files - Raininjury.png](https://github.com/MITESHPUTHRANNEU/puthran_mitesh_spring2017/tree/master/Final%20Project/GeneratedImages).


![](images/programs_OpenData.png?raw=true,#center)
