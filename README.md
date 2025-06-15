# Spotify End-To-End Data Engineering Project

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

