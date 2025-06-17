# Spotify End-To-End Data Engineering Project (Python)

## Introduction
In this project, we will build an ETL (Extract, Transform, Load) pipeline using the Spotify API on AWS. The pipeline will retrieve data from the Spotify API, transform it to a desired format, and load it into an AWS data store.

## Overview:
- Integrating with Spotify API and extracting Data
- Deploying code on AWS Lambda for Data Extraction
- Adding trigger to run the extraction automatically
- Writing transformation function
- Building automated trigger on transformation function
- Store files on S3 properly
- Building Analytics Tables on data files using Glue and Athena

## About Dataset:
This Spotify API data contains information about musics, artists, albums and songs. [Spotify API link](https://developer.spotify.com)

## Tech Stacks:
- Python (libraries: spotipy, pandas)
- AWS Lambda: A serverless computing service.
- AWS CloudWatch: A monitoring service for AWS resources.
- AWS S3 (Simple Storage Service)
- AWS Glue Crawler: A service that crawls your data sources, identifies data format and schema.
- AWS Glue Catalog: A metadata repository.
- AWS Athena: An interactive query service that makes it easy to analyze data in Amazon S3.
  
## Architecture Diagram:
![Architecture Diagram](https://github.com/Logan0818/spotify-end-to-end-data-engineering-project/blob/main/spotify%20architecture%20aws.png)

## High Level Steps and Notes
### Extract
1. Register an App in Spotify API site, get client id and cliend secret
2. Use python library **spotipy** to connect to the API (develop your python codes in Jupyter notebook first)
3. Spotify has locked access to most playlist, but we can use this one https://open.spotify.com/playlist/3cEYpjA9oz9GiPac4AsH4n
4. Deploy our code on Lambda (create function, create environment variables) and test
5. Lambda does not support external library, need to create a lambda layer
6. Import boto3 package to interact with S3, load raw data (json file) into raw_data/to_process folder

### Transform and Load
1. Study the API response (json file structure) and use for loop to get what we want from it (information about albums, artists, songs)
2. Pull the file in raw_data S3 folder and apply transformation logics, convert data to python dataframe.
3. Generate three csv files and put the files back to S3 bucket into transformed_data folder.
4. Copy raw data from raw_data/to_process folder to raw_data/processed folder, then delete raw file in raw_data/to_process folder.

### Reference
https://www.linkedin.com/in/darshil-parmar/
