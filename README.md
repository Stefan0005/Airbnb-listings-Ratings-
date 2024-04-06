Problem statement:

To Identify Factors Influencing Airbnb Listing Performance

The dataset contains information about Airbnb listings, including various attributes such as host details, property characteristics, location, and review scores, the problem is to analyze and identify the key factors that significantly impact the performance of listings on the platform. Performance metrics may include occupancy rates, and customer satisfaction ratings.

The aim is to help hosts help optimize their listings to attract more guests and enhance their overall experience. This analysis will provide actionable insights for hosts and Airbnb management to improve the platform's competitiveness and user satisfaction.

STEPS IN DATA CLEANING
1.	First the data was imported using pandas because of its alpha numerical nature, although there were some issues with the encoding format of the data set because one or more columns had conflicting data types. In order to fix this, we had to change the format from UTF-8 to Latin-1 (ISO-8859-1) in taking this step the data was imported successfully.
2.	The next step was to make an unaltered copy to ensure we can revert to the original copy in case of any errors or reference.
3.	Both tables were merged listings and Reviews tables 
4.	 Conducted a search for the percentage of missing or null values by column to determine based on the percentage which would be dropped or subsequently filled.
5.	Based on the findings the district column was dropped because it had the highest percentage of null values present.
6.	The null values in (host response time, host response rate, host acceptance rate, bedrooms, host since, host is super host, host total listing count, host has profile pic, host identity verified, reviews scores rating, reviews score accuracy, reviews score cleanliness, review scores check-in, reviews scores communication, reviews scores location, reviews scores values).
7.	The Name column was changed to Description because its content contained the detailed description of various listings instead of names of the owners of various listings.
8.	The null values were dropped in the new Description column.
9.	After consultation and collaborative engagements with stakeholders it was decided that the rows in the description column with the string (“Ã”) because it affected the integrity of the dataset.
10.	 The Location column was dropped to ensure the integrity and clean nature of the dataset, it was filled with too many inaccuracies.
11.	Ater this process the dataset was called to eyeball for integrity and ensure it has been cleaned properly. 
12.	The file was saved to CSV format.

DATA ANALYSIS: 

1.	(. Describe) was used to Calculate summary statistics such as mean, standard deviation, 25th percentile,75th and many more column by column.
2.	The scientific symbols in the data set were suppressed with (np.set_printoptions).
3.	The scatter plot was used to visualize the relationship between PRICE and PROPERTY TYPE.
4.	The date column was converted to proper date format 
5.	A function was defined to map months to weather seasons year round
6.	The various weather seasons were used to calculate the AVERAGE PRICE BY SEASONS.
7.	A bar char was then used to visualize the relationship between weather seasons and Average price.
8.	Given the nature of the data and some incomplete or missing metrics an attempt was made to calculate ‘Potential nights booked’ with a view to calculate occupancy rate.
9.	In calculating the Occupancy rate the column Reviews_scores_checkin was divided by Potential nights booked the result was multiplied by 100 to give an estimation of the Occupancy rate to the best of our ability.
10.	 The relationship between rental prices and property type was explored using the average price rate and property type and a scatter plot chart to visualize this.
11. Correlation between total review score and review score cleaniness was esabilshed using a correlation matrix.
12. After which visualizatio nwas handled using power bi.
