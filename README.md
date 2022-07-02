# Movies-ETL

## Overview

This analysis uses and ETL process to extract Wikipedia, Kaggle and MovieLens rating data, transform the datasets by cleaning them up and joining them together, and then load the cleaned dataset into a SQL database.

## Resources

    - Kaggle metadata(movies_metadata.csv) 
    - MovieLens ratings (ratings.csv) 
    - Wikipedia JSON file (wikipedia-movies)
    
## Results

### Deliverable-1

ETL function written to read the three resource files and convert to respective Pandas Dataframes.

    Image-1: wiki_movies_df DataFrame

  ![wiki_movies_df](https://user-images.githubusercontent.com/104603128/176983061-200eb8c9-b07c-4fb0-bd72-33f5b411e2b4.png)


    Image-2: kaggle_metadata DataFrame

  ![kaggle_metadata](https://user-images.githubusercontent.com/104603128/176983079-a2b59321-32d3-4341-adfd-e37cd8c0fded.png)


    Image-3: ratings DataFrame

  ![ratings](https://user-images.githubusercontent.com/104603128/176983095-9e89ab85-cb44-4cc3-8f15-eb02129922a0.png)


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


    Image-4: wiki_movies_df DataFrame

  ![wiki_movies_df_2](https://user-images.githubusercontent.com/104603128/176983115-766c5059-337a-4434-97db-e3dbcf7e67b9.png)


    Image-5: Columns from wiki_movies_df

  ![wiki_movies_df_columns](https://user-images.githubusercontent.com/104603128/176983120-a504d37b-d980-4b4c-af2b-c9df71e2174e.png)


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


    Image-6: movies_with_ratings_df DataFrame

  ![movies_with_ratings_df](https://user-images.githubusercontent.com/104603128/176983131-6e2f1d14-19f0-4a1d-9fc2-46f050329ca3.png)


    Image-7: movies_df DataFrame

  ![movies_df](https://user-images.githubusercontent.com/104603128/176983138-e35cc0f7-bbbd-46f2-8c05-bc1465cef62e.png)


### Deliverable-4

    - SQL movies table data replaced by movies_df data.

    Image-8: Row count of movies table
    
  ![movies_query](https://user-images.githubusercontent.com/104603128/176983182-12c0ece6-45f6-4775-b417-ca148ee7e942.png)

  ![movies_query2](https://user-images.githubusercontent.com/104603128/176983251-a83ae6d1-6f28-4f46-842c-11c32d52597d.png)


    - Data added to ratings table in SQL database from MovieLens rating CSV file.
    
    Image-9: Row count of ratings table
    
  ![ratings_query](https://user-images.githubusercontent.com/104603128/176983196-a776054d-e765-499e-8ce0-1847aeafb256.png)
    
    - Displayed Elapsed time for adding data to the database.

    Image-10: Elapased time displayed
    
  ![Time Elapsed Display](https://user-images.githubusercontent.com/104603128/176983208-ae569c79-efa4-4a60-814f-00c68808a941.png)



