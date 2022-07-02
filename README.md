# Movies-ETL

## Overview

This analysis uses and ETL process to extract Wikipedia, Kaggle and MovieLens rating data, transform the datasets by cleaning them up and joining them together, and then load the cleaned dataset into a SQL database.

## Resources

    - Kaggle metadata(movies_metadata.csv), MovieLens ratings (ratings.csv) files, Wikipedia JSON file (wikipedia-movies)
    
## Results

### Deliverable-1

ETL function written to read the three resource files and convert to respective Pandas Dataframes.


    **Image-1: wiki_movies_df DataFrame


    **Image-2: kaggle_metadata DataFrame


    **Image-3: ratings DataFrame

### Deliverable-2

Extraction and transformation of Wikipedia data

    - TV shows filtered out and dataframe created.
    - IMDB IDs extracted and duplicate IDs dropped.
    - ETL function created for following:
        - Retain columns with non-null values.
        - Non-null box office data converted to string values.
        - Matched six elements of "form_one" of box office data.
        - Matched three elements of "form_two" of the box office data.
        - Columns cleaned in Wikipedia DataFrame.
        - Cleaned Wikipedia data converted to a Pandas DataFrame.


    **Image-4: wiki_movies_df DataFrame


    **Image-5: Columns from wiki_movies_df

### Deliverable-3

#### Extraction and Transformation of Kaggle Data

    - Cleaned Kaggle metadata
    - Merged Wikipedia and Kaggle DataFrames
    - Functions performed on merged DataFrames:
        - Dropped unecessary columns.
        - Missing Kaggle data filled using a function.
        - Filtered movies_df to keep specific columns.
        - Renamed movies_df columns.

#### Extraction and transformation of MovieLens ratings data

    - Cleaned ratings counts.
    - Merged cleaned ratings DataFrame with movies_df into movies_with_ratings_df.
    - Empty values in movies_with_ratings_df filled wiht "0"


    ** Image-6: movies_with_ratings_df DataFrame


    ** Image-7: movies_df DataFrame

### Deliverable-4

    - SQL movies table data replaced by movies_df data.

    ** Image-8: Row count of movies table

    - Data added to ratings table in SQL database from MovieLens rating CSV file.
    
    ** Image-9: Row count of ratings table

    - Displayed Elapsed time for adding data to the database.

    ** Image-10: Elapased time displayed


