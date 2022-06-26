# Amazon_Vine_Analysis

## Overview
The purpose of this project is to analyze Amazon reviews written by members of the paid Amazon Vine program, a service that allows manufacturers and publishers to receive reviews of their products and determine if there are any biases between Vine members and Non-Vine member's reviews.

Companies that will pay a fee to Amazon and may provide free products to Vine members who are then required to publish a review. In order to determine if there is any bias towards favorable reviews from Vine members vs. non-members, we need to identify the percentage of 5 star ratings to total rating. As part of this exercise, we were asked to choose from 50 datasets to extract, transform and load into a dataframe in order to complete our analysis. Throughout this analysis, we use:

PySpark to extract the dataset, transform the data, connect to AWS RDS instance and load the transformed data into pgAdmin.
Google Colaboratory to import PySpark libraries and connect to Postgres in order to create SQL tables and export the results.
Of the 50 datasets, I chose to analyze reviews that were made by users in the Health and Personal Care.

https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Health_Personal_Care_v1_00.tsv.gz

## Results
The dataset had over 3096336 Customers reviews recorded. In order to focus on reviews that would be considered more likely to be helpful, we needed to filter the dataset by:

Count of Total Votes equal or greater than 20.
Percent of Helpful Votes to Total Votes equal or greater than 50%.

