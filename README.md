# DYD Data

## Overview
What heating/cooling setpoints are appropriate for the reference building in a high-performance residential standard?

## The Task
Extract the data from the BigQuery dataset and get in a format that can be analyzed by staff at Mathis Consulting.

## Data
There are two tables in the dataset, “dyd” and “meta_data” which exist in the Google Cloud Platform. The “dyd” table is quite large and has a lot of fields that are not needed. The “meta_data” table is smaller. The “Identifier” field exists in both tables and will be the field in which data will be merged. Sorting  “meta_data” table by “First_Connected” date shows data from 2010-2019.  Sorting  “dyd” table by “date_time” date shows data from 2017-2021. Data from 2017-2019 will be extracted from the “dyd” table. 

## Process
1. Clean extract the wanted columns from the tables and clean all the data by removing duplicates and NULLS.

2. Merge the two datasets on "Identifier."

3. Select the wanted dates (winter and summer solstice).

4. Establish final queries based on home vintage and country. Then aggregate the temperature control, heating, cooling based on vintage (increments of 5 years)

5. Export tables to CSV files

6. Bring in to Jupyter Notebook and combine CSVs for each vintage for summer and winter

7. Export CSV files (summer and winter)
