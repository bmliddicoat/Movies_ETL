# Movies_ETL

## Overview
Amazing Prime has been hosting a hackathon.  The goal is to data from both Wikipedia and Kaggle, combine them, and save them into a SQL database.  The objective is to refractor the original code to improve the database.  The main areas of improvement are creating an automated pipeline that takes in new data, performs the appropriate transformations, and loads the data into existing tables.  To accomplish this, Jupyter Notebook, Python and SQL will be used during the process of extract, transform and load (ETL).  

## Process
The first objective to ensure refactoring was to create a function test of the extract, transform and load.  The three databases were loaded using a function.  At first, I simply just used the pd.read_csv directly rather than using the argument of the function that I had developed.  I was able to go back and catch my error.  I altered my code to use wiki_file, kaggle_file and ratings_file as the arguements.  I converted the Wikipedia JSON, kaggle metadata, and MovieLens ratings files to a Pandas DataFrame. 

The second objective was to extract and transform the Wikipedia data. Python, Pandas, the ETL process were used extract and transform the Wikipedia data to merge it with the Kaggle metadata.  The goals were to filter out to tv shows,on-null box office data is converted to string values using the lambda and join functions, use of regular expressions for elements in box office data, columns within WikiPedia were cleaned(box office, budget, release date and running time) and cleaned version of Wikipedia data was converted into a Pandas DataFrame.

For the third objective, Python, Pandas, the ETL process, and code refactoring, extract and transform were used for the Kaggle metadata and MovieLens rating data, then convert the transformed data into separate DataFrames. These dataframes were then merged into one DataFrame called movies_df. 

The last objective was to convert the movies_df and rating to a SQl Database.  The movies_df was counted to have 6,052 rows and ratings table have 26,024,289 rows.  I was successful in the movies_df count but was not successful with ratings data.
 
