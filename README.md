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
![](https://github.com/zxinranz/img-folder/blob/main/%E6%88%AA%E5%B1%8F2023-06-11%20%E4%B8%8B%E5%8D%8811.35.39.png)
- For `yelp_business`, we check for missing values and outliers.
- We remove businesses that are closed all seven days of the week and businesses with no business hours information (`yelp_business_hours`). 
- For `yelp_checkins`, `yelp_review`, `yelp_tip`, and `yelp_user`, we examine for the presence of outliers. 
- We remove user information from the table if it does not have a name, review, and registration information (`yelp_user`).

## Data Analysis 
### Customer Dimension
![](https://github.com/zxinranz/img-folder/blob/main/%E5%9B%BE%E7%89%871.png) Based on the latest registration date.<br>

#### On average, how many reviews does an ordinary user post per month since creating their account? How many reviews does an elite user post on average per month?

![](https://github.com/zxinranz/img-folder/blob/main/%E5%9B%BE%E7%89%872.png)
![](https://github.com/zxinranz/img-folder/blob/main/%E5%9B%BE%E7%89%873.png)

#### The number and proportion of reviews considered useful, funny, and cool?

![](https://github.com/zxinranz/img-folder/blob/main/%E5%9B%BE%E7%89%874.png)
![](https://github.com/zxinranz/img-folder/blob/main/%E5%9B%BE%E7%89%875.png)

It can be observed that on average, elite users post 2.98 reviews per month, which is approximately 10.2 times more than regular users.

Elite users receive 2.10 times more useful evaluations, 1.14 times more funny evaluations, and 1.63 times more cool evaluations compared to the number of reviews they post. These figures are respectively 3.56, 5.43, and 7.76 times higher for elite users compared to regular users. Elite users have visited a significantly higher number of businesses and posted more reviews, and their reviews are more likely to receive praise. 

It is also noticed that regardless of user type, the probability of receiving useful evaluations is much higher than receiving funny and cool evaluations. This indicates that users focus more on the content rather than the language style and wording when writing reviews. Other users, when reading reviews, also pay more attention to the usefulness of the content.

#### Are reviews with a higher number of useful votes more positive or more negative? What are the characteristics of the review length for funny and cool evaluations?

Let's separately analyze the number of reviews that received more than 1000, 500, 200, and 100 useful votes. We'll calculate the average rating given by customers for those reviews and the average length of the reviews.

![](https://github.com/zxinranz/img-folder/blob/main/%E5%9B%BE%E7%89%876.png)

For reviews that received more than 1000 useful votes, there are a total of 11 reviews. On average, these reviews gave the restaurant a rating of 1.3 stars, and the average length of these reviews is 2204 words.

![](https://github.com/zxinranz/img-folder/blob/main/%E5%9B%BE%E7%89%877.png)

For reviews that received more than 500 useful votes, there are a total of 36 reviews. On average, these reviews gave the restaurant a rating of 1.3 stars, and the average length of these reviews is 1456 words.

![](https://github.com/zxinranz/img-folder/blob/main/%E5%9B%BE%E7%89%878.png)

For reviews that received more than 200 useful votes, there are a total of 138 reviews. On average, these reviews gave the restaurant a rating of 1.8 stars, and the average length of these reviews is 1342 words.

![](https://github.com/zxinranz/img-folder/blob/main/%E5%9B%BE%E7%89%879.png)

For reviews that received more than 100 useful votes, there are a total of 408 reviews. On average, these reviews gave the restaurant a rating of 2.4 stars, and the average length of these reviews is 1479 words.

The regression plot titled "Highest Rating with increasing Useful" illustrates the trend of the highest rating (stars) as the number of useful tags in the reviews increases.

The x-axis represents the thresholds of useful tags, ranging from 100 to 1000 with an interval of 20.

The y-axis represents the corresponding highest rating values for each threshold. This plot helps us understand the relationship between the number of useful tags and the highest rating.

![](https://github.com/zxinranz/img-folder/blob/main/%E5%9B%BE%E7%89%8710.png)
![](https://github.com/zxinranz/img-folder/blob/main/%E6%88%AA%E5%B1%8F2023-06-12%20%E4%B8%8B%E5%8D%883.01.31.png)
![](https://github.com/zxinranz/img-folder/blob/main/%E6%88%AA%E5%B1%8F2023-06-12%20%E4%B8%8B%E5%8D%883.01.42.png)

#### Average star ratings of restaurants based on different scores given by users.

![](https://github.com/zxinranz/img-folder/blob/main/%E5%9B%BE%E7%89%8713.png)

#### Statistics of the star ratings for restaurants that have received 5-star reviews from users.

![](https://github.com/zxinranz/img-folder/blob/main/%E5%9B%BE%E7%89%8714.png)

#### The most frequently reviewed states by users.

![](https://github.com/zxinranz/img-folder/blob/main/%E5%9B%BE%E7%89%8716.png)

#### The relationship between review count, photo count, and number of fans. Regarding the difference between elite users and non-elite users.

*Elite users*

![](https://github.com/zxinranz/img-folder/blob/main/%E5%9B%BE%E7%89%8717.png)

*Non-elite users*

![](https://github.com/zxinranz/img-folder/blob/main/%E5%9B%BE%E7%89%8718.png)

Elite users have approximately 10 times the number of reviews compared to the number of their fans. The number of fans and the number of photos posted by elite users are relatively similar.

On the other hand, for non-elite users, the number of reviews is approximately 28 times the number of their fans, while the number of photos posted is about 0.38 times the number of their fans.

Comparing elite users and non-elite users, we can observe that the total number of reviews is similar between the two groups. However, elite users have a higher ability to attract fans through their reviews, indicating a higher probability of gaining followers. Elite users also post a significantly higher number of photos compared to non-elite users, approximately 6 times more. However, the number of fans is less than 3 times that of non-elite users, suggesting that photos are less likely to attract the attention of other users and have a lower probability of gaining followers.

#### The difference lies in the number of fans between elite users and non-elite users

![](https://github.com/zxinranz/img-folder/blob/main/%E5%9B%BE%E7%89%8719.png)

On average, elite users have approximately 22 fans each, which is more than 45 times the number of fans for non-elite users. It can be speculated that when Yelp selects elite users each year, the number of fans is an important criterion. This is because the number of fans not only indicates the user's high reliance on the platform and their ability to provide more valuable information but also brings more traffic, which is vital for the survival of the platform.

![](https://github.com/zxinranz/img-folder/blob/main/%E5%9B%BE%E7%89%8720.png)

The total number of fans for non-elite users is approximately 0.47 times the number of non-elite users, with an average of less than 1 fan per person. This indicates that a significant number of non-elite users do not have any fans.

### Business Dimension

#### Number of restaurants by star rating? Average star rating of restaurants? What is the relationship between the number of stars and ratings, the average rating, and the number of good and bad ratings?

First, we calculate the average star rating of the restaurants.

![](https://github.com/zxinranz/img-folder/blob/main/%E5%9B%BE%E7%89%8721.png)

Since the star rating ranges from 1 to 5 stars, with each 0.5-star increment considered as a category, the average star rating of the restaurants is expected to be around 3 stars if the ratings follow a normal distribution. However, the data shows that the average rating is higher than 3 stars, indicating that the majority of restaurants have received ratings of 3 stars or higher. This suggests that the platform tends to assign higher star ratings to restaurants and is less inclined to give lower ratings.

Next, we count the number of restaurants in each star rating:

![](https://github.com/zxinranz/img-folder/blob/main/%E5%9B%BE%E7%89%8723.png)

The histogram approximately follows a left-skewed distribution, indicating that there are more high-rated restaurants compared to low-rated ones, which aligns with the information provided by the mean. We can observe that the highest number of restaurants has a rating of 4.0, accounting for 19.19% of the total, closely followed by 3.5-rated restaurants at 18.35%. The majority of restaurants have managed to satisfy their customers to a considerable extent.<br>
It is noteworthy that there is a significant number of 5-star restaurants, with 15.78% of all restaurants belonging to this category, even surpassing the number of 4.5-star restaurants. On one hand, user ratings can influence a restaurant's star rating. When users have an exceptional dining experience, they tend to give a perfect rating to express their appreciation, support, and fondness, often overlooking any flaws the restaurant may have. In such cases, the restaurant's shortcomings are typically seen as insignificant or overshadowed by its positive aspects.<br>
On the other hand, the platform itself may be inclined to promote 5-star restaurants over those with a rating of 4.5 stars. This benefits the platform's advertising efforts since a perfect score serves as a compelling selling point compared to a rating of 4.5 stars. Additionally, restaurants that are actively promoted by the platform can offer exclusive deals or discounts on the Yelp platform, thereby reciprocating their appreciation to the platform and attracting a substantial influx of customers for both the business and the platform.

For each star rating, we then analyze the average rating given by users and the number of reviews.
