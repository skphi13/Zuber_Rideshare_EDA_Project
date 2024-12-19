# Zuber_Rideshare_EDA_Project
In this project, I conducted an exploratory and statistical analysis to find patterns from the multiple datasets from Zuber, a ridesharing company in Chicago, and from parsing data from [Zuber Data](https://practicum-content.s3.us-west-1.amazonaws.com/data-analyst-eng/moved_chicago_weather_2017.html). After data cleanup, I tested the following hypothesis:

Duration of rides from the Loop to O'Hare International Airport changes on rainy Saturdays.

# Data Description
A database with info on taxi rides in Chicago:

`neighborhoods table`: data on city neighborhoods

- name: name of the neighborhood
- neighborhood_id: neighborhood code

`cabs table`: data on taxis

- cab_id: vehicle code
- vehicle_id: the vehicle's technical ID
- company_name: the company that owns the vehicle

`trips table`: data on rides

- trip_id: ride code
- cab_id: code of the vehicle operating the ride
- start_ts: date and time of the beginning of the ride (time rounded to the hour)
- end_ts: date and time of the end of the ride (time rounded to the hour)
- duration_seconds: ride duration in seconds
- distance_miles: ride distance in miles
- pickup_location_id: pickup neighborhood code
- dropoff_location_id: dropoff neighborhood code
- weather_records table: data on weather

`record_id`: weather record code
- ts: record date and time (time rounded to the hour)
- temperature: temperature when the record was taken
- description: brief description of weather conditions, e.g. "light rain" or "scattered clouds"


# Conclusion
After conducting our EDA and SDA on the data that we obtained we discovered many useful insights.

**Results:**

T-statistic: 7.186
P-value: 6.739e-12

Given the extremely low P-value, which is much smaller than any common significance level (e.g., 0.05), we reject the null hypothesis. This means that there is strong evidence to suggest that the duration of rides from the Loop to O'Hare International Airport does indeed change on rainy Saturdays.


The hypothesis test indicates that weather, particularly rain on Saturdays, has a statistically significant impact on the duration of rides from the Loop to O'Hare International Airport. This finding suggests that rainy conditions likely lead to longer travel times, possibly due to factors like slower traffic or increased caution by drivers. This insight could be crucial for Zuber's operational planning, especially in forecasting ride durations and managing customer expectations during inclement weather.
