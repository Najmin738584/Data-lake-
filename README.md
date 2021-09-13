## Project : Data Lake

A music streaming startup Sparkify, has grown their user base and song database even more and want to move their data warehouse to a data lake. Their data resides in S3, in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.They want their analytics team to find what songs their users are listening to.

The aim of the project is to build an ETL pipeline that extracts their data from S3, processes them using Spark, and loads the data back into S3 as a set of dimensional tables.

###  Datasets

There are two datasets that reside in S3. 
1] Song data
2] Log data

### preliminaries

Make sure you have an AWS secret and access key and an own S3-Bucket as well. Then edit the dl.cfg file the following entries:
AWS_ACCESS_KEY_ID =                     
AWS_SECRET_ACCESS_KEY =                

### ETL Pipeline

Run python3 etl.py in a terminal to import the raw sets from S3 bucket and store data in the following star schema:  

Fact Table
1] songplays - records in log data associated with song plays i.e. records with page NextSong (songplay_id, start_time, user_id, level,       song_id, artist_id, session_id, location, user_agent)

Dimension Tables
1] users - users in the app(user_id, first_name, last_name, gender, level)
2] songs - songs in music database (song_id, title, artist_id, year, duration)
3] artists - artists in music database(artist_id, name, location, lattitude, longitude)
4] time - timestamps of records in songplays broken down into specific units (start_time, hour, day, week, month, year, weekday)




