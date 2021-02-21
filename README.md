## Project Overview

The purpose of this project is to create a data pipeline using an ETL to extract the JSON Wikipedia and CSV Kaggle dataset from their respective files, transform the datasets by cleaning them up and joining them together, and load the cleaned dataset into a SQL databases.

## Resources

- Datasets (Resources folder): wikipedia-movies.json, ratings.csv, movies_metadata.csv
- Software: PostgreSQL 11.10 and Jupyter Notebook

## Results

We extract, transform and load into PostgreSQL 26MM lines of data and these were cleaned using drop.na, lambda function, regex.

### Step 1: load the raw data

Please refer to the file "ETL_function_test.ipynb" to better understand the important of the JSON and CSV files using OS, JSON and PANDAS module from python 3.

### Step 2: transform

Please refer to the file "ETL_clean_wiki_movies.ipynb" to better understand the cleaning of the datasets. The function "change_column_name" is used to convert a dataframe to be universal with the others. The function extract_transform_load is used to clean the wikipedia & Kaggle datasets by using Regex (RE) for a search pattern like the function below.

> release_date.str.extract(f'({date_form_one}|{date_form_two}|{date_form_three}|{date_form_four})', flags=re.IGNORECASE)

### Step 3: load the data

Below are the results after the cleaning in our database.

<img src="https://github.com/poboisvert/Movies-ETL/blob/main/Resources/movies_query.png?raw=true" width="250" />
<img src="https://github.com/poboisvert/Movies-ETL/blob/main/Resources/ratings_query.png?raw=true" width="250" />
