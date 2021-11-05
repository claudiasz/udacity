# Project: Data Warehouse - Song Play Analysis including AWS S3 and redshift

### Project Overview

Students will build an ETL pipeline that extracts data from S3, stages them in Redshift, and transforms data into a set of dimensional tables to continue finding insights.

* loading data from S3 to staging tables on AWS redshift
* database hosted on AWS redshift
* executing SQL statements to create analytics tables 

### Datasets

Data for the project is procided in public S3 data buckets. One containing info about songs and artists and one providing information on the user actions. Both are provided as JSON files.

### Database Schema

Two staging tables are copied from the JSON files in the S3 data buckets

#### Staging Tables

* staging songs
* staging events

#### Fact Table

* songplays

#### Dimension Tables

* users
* songs
* artists
* time

### Detailed Project Description

#### AWS SetUp

With the help of 'aws_setup.ipynb' create a new 'IAM user' in the AWS account and give it AdministratorAccess along with attaching policies. Secret and Key have to be provided to create the clients for 'EC2', 'S3', 'IAM' and 'Redshift'. Afterwards an 'IAM Role' is created that allows 'Redshift' to access the 'S3' data bucket. At last a 'Redshift Cluster' has to be created to get the host address 'DWH_ENDPOINT' and the 'DWH_ROLE_ARN'. All information is provided in the config file dwh.cfg.

#### ETL Pipeline

rRun test.ipynb to run create_tables.py and etl.py, this way the data is loaded from S3 to reshift, all tables are created and the subsequent data analytics can be performed.

#### Project Files

aws_setup.ipynb - initialize whole AWS setup
create_tables.py - where fact and dimension tables are created in redshift
dwh.cfg - AWS credentials and config
etl.py - where data is loaded from S3 into staging tables on redshift and data is processed into the analytics tables on redshift
sql_queries.py - where all SQL statements are defined
test.ipynb - to run create_tables.py and etl.py
README.md - project description