# sqlalchemy-challenge

## Step 1-Climate Analysis and Exploration

#### Precipitation Analysis- the code will

* retrieve the `date` and `prcp` values from the last 12 months of precipitation data (from the most recent date in the database).
* Calculate the average of these values to have a single `prcp` value per date.
* Load the query results into a Pandas DataFrame and set the index to the date column.
* Sort the DataFrame values by `date`.
* Plot the results using the DataFrame `plot` method

#### Station Analysis- the code will

* calculate the total number of stations.

*  list all stations with their corresponding observation count in descending order.

  - Which station is the most active (i.e., has the greatest number of observations)?

* retrieve the last 12 months of temperature observation data (TOBS) for the most active station.

  - Plot the results as a histogram with `bins=12`.

    

## Step 2 - Climate App

a Flask API is designed on queries from the previous part:

* ### Routes

  - `/api/v1.0/precipitation`
    - Returns dictionary using `date` as the key and `prcp` as the value.
  - `/api/v1.0/stations`
    - Returns a JSON list of stations from the dataset.
  - `/api/v1.0/tobs`
    - Returns a JSON list of temperature observations (TOBS) for the latest year.
  - `/api/v1.0/<start>` and `/api/v1.0/<start>/<end>`
    - returns the minimum temperature, the average temperature, and the max temperature for a given start or start-end range.
    - When given the start date only, calculates min, max, and avg for all dates greater than and equal to the start date.
    - When given the start and the end date, calculates the min, avg, and max for dates between the start and end date inclusive.
    - Return a JSONified dictionary of min, max, and avg temperatures.



 