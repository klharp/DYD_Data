# DYD Data

## Overview
What heating/cooling setpoints are appropriate for the reference building in a high-performance residential standard?

## The Task
Extract the data from the BigQuery dataset (7.6TB) and get in a format that can be analyzed by staff at Mathis Consulting. The team determined that it wanted the data by state/province.

## Data
There are two tables in the dataset, “dyd” and “meta_data” which exist in the Google Cloud Platform. The “dyd” table is quite large and has a lot of fields that are not needed. The “meta_data” table is smaller. The “Identifier” field exists in both tables and will be the field in which data will be merged. 

## Process
1. Clean extract the wanted columns from the tables and clean all the data by removing duplicates and NULLS.

2. Merge the two datasets on "Identifier."

3. Select the wanted time and dates (by day hours and night hours, month).

4. Establish final queries based state, year, day/night. 

5. Export tables to CSV files

6. Bring in to Jupyter Notebook and aggregate the data for temperature control, heating, and cooling based on each identifier.

7. Export CSV files for each state, month, and day/night hours.
