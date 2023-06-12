![image](https://github.com/zxinranz/yelp_data_analysis/assets/55777804/c4a1f809-33e1-404b-b672-91741af4f5be)
# Yelp Data Analysis
> By Noora Zhou
## Introduction
**Yelp** is an online platform that allows users to search for and browse information about businesses, including their address, phone number, hours of operation, and other details. It also enables users to view reviews and ratings of businesses written by other users, and to write and publish their own reviews and comments. Yelp's review system leverages the power of social networking, encouraging users to share their experiences and opinions about businesses, which helps other users to find better businesses. Yelp was founded in 2004 in the United States and has expanded to other countries including Canada, the United Kingdom, Australia, France, Germany, Italy, and Switzerland, among others.<br>

**The Yelp dataset** is a collection of data related to businesses, reviews, users, and other interactions on the Yelp platform. The dataset includes information from several cities across the United States, covering a variety of business categories and user demographics.
The purpose of this dataset is to enable researchers, data analysts, and data scientists to explore and analyze the dynamics of the Yelp platform and gain insights into user behavior, business performance, and market trends. With the increasing popularity of online review platforms like Yelp, this dataset provides a valuable resource for understanding the factors that influence customer satisfaction, business success, and platform growth.

## Project Summary
Comprehensive exploratory data analysis of large-scale yelping reviews broken down by user, customer and platform dimensions using MySQL and Tableau, with python for in-depth research and supplementation to provide data-driven insights.

## Database

### `yelp_tip.csv` 

This is a dataset that contains Tips information posted by Yelp users on business pages. It typically includes the following fields:

1. `user_id`: The user ID of the user submitting the tip.
2. `business_id`: The business ID of the business receiving the tip.
3. `text`: The text content of the tip.
4. `date`: The date and time when the tip was submitted.
5. `compliment_count`: The number of compliments the tip received.
6. `type`: The type of the data entry, typically "tip".
7. `cool`: The "cool" rating given by users to the tip.
8. `funny`: The "funny" rating given by users to the tip.
9. `useful`: The "useful" rating given by users to the tip.

These data can be used to explore user behavior and interactions on Yelp, gaining insights into user feedback and evaluations of businesses. This information can be valuable for businesses and the Yelp platform to make improvements and optimizations.

###  `yelp_business.csv` 

This dataset contains information about Yelp businesses, including the following fields:

1. `business_id`: Unique identifier for the business
2. `name`: Name of the business
3. `address`: Address of the business
4. `city`: City where the business is located
5. `state`: State or province where the business is located
6. `postal_code`: Postal code of the business location
7. `latitude`: Latitude coordinate of the business location
8. `longitude`: Longitude coordinate of the business location
9. `stars`: Rating of the business on a scale of 1 to 5
10. `review_count`: Number of reviews for the business
11. `is_open`: Indicator of whether the business is open or closed (0 for closed, 1 for open)
12. `categories`: Categories or types of the business, typically separated by commas

These fields provide basic information about Yelp businesses, including their names, addresses, location coordinates, ratings, review counts, open/closed status, categories, attributes, and operating hours. This data can be used to analyze the performance of businesses on Yelp, explore differences and similarities between businesses, conduct geographic analysis, and gain insights into the Yelp business ecosystem and consumer behavior.

### `yelp_business_hours.csv` 

The dataset contains information about the operating hours of Yelp businesses, including the following fields:

1. `business_id`: Unique identifier for the business, corresponding to the `business_id` field in the `yelp_business.csv` dataset.
2. `monday`: Operating hours of the business on Mondays.
3. `tuesday`: Operating hours of the business on Tuesdays.
4. `wednesday`: Operating hours of the business on Wednesdays.
5. `thursday`: Operating hours of the business on Thursdays.
6. `friday`: Operating hours of the business on Fridays.
7. `saturday`: Operating hours of the business on Saturdays.
8. `sunday`: Operating hours of the business on Sundays.

The operating hours are typically represented in hours, for example, "9:00-17:00" represents the operating hours from 9:00 AM to 5:00 PM. Fields where the business has not provided operating hours typically contain null values.

These fields provide information about the operating hours of Yelp businesses on each day of the week. They can be used to analyze the business's operating patterns, compare the operating hours of different businesses, and perform analyses on consumer activity within specific time periods. These data can be combined with other business information from the `yelp_business.csv` dataset to gain a more comprehensive understanding of the business's operations.

### `yelp_checkin.csv` 

The dataset contains information about Yelp user registrations at businesses, including the following fields:

1. `business_id`: Unique identifier for the business, corresponding to the `business_id` field in the `yelp_business.csv` dataset.
2. `date`: Date of user registration in the format "YYYY-MM-DD".
3. `time`: Time of user registration in the format "HH:MM:SS".

This dataset records the date and time when Yelp users registered at businesses. The data can be used to analyze user registration activity, distribution of registration times, user registration patterns at different businesses, and more. This information can help businesses gain insights into user behavior, optimize their operations, and make data-driven decisions.

These data can be combined with other business information from the `yelp_business.csv` dataset to get a more comprehensive understanding of user registration patterns at businesses. It can assist businesses in gaining insights into their user base and making informed business decisions based on the data.

### `yelp_user.csv` 

The dataset contains information about Yelp users, including the following fields:

1. `user_id`: Unique identifier for the user.
2. `name`: User's nickname or username.
3. `review_count`: Number of reviews the user has posted.
4. `yelping_since`: Date when the user joined Yelp in the format "YYYY-MM-DD".
5. `friends`: List of user's friends, represented as a comma-separated list of user IDs.
6. `useful`: Number of times the user's content has been voted as "useful" by other users.
7. `funny`: Number of times the user's content has been voted as "funny" by other users.
8. `cool`: Number of times the user's content has been voted as "cool" by other users.
9. `fans`: Number of fans (users following) the user has.
10. `elite`: User's elite membership status, indicating whether the user has been an elite member of Yelp and listing the specific years.
11. `average_stars`: User's average rating.
12. `compliment_hot`: Number of times the user has been complimented for being "hot".
13. `compliment_more`: Number of times the user has been complimented for "more".
14. `compliment_profile`: Number of times the user has been complimented for their "profile".
15. `compliment_cute`: Number of times the user has been complimented for being "cute".
16. `compliment_list`: Number of times the user has been complimented for creating a "list".
17. `compliment_note`: Number of times the user has been complimented for a "note".
18. `compliment_plain`: Number of times the user has been complimented for being "plain".
19. `compliment_cool`: Number of times the user has been complimented for being "cool".
20. `compliment_funny`: Number of times the user has been complimented for being "funny".
21. `compliment_writer`: Number of times the user has been complimented for their "writing".
22. `compliment_photos`: Number of times the user has been complimented for their "photos".

These fields provide information about Yelp users, including their activity, engagement, ratings, and interactions with other users. The data can be analyzed to understand user behavior, preferences, and influence within the Yelp community.


### `yelp_review.csv` 

This is a dataset that contains reviews information posted by Yelp users on business pages. It typically includes the following fields:

1. `review_id`: The ID of this review.
2. `user_id`: The user ID of the user submitting the review.
3. `business_id`: The business ID of the business receiving the review.
4. `stars`: The stars given by the reviewer to the business.
5. `date`: The date when the review was submitted.
6. `text`: The text content of the review.
7. `useful`: The "useful" rating given by users to the review.
8. `funny`: The "funny" rating given by users to the review.
9. `cool`: The "cool" rating given by users to the review.

These data can be used to explore user behavior and interactions on Yelp, gaining insights into user feedback and evaluations of businesses. This information can be valuable for businesses and the Yelp platform to make improvements and optimizations.

## Data Cleaning
![]()
## Customer Dimension
