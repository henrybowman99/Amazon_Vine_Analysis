# Amazon Vine Analysis

## Overview

In this project I used a dataset containing Amazon reviews for sports equipment products. First, I created several dataframes on google colab using python and the pyspark library. Then I exported these dataframes to tables in pgAdmin using an RDS database sever from Amazon Web Services. This step was necessary because the size of the dataframes were too large to store on the hard drive of my laptop. Then, using pgAdmin, I exported the vine table to a csv file. Lastly I read this vine csv file into a new jupyter notebook and ran my final analysis to provide metrics that compare reviews for products that are reviewed by vine members to those that are not involved in the vine program.

## Results

NOTE: The below analysis uses a vine dataframe that has been filtered to inclue product reviews in which the total votes >= 20 and the percentage of helpful votes is more than half the number of total votes.

![Vine_program_total](https://user-images.githubusercontent.com/95651156/165016953-0e24a724-5f81-4595-8080-8a1e3ac02f70.png)


![no_vine_program_total](https://user-images.githubusercontent.com/95651156/165017125-e7c1da8b-1fd4-4bff-b7b1-9fef0de6761f.png)

61,614 of reviews were for products not included in the vine program, while just 334 of the reviews were for products in the vine program.

![five_star_count_vine](https://user-images.githubusercontent.com/95651156/165017545-e2b66e33-22ca-4615-b08e-8974889c24c8.png)

![five_star_count_no_vine](https://user-images.githubusercontent.com/95651156/165017549-f7f7cefa-de27-4aaf-9c17-87473da2101e.png)

139 of the reviews for products in the vine program received 5 stars while 32,665 of the reviews for products not in the vine program received 5 stars.

![five_star_percentage_vine](https://user-images.githubusercontent.com/95651156/165017708-bab3a348-2a79-4cd0-8d43-4bf204628762.png)

![five_star_percentage_no_vine](https://user-images.githubusercontent.com/95651156/165017722-0f315bf0-9e9e-413c-b086-b2fef508e5ec.png)

41.62% of reviews for vine products received 5 stars while 53.02% of non-vine products received 5 stars.

## Summary

Based on my above analysis, there is no indication that there exists positivity bias for reviews in the vine program. In fact, there is evidence that bias for vine products actually runs in the opposite direction. This claim is supported by the fact that 41.62% of vine reviews are of the 5-star variety compared to 53.02% for non-vine reviews.

To analyze this notion of positivity bias further, I would recommend expanding beyond the metric of 5-star reviews. One way to do this would be to find the average star rating for both vine and non-vine reviews and compare the two values. 
