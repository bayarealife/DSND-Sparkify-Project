# DSND-Sparkify-Project

Udacity Data Science Nano Degree Program Capstone Project - Sparkify

The blog is published at this link:
https://kyoko-desiderio.medium.com/seattle-airbnb-top-listings-trends-6b3b034acd12

This repository is a container for the python script and data file

Library Requirement
pandas==1.1.3
pyspark==3.1.2
matplotlib==3.3.1
numpy==1.19.2
seaborn==0.11.0


What's Included
DSND-Sparkify-Project/ |--Sparkify.ipynb -- Python Notebook script to analyze the data, train models using different algorithms and tune the best model. |-- Data/ -- data folder containing the raw data | |-- listings.csv -- Detailed Listings data for Seattle

Documentation
In order to run the script, download the files (keep the folder hierarchy as is) under Jupyter directory, open the script file in the Notebook and run.

Motivation
I would like to find popular listings and the differences from non-popular listings in order to provide tips to those who want to increase bookings.

Methodoloty
Comparing the pre-determined metadata in each group will help identifying what factors may help booking the property. In this analysis, the property with 80% or more booking is defined as popular listing and less than 80% booking is grouped in non-popular listing.

Business Questions:
Does property neighborhood have effect on popularity?
Does Superhost status have effect on popularity?
Does Host ID Verification Status have effect on popularity?
Does Property Type have effect on popularity?
Does Host Response have effect on popularity?
Summary of the Analysis
The selected metadata -- Neighbourhood, Superhost Status, Property Type and Host Response all showed some patterns in each group except the diffference in Host ID Verification status was very minimal.

Some of the neighbourhood were identified as slightly more popular than others.
Superhost status was slightly advantageous than non-Superhost status
The difference for Host ID Verification status was very minimal.
Entire property appealed to more customers than shared rooms and apartment.
Although being responsive appealed to more customers, but it does not necessarily have to be prompt.
Data Sources
Datasets used in this analysis was collected from this source: http://insideairbnb.com/get-the-data.html File location:
http://data.insideairbnb.com/united-states/wa/seattle/2021-02-21/data/listings.csv.gz http://data.insideairbnb.com/united-states/wa/seattle/2021-02-21/data/calendar.csv.gz <-- This file could not be uploaded to this repository due to size limiation

Data Description
The data files are in CSV format.

""""listings.csv"""" The file contains 4197 records and 74 fields. The field list is as follows: 'id', 'listing_url', 'scrape_id', 'last_scraped', 'name', 'description', 'neighborhood_overview', 'picture_url', 'host_id', 'host_url', 'host_name', 'host_since', 'host_location', 'host_about', 'host_response_time', 'host_response_rate', 'host_acceptance_rate', 'host_is_superhost', 'host_thumbnail_url', 'host_picture_url', 'host_neighbourhood', 'host_listings_count', 'host_total_listings_count', 'host_verifications', 'host_has_profile_pic', 'host_identity_verified', 'neighbourhood', 'neighbourhood_cleansed', 'neighbourhood_group_cleansed', 'latitude', 'longitude', 'property_type', 'room_type', 'accommodates', 'bathrooms', 'bathrooms_text', 'bedrooms', 'beds', 'amenities', 'price', 'minimum_nights', 'maximum_nights', 'minimum_minimum_nights', 'maximum_minimum_nights', 'minimum_maximum_nights', 'maximum_maximum_nights', 'minimum_nights_avg_ntm', 'maximum_nights_avg_ntm', 'calendar_updated', 'has_availability', 'availability_30', 'availability_60', 'availability_90', 'availability_365', 'calendar_last_scraped', 'number_of_reviews', 'number_of_reviews_ltm', 'number_of_reviews_l30d', 'first_review', 'last_review', 'review_scores_rating', 'review_scores_accuracy', 'review_scores_cleanliness', 'review_scores_checkin', 'review_scores_communication', 'review_scores_location', 'review_scores_value', 'license', 'instant_bookable', 'calculated_host_listings_count', 'calculated_host_listings_count_entire_homes', 'calculated_host_listings_count_private_rooms', 'calculated_host_listings_count_shared_rooms', 'reviews_per_month'

""""calendar.csv"""" The file contains 1531652 rows and 7 columns. The field list is as follows: 'listing_id', 'date', 'available', 'price', 'adjusted_price', 'minimum_nights', 'maximum_nights'

Reference
https://pandas.pydata.org/docs/reference/index.html
