# PROJECT DESCRIPTION:This project is about creating a data model for a music streaming app. 

The data  model followed here is of a Star Schema. We have a fact table (_SongPlays_) and  four dimension tables (_songs, artists, users, time_).

We have the below files:
**sql_queries.py:** Contains the DDLs of the tables, insertion statements, drop statements along with a select query to fetch primary keys from the dimension tables songs, artists for the fact table.
**create_tables.py:** File to execute the ddls, insertions queries in the sql_queries file
**etl.ipynb:** Read Data from the json files and insert samples of data
**test.ipynb:** To validate the creation, insertion of data for all the tables
**etl.py:** To list, process all the json files and insert data into the tables

Data from the sparkify music streaming app is stored in json files and is of two types _song data_ and _log files_. In _etl.py_ functions performing below actions are included:
* list all the json files in a given directory
* loop through the list of files, read each json file into a dataframe and load the data into corresponding table 