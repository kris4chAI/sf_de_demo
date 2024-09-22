1. Analyze the data and describe all the fields you will be extracting to derive meaningful insights from the dataset
    -> analyze method
        read json 
        - derive table metadata
        - derive column metadata
        - derive data
2. upload the json to s3 bucket
3. write python method to read from s3 
    s3 bucket will have two folders - raw data and derived data
4. call analyze method and write three json files - table_metadata.json, column_metadata.json, data.json
5. Create external stage on derived location for bronze tables - external table
6. Create methods for data type conversion (date, data quality checks - valid date/timestamp, valid state,valid zipcode )
7. Write standardized data to silver - managed table in snowflake
8. write queries to generate insights. 
9. Create 2 databases - dev/uat
10. put all the code from git into snowflake notebook


- data
- setup 
    - create s3.py 
    - create sf_objects.py
- processing
    - extract_data.py
    - populate_bronze.py
    - populate_silver.py
    - populate_gold.py
- analyze
    - generate_insights.sql
- ci
    -dev.yml
    -prod.yml
- readme.md

s3 (raw (1 json) -> derived (3 json/csv) ->bronze (3 parquet)) -> (data quality, standardization) silver (sf table) ->  

