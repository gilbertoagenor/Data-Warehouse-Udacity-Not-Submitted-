# Project summary

## Project description

In this project, we built an ETL pipeline for a database hosted on Redshift. To complete the project, we loaded data from S3 to staging tables on Redshift and execute SQL statements that create the analytics tables from these staging tables. The tables used were:

1. songplays - records in event data associated with song plays
2. users - users in the app
3. songs - songs in music database
4. artists - artists in music database
5. time - timestamps of records in songplays broken down into specific units

## Project files and running the project

To run the project we first need to create a cluster and appropriate IAM Roles. This as done using the file create_cluster.ipynb.

The project template includes four files:

1. create_table.py - where we create your fact and dimension tables for the star schema in Redshift.
2. etl.py - where we load data from S3 into staging tables on Redshift and then process that data into your analytics tables on Redshift.
3. sql_queries.py - where we define SQL statements, which will be imported into the two other files above.
5. dwh.cfg - where all credential information is store

Once the sql_queries are created in sql_queries.py file, including the SORTKEY and DISTKEY decisions to optimize the queries, we can run the create_table.py file to create the tables in Redshift followed by the etl.py to actually load the data into the tables so we are able to work with them on future projects such as adding data quality checks and creating a dashboard for analytic queries on new database.

