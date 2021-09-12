# Analyze MovieLens Data

## Project Description

Import csv data about movies and their ratings into HDFS, then create tables from the imported files in Hive.
Once imported, create queries to analyze and display data about the movies and their ratings.
For e.g.; display first 5 entries from movies table, count number of unique movies, Which movie received the highest number of ratings, top 25 most rated movies etc.

## Technologies Used

* Hive
* HDFS

## Features

List of features:
* Creating Hive tables form raw data.
* Processing and analysis of data can be done on created tables. 

To-do list:
* More processing can be done on this type of datasets.

## Getting Started
  -clone the project 
  >git clone https://github.com/shivajigoulikar/project1.git
  
  -Download Hadoop.

## Usage

Make sepreate directories to load the tables.
Ex:
> hdfs dfs -mkdir /user/maria_dev/project1/ratings

Copy the data to the respective directories:
Ex:
>hdfs dfs -put ./ratings.csv /user/maria_dev/project1/ratings/

Creating external table
Ex:
>create external table ratings(userid int, movieid int, rating float, tstamp string)                                                                                         
>row format delimited                                                                                                                                              
>fields terminated by ','                                                                                                                                          
>location '/user/maria_dev/project1/ratings';

Create Database
>Create Database;

use that database
>use database;

check whather the created tables exists or not 
>show tables;

Now start with queries
Ex:
>select * from movies limit 5;


