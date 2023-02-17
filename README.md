# Python-Data-Engineering---Pyspark
Transforming datasets in pyspark to achieve the desired results.


Datasets used <br />
https://www.kaggle.com/shivamb/netflix-shows <br />
https://www.kaggle.com/shivamb/amazon-prime-movies-and-tv-shows  <br />
https://www.kaggle.com/shivamb/disney-movies-and-tv-shows <br />


Operations performed

- File loaded as csv file into pyspark before applying some transformations and then outputting it to a parquet dataset. 
- filter out all records which are TV Shows - we’re only interested in films
- cast the date added to the format yyyy-mm-dd e.g. 2018-01-13
- rename the date_added column to airing_date
- add a new column ‘streaming_service’ to all entries with the value ‘Netflix’,'Amazon', 'Disney'
- create new column ‘adult’ which will be True for all entries with a rating of ‘TV-MA’ or ‘R’ and False otherwise
- create new column ‘american’ which will be True for entries with a country of ‘United States’ and False for all other values (including US or only US ? - Alin)
- keep only the following columns
    title
    director
    airing_date
    country
    adult
    american
    streaming_service
    runtime
- you’ll need to adapt the amazon and disney duration columns to match the format of the netflix column
i.e. in netflix, the runtime column is split into < 30 minutes, 1-2 hour, > 2 hrs (missing 30-60 mins also in Netflix it isn’t like that)
- Append all files together
