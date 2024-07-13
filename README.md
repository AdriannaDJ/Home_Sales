# Home_Sales
Challenge 22

## Overview ##
This practice focused on exploring different techniques used in big data with a home sale dataset including: spark, caching, and parquet partitioning.
Four questions were answered. One of these questions was tested in all three techniques.

## Results ##
### Spark ###
A temporary view was created using a spark dataframe. Several questions were answered:
* What is the average price for a four-bedroom house sold for each year?
* What is the average price of a home for each year the home was built, that has three bedrooms and three bathrooms?
* What is the average price of a home for each year the home was built, that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet?
* What is the average price of a home per "view" rating having an average home price greater than or equal to $350,000?
    * The last question is tested in all three techniques
    * Run time: 1.71 seconds

### Caching ###
The temporary table for home_sales dataset was cached. The same query was run for the above question.
    * Run time: 0.58 seconds

### Parquet Partitioning ###
The home_sales dataset was formatted to parquet and was partitioned by date_built column. The same query was run for the above question.
    * Run time: 1.13 seconds

## Summary ##
For the home_sales dataset, the caching technique provided the quickest results at 0.58 seconds of run time. Partitioning with a parquet formatted dataset was second at a run time of 1.13 seconds, and spark temporary view was last with a run time of 1.71 seconds.

## Resources ##
* Referenced lesson activities from Module 22 Big Data.