# CitiBikeNYCAnalysis
Objective: Determine which hours and days are the busiest for optimal bike placement.

Citi Bike Data Set
Source – The source I used for this data was Kaggle and was based on Citi Bike. Kaggle is a trusted website so this source can be trusted.

Collection – The data was collected through company and usage-based data. Whenever anyone uses a Citi Bike the company can gather information from the customer’s app. This information can be geographical, time based, age of customer, and what customer type they fall into. There is a high chance the data is up to date with limited lag because of the data being immediately updated based on app usage.

Contents: This data is from riders from May 2013 to October 2013. Each observation has its own unique identifier. The day, start time, end times, trip duration, start station id, start station name, start station latitude, start station longitude, end station id, end station name, end station latitude, end station longitude, bike ID, birth year of rider, user type (Customer = 24-hour pass or 3-day pass user; subscriber = annual member), and gender (zero = unknown; 1 = male; 2 = female) are the characteristics available for each observation. There are 50,000 observations with a total of 18 characteristics.

Limitations: There is no rider specific ID so there is no way to determine if any riders had more then one trip. Also, the fact that there is only 50,000 observations leads to the possibility that not all rides were recorded or are included in this data set. 

Ethics: There are no ethical concerns because this data is public information that can be found on Citi Bike’s website and it states that they follow the NYCBS Data Use Policy and their Data License Agreement, so with both of those being followed there is no concern for breach of personal privacy,

Relevance: This data was provided in the CareerFoundry brief for this project, so I feel confident in it’s relevance to this project. 
Data Profile

Variable	Description	Time Variant/Invariant	Structured/Unstructured	Quantitative/Qualitative	Nominal/Ordinal/Discrete/Continuous
Trip_id	Trip ID	Invariant	Structured	Qualitative	Nominal
Bike_id	Bike ID	Invariant	Structured	Qualitative	Nominal
Weekday	Day of Week  of ride	Invariant	Structured	Quantitative	Discrete
Start_hour	Hour of ride	Invariant	Structured	Quantitative	Discrete
Start_time	Time ride began	Invariant	Structured	Quantitative	Discrete
Start_station_id	Station ID where bike was taken from	Invariant	Structured	Qualitative	Nominal
Start_station_name	Name of Station where bike was taken from	Invariant	Structured	Qualitative	Nominal
Start_station_latitude	Latitude of station where bike was taken from	Invariant	Structured	Quantitative	Continuous
Start_station_longitude	Longitude of station where bike was taken from	Invariant	Structured	Quantitative	Continuous
End_time	Time ride ended	Invariant	Structured	Quantitative	Discrete
End_station_id	ID of Station where bike was left	Invariant	Structured	Qualitative	Nominal
End_station_name	Name of station where bike was left	Invariant	Structured	Qualitative	Nominal
End_station_latitude	Latitude of station where bike was left	Invariant	Structured	Quantitative	Continuous
End_station_longitude	Longitude of station where bike was left	Invariant	Structured	Quantitative	Continuous
Trip_duration	Duration of ride in seconds	Invariant	Structured	Quantitative	Discrete
Subscriber	Indicator of if the rider was a subscriber or not	Variant	Structured	Qualitative	Ordinal
Birth_year	Year of birth of rider	Invariant	Structured	Quantitative	Ordinal
Gender	Gender of rider	Invariant	Structured	Quantitative	Discrete

Data Cleaning Measures
Wrangling
Columns Dropped	Renamed Columns	Columns Type Changed	Reason
	Changed weekday to day_of_week		Clarity
		Bike_id to string	Not necessary for descriptive statistics
Unnamed:0, Trip_id, Bike_id			Not necessary
Start time and end time		New columns for start and end time called start of ride and end of ride. Data type changed to datatime64	Change of data type was needed for analysis

Consistency Checks
Missing Values	Treatment	Duplicates	Inaccuracies
Birth year - 6979	Dropped		
		None	
	Cap will be 90 yrs old so 1923 and earlier will be removed		Some birth years are clearly incorrect and will need to be reviewed later.

Questions to consider:
1.	What day is the busiest? Time?
2.	What percent of riders are subscribers? Non-Subscribers?
3.	What stations are the busiest? Which are the least busy?
4.	What are the ages that use the bikes more frequently?

