# Movies-ETL

## Overview

For our 8th data analytics project, we created an ETL process using Pandas dataframes, Jupyter Notebooks, and SQLAlchemy.  We pulled data from a variety of sources, imported the data into Pandas dataframes, used our python skills to clean up and transform the data, and finally imported the cleaned data into our PostgreSQL database.  

## Results

The final product resulted in a cleaned movies table.  Our python function is setup such that in can be run multiple times and will replace the table each time and insert the new data in it.
![Movies Table Import](/movies_query.png) 

We also imported the very large ratings file into our database.  To accomplish this, we divided the data into chuncks and imported it into our database 1 million records at a time.  I added a line of code to check if the iteration through the chunks was the first one, and if so it replaces the table, if not it appends the data to the existing table, that prevented the table from getting overwritten each time and ending with only the last chunk available.  

![Ratings Table Import](/ratings_query.png) 