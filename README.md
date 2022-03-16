# Yelp-DataSet-analysis-using-BigData-Tools
The Yelp dataset was originally released in order for students to do research and analysis in to how food trends begin and how they impact locations. The dataset includes data about businesses, reviews, users, checkins, tips, and photos. Here in my project I used users,review and business dataset.

## Table of Contents
1. [Introduction](##introduction)
2. [Goal](##goal)
3. [Technology Stack](##technology-stack)
4. [Bucket Calculation](##bucket-calculation)
5. [Project Architecture](##project-architecture)
6. [ER Diagram](##er-diagram)
7. [Analysis](##analysis)

## Introduction
Most businesses seek to get reviews on their goods and services one way or another. It is a most basic way for the business to improve their efficiency and subsequently their bottom-line. Get the review is not only the issue, ability to extract and visualize analytics from review data is critical to business success.

In this Project, we will use the yelp review dataset to analyze businesses and reviews over a period of time. Perhaps we will spot potential gaps in service delivery or see how business thrive in different scenarios.

Beyond processing this data, we will ingest the final output of our data processing in PowerBI and use the visualization tool to visualize various kinds of ad-hoc reports from the data.

## Goal
Goal is to create data pipeline for yelp dataset to finally load in hive external tables so that analysis team can make use of this data. Along with this goal is to extract required data using some free-form queries for geeral business usecases.

## Technology Stack
- HDFS
- Hive
- PowerBI

## Bucket Calculation

Block Size in HDFS = 128 MB

Size of review dataset = 5120 MB

5120/128 = 40

2^x = 40 where x will be number of buckets

Hence we will take number of bucket = 6

Size of user dataset = 3205 MB

3205/128 = 25

2^x = 25  where x will be number of buckets

Hence we will take number of bucket = 5


## Project Architecture

![image](https://user-images.githubusercontent.com/100192236/158610938-a835ab70-4d08-4028-9613-31b497ddddae.png)


## ER Diagram
![image](https://user-images.githubusercontent.com/100192236/158611046-2b242818-4a95-439d-9042-c65e39e1fd53.png)

## Analysis

#### Top Users who posted reviews (by count)
![image](https://user-images.githubusercontent.com/100192236/158611143-69a81941-23f4-4d82-b1d1-27b1d40edf95.png)

#### Average Rating of business per year
![image](https://user-images.githubusercontent.com/100192236/158611924-77a07bdd-a90a-4911-878f-8e1af5ed2efa.png)

#### Top users who posted funny reviews
![image](https://user-images.githubusercontent.com/100192236/158611455-adf6b1a9-cd5f-4867-a580-5c8fce4261ec.png)

#### Top users who posted useful reviews
![image](https://user-images.githubusercontent.com/100192236/158611533-d956d056-045a-4a88-b6f8-9dd2227a2b68.png)

#### Top users who have most fans
![image](https://user-images.githubusercontent.com/100192236/158611589-22a957f2-d1c0-47c6-886d-716758dbf743.png)

#### Business who has most reviews
![image](https://user-images.githubusercontent.com/100192236/158611634-720e984b-6de1-4ac2-84b4-4968782ccdac.png)
