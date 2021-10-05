# Project: Data Modeling with Postgres - A Song Play Analysis
> Claudia Scholz

## Project Description 

The startup Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. To do so a database schema and ETL pipeline for analysis along a postgres database has been created to optimize on their song play analysis. 

## Files in Project
In the project you'll find the following files.

* `create_tables.py`: Python Scrip for creating and dropping tables in the database.

* `etl.py`: Python Script running the ETL Pipeline to put Sparkify's data from JSON files into the database.

* `sql_queries.py`: Python Script with all databse relevant queries, used by create_tables.py and etl.py.

* `etl.ipynb`: Notebook to develop the ETL Pipeline.

* `test.ipynb`: Notebook to visualize and test the ETL process along with the created tables.


## How to Run the Project

***create_tables.py*** to create the database along with its tables.
***etl.py*** to process the complete data from the JSON files and put them in the database.
***test.ipynb*** to check wether etl.py was succesfull creating the content of the database.
***etl.ipynb*** to test smaller steps instead of the complete ETL Pipeline.
